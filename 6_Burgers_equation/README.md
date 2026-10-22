STEP 5: Burgers equation 1D

The Burgers equation is a combination of non-linear convection + diffusion in 1D. We discretize the velocity using backwards scheme (or upwind) and time using forward difference. The second order derivative is calculated using centered scheme

We combine all this discretizations and isolate the next step term.

We will use different initial and boundary conditions (trouble to derivate things and etc: we introduce a new library: SymPy)

Use of sympy for simbolic manipulation of functions:
    - define symbols using sp.symbols()
    - define a function and derivate using diff
    - define a callable function using lambdify

After we defined a know u funciton with periodical boundary conditions (u(0) = u(2pi))
    We need to apply that in the solver iterations

    what we do
    it the space iterations we iterate from 1 to nx - 1. To solve the internals
    outside the loop we calculate u[-1], last terme and we make u[0] = u[-1]