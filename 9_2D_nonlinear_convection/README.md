2D NON LINEAR CONVECTION

- Similar to non linear, but c is replaced by u
- to get to the 2D convection equation:
    - wrtie the transport equation for $\underline{u}$, and ignore diffusion and source terms
    - $$ \frac{\dif u}{\dif t} + (\underline{u} \cdot \underline{\nabla})\underline{u} $$
    - OBSERVATION: the term $$\nabla \cdot (\underline{u} \otimes \underline{u})$$ can be separated in two (similar to product rule)
    - but take care with the order of application!!!
    - then we use discretization and isolates the next step temporal term

    -same initial conditions
    -initialize the vectors and set initial conditions
    -loop (safe past state, write numpy arrays equations for better efficiency, apply boundary conditions)
    -plot