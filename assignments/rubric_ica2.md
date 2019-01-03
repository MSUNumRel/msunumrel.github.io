# Rubric for ICA 2

1. Did they submit correct code? (2 pts)  Is the code clean and readable? (1 pt)
2. $2N^3$ (1 pt)
3. Does their code do repeated calculations? They do not have to use `get_walltime.c` so long as the use an appropriate timer. (2 pt)
4. Do they report reasonably correct numbers for their machine's CPU? Do they explain how either multiple mult/add units per core or how vector processing units could affect this? (1 pt)
5. Did the produce a plot? Does it look right? (2 pt)
6. Should be less than peak by a lot, unless they were clever about enabling vectorization, etc. They should see the memory hierarchy and recognize it as such. (1 pt)

10 pts total. You can using 0.5 pt accuracy, if you like. Feel free to be lenient. Don't get bogged down in giving detailed comments, but give them brief hints about why you are taking away points. I find that if you are too strict or hard a grader, it's just inviting complaints. But be "fair," which is to say have a justification that you can hit them with if they complain about missing points.

I took a look at Steve Fromm's ICA 2 and I would probably give him a 10/10. See if you agree and you can then use that as a baseline for the others. Feel free to shoot me questions if there are any.