# Laplace's equation in 2D

The laplace equation are basically a equilibrium diffusion solution (so no time derivative), we calculate the equilibrium state of a body based on boundary conditions.

$$\frac{\partial^2 p}{\partial x^2} + \frac{\partial^2 p}{\partial y^2} = 0$$

We discretize the 2 second order derivatives with central-difference schemes. Than our idea, instead of solving for time t, we solve for $p^n_{i, j}$. In theory if we make the number of iterations tend to infinite, we get the final solution, to do so we evaluate convergence of the solution.

OBS: using 2 central-difference schemes (in x and y) is know as using five-point difference operator

We consider boundary conditions in our solutions equations