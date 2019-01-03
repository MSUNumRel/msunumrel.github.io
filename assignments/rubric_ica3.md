# Rubric for ICA 3

Arithmetic intensities:

- 2 flops, 3 loads, 1 store = 2/(8*4) = 1/16 flops/byte
- 1 flops, 1 load = 1/8 flops/byte (`s` is scalar in register)
- 1 flops, 2 loads = 1/16 flops/byte
- 2 flops, 2 loads, 1 store = 2/(8*3) = 1/12 flops/byte ('C' is scalar in register)

0.5 points for each (2 points total) If they forget to express this in flops per byte and instead do flops/word, take off 0.5 points but give them credit otherwise if their analysis is correct (i.e., if they counted right but didn't divide by 8 bytes, they should get a 1.5 for this).

## Questions

3. 0.5 point each for peak, bandwith of L1, L2, L3, and DRAM, and ridge points (3 points total)
4. Answers _kinda_ depend on their machine, but most machines will be very similar. Basically, compare the AI's for these kernels to the data they report and check if they come to the correct conlcusion. 0.5 points for each of the four kernels. Then 1 point total for suggesting optimization strategies (3 points total)

2 points if they produced and committed a correct Roofline plot.

10 points total for the assignment.