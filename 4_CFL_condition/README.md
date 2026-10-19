Notes on Step 3 - Convergence and CFL Criterion

Questions?
1. Why does the numerical solution tend to diffuse compared to the analytical solution?
2. Why is it necessary for the CFL number to remain below 1?
3. What causes a numerical solution to diverge when the velocity c is negative?

First we analyse a 1D linear convection. Changing the grid size, ploting solution in the 20th time step and the resultant CFL number (we maintain dt constant so CFL = c *dt/dx, and CFL reduces if we reduce the number of nodes (dx increases)). CFL IS RELATED TO dx not to nx.

We observed that linearconv(41) (cfl = 0.5) had much more diffusion than linearconv(81) (cfl = 1.0)

Wen CFL gets grater then 1 we have huge instabilities. These instabilities appear because for CFLs greater than 1, the wave (case of 1D linear equation) have traveled a distance greater than dx in the time step dt.

COURANT NUMBER = u * dt/dx <= MAX COURANT NUMBER (THIS IS THE NUMBER THAT ASSURES STABILITY WILL RELY ONLY IN DISCRETIZATION SHCEMES)

We can use a method to calculate the dt based on the dx, to assure stability. For example we impose the courant number = 0.9 and calculate the dt. To assure that, the smaller our mesh is (more nx, less dx), the smaller dt must be.