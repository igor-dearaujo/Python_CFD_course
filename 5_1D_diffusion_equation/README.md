NOTES ON STEP : 1D Diffusion equation

Basically there is no convection so the term u * du/dx is zero. In the RHS there is the diffusive term that comes from:
div(stresses) = nu * div(grad(u))

$$\frac{\partial u}{\partial t}= \nu \frac{\partial^2 u}{\partial x^2}$$

It appeared a second order derivative that needs to be discretized. To do that we use the Taylor series expansio of $$u_(i+1)$$ and $$u_(i-1)$$ arround u_i and sum them both. We get rid of odd index terms and get the folowing equation:

$u_{i+1} + u_{i-1} = 2u_i+\Delta x^2 \frac{\partial ^2 u}{\partial x^2}\bigg|_i + O(\Delta x^4)$

After that the divide all by $$\Delta x^2$$ and get the solution for the second order derivative in point i.

$$\frac{\partial ^2 u}{\partial x^2}=\frac{u_{i+1}-2u_{i}+u_{i-1}}{\Delta x^2} + O(\Delta x^2)$$

After that we can rewrite the 1D Diffusion equation in its discrete form (using forward difference shceme for the time):
Once we have a initial condition, the only unkwown is the term $$u_{i} ^{n+1}$$

After that to solve the problem numerically we follow the same steps:

- Definition of geometrical Domain
- Definition of discretized domain (array of nx items) > dx elements
- Definition of discretized time steps
- Initialize velocity vector with initial conditions
- Iterations loop in time array
    - save a copy of the previous solution
    - Iterations loop in space array
        - Calculate new u vector based on previous vector and space discretization

