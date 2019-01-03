# Rubric for ICA 14

## OpenMP Tasks

Basically, if they turned in anything for this that is half-way correct, give them the points. This one is really straightforward and I wasn't looking for anything exotic. My code is bellow. It is a simple modification. Technically, the private and depend statement aren't required, but they are important in the case that this function is called from within a parallel region (which is the assumption here). 

10 points.


```C++
#define N 512
#define BS 16
#define EPS 0.000001

#include <iostream>
#include <cstdlib>
#include <time.h>

using namespace std;

void matmul_depend(float A[N][N], float B[N][N], float C[N][N])
{
    int i, j, k, ii, jj, kk;
    
    for (i = 0; i < N; i += BS)
        for (j = 0; j < N; j += BS)
            for (k = 0; k < N; k += BS)
            #pragma omp task private(ii, jj, kk) depend(in: A [i:BS] [k:BS], B [k:BS] [j:BS]) \
            depend(inout: C [i:BS] [j:BS])
                for (ii = i; ii < i + BS; ii++)
                    for (jj = j; jj < j + BS; jj++)
                        for (kk = k; kk < k + BS; kk++)
                            C[ii][jj] = C[ii][jj] + A[ii][kk] * B[kk][jj];
}
```