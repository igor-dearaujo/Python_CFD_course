# BURGER'S EQUATION IN 2D

Again, as in step 5, the burger's equation is a combination of non-linear convection + diffusion. We part from transport equation, apply non-linear convection and diffusion (ignore source terms) and then we discretize in time (forward) and space (backward) (careful because in space we have first order derivatives and second order derivatives). We then arrive in:

$$
\begin{split}
u_{i,j}^{n+1} = & u_{i,j}^n - \frac{\Delta t}{\Delta x} u_{i,j}^n (u_{i,j}^n - u_{i-1,j}^n)  - \frac{\Delta t}{\Delta y} v_{i,j}^n (u_{i,j}^n - u_{i,j-1}^n) \\
&+ \frac{\nu \Delta t}{\Delta x^2}(u_{i+1,j}^n-2u_{i,j}^n+u_{i-1,j}^n) + \frac{\nu \Delta t}{\Delta y^2} (u_{i,j+1}^n - 2u_{i,j}^n + u_{i,j-1}^n)
\end{split}
$$

$$
\begin{split}
v_{i,j}^{n+1} = & v_{i,j}^n - \frac{\Delta t}{\Delta x} u_{i,j}^n (v_{i,j}^n - v_{i-1,j}^n) - \frac{\Delta t}{\Delta y} v_{i,j}^n (v_{i,j}^n - v_{i,j-1}^n) \\
&+ \frac{\nu \Delta t}{\Delta x^2}(v_{i+1,j}^n-2v_{i,j}^n+v_{i-1,j}^n) + \frac{\nu \Delta t}{\Delta y^2} (v_{i,j+1}^n - 2v_{i,j}^n + v_{i,j-1}^n)
\end{split}
$$

For the solution we follow the same steps:
- Initialize space discretization mesh (nx, dx, ny, dy, X, Y)
- Initialize time discretization parameters (sigma, dt, soltime, etc)
- Initialize the vector velocity with initial conditions
- Sovler loop (un = u.copy())
- Plot solution in gif

