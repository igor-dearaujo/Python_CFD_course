Notes about Step 1: 1D Linear Convection

1D linear convection equation

(I) du/dt + u . du/dx = 0 (is the non-linear 1d convection = Burgers)

(II) du/dt + c du/dx = 0 is the 1D linear convection equation

to get from I to II we linearize u with small perturbations.

u = U0 + u'(x, t)
U0 + u'(x, t) * d(U0 + u'(x, t))/dx
U0 + u'(x, t) * d(u'(x, t))/dx
(U0 + u'(x, t)) * d(u'(x, t))/dx
removing second order terms we get II

(II) representes a propagation of a wave with initial velocity c.

discretizing eq (II) with forward difference scheme for time:
du/dt = (u(t + delta t) - u(t))/delta t = u_n+1 - u_n

and backward diffrenece scheme for space derivative":
du/dx = u_i - u_i-1 / deltax

we get the equation: (n is a time step and i is a point in space)

(u_n+1_i - u_n_i) / delta t + c * (u_n_i - u_n_i-1)/delta x = 0 (this for a specific point (xi, tn) (Upwind Scheme)

with a initial condition through all the space, we know all points i in time n, so the only unknown is u_n+1_i = u_n_i - c * dt/dx * (u_n_i - u_n_i-1)

domain 2 units of lenght wide
lenght = 2

u = np.ones(nx)
x = np.linspace(0, lenght, nx)
plot(u, x) to see initial conditions

un is temporary array to store data from the last solution to get the next and store in u

than we have 2 loops. 1 loop iterate in time and the other in space.

for n in range_number_of_timesteps:
	un = u.copy() #get values of the current time step to calculate the next time step

	for i in range_xs:
		solve the discrete equations to find all the new u in the next timestep

the wave is moving to the right but it is losing its shape due do diffusion. The exact solution should stay as a hat, but we are losing shape due to numerical erros introduced.

Study of erros of truncation based on Taylor series and manipulation
