STEP 5: Burgers equation 1D

The Burgers equation is a combination of non-linear convection + diffusion in 1D. We discretize the velocity using backwards scheme (or upwind) and time using forward difference. The second order derivative is calculated using centered scheme

We combine all this discretizations and isolate the next step term.

We will use different initial and boundary conditions (trouble to derivate things and etc: we introduce a new library: SymPy)

