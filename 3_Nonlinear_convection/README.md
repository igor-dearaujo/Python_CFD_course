MODULE 3

NON LINEAR 1D CONVECTION:
du/dt + u . du/dx = 0 (is the non-linear 1d convection = Burgers)

Same discretization as previous module (forward difference for time and backward difference for space)

(u_n+1_i - u_n_i) / delta t + u_n_i * (u_n_i - u_n_i-1)/delta x = 0 (this for a specific point (xi, tn) (Upwind Scheme)

defined CFL to correlate dx and dt > CFL = dt / dx * max(abs(u))

changing the CFL value has high influence in results stability (for values higher than 1) and makes the timestep too litle if too close to zero

Also with the Scheme utilized, negative initial conditions lead the solution to divergence. The backard difference scheme for the convection term is not effective when dealing with negative convection.

To solve this we introduce the Upwind Scheme that adjusts the discretization Direction based on the sign of convection coeficient
Basically we introduce a function that returns (1, 0) and (0, 1) depending on the sign of a value. Evaluating in the velocity sign in each node, we apply the results to a east and a West functions constants and ue-uw returns the backward difference scheme if u > 0 and forward difference scheme if u < 0.

It is also possible to analyse using if/else condition (evaluate difference in time consuming using python capabilities)

Using Numpy arrays manipulation: 
    20 iterations = 0.022471766999842657 s
    100 iterations = 0.07523711599969829 s
    1000 iteartions = 0.717492226000104 s


Using if/else conditions:
    20 iterations = 0.011163707999912731 s
    100 iterations = 0.02473336200000631 s
    1000 iterations = 0.3136802170001829 s