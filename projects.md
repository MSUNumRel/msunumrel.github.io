# Course Projects

More details about the course projects will be developed as the course proceeds. For now, here is are the basics.

## Midterm Project

Due March 12, 2019.

For the midterm project, you will develop a Tolman-Oppenheimer-Volkov (TOV) solver to compute the hydrostatic structure of a relativistic neutron star. You will use this to determine the maximum masses of cold neutron stars (NSs) for several different equations of state (EOS).

Your code should adhere to the course [Coding Standards](coding.md). 

1. Write a numerical solver for the spherically-symmetric TOV equations using a fourth-order Runge-Kutta integrator. Assume a polytropic EOS specified by $K$ and $\gamma$. You may find [these notes](notes/TOV_Notes.pdf) particularly helpful.
2. Determine the maximum mass of a cold NS for $K=3000$ (in $G=c=M_\odot=1$ units) and $\gamma=2.75$. 
3. Now, modify your code to use any arbitrary table-based EOS. Specifically, make your solver compatible with the EOS available on [stellarcollapse.org](https://stellarcollapse.org/equationofstate). There is example code on that site in C++ and Fortran for reading and using the tables there, and working with the EOS tables is trivial in Python using `h5py`. 
4. Determine the maximum mass for any five of the EOS available on stellarcollapse.org. 
5. Make mass vs. radius plots for these same five EOS. 

## Final Project

_Subject to change._

For the final project, you will work as a group to develop a general relativistic hydrodynamics solver, solving for the spacetime evolution using the conformal flatness approximation. The ultimate goal of this project will be a peer-reviewed publication in a suitable journal co-authored by the entire class. 