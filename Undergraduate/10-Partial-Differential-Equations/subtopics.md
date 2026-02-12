# Unit 10: Partial Differential Equations

## Subtopics

1. **Introduction to PDEs**
   - What is a PDE?
   - The three classic types: elliptic, parabolic, hyperbolic
   - Physical examples: heat flow, wave propagation, steady-state problems
   - Boundary and initial conditions for PDEs

2. **Finite Differences in Two Dimensions**
   - Extending finite differences to 2D grids
   - Discretizing partial derivatives
   - The computational grid

3. **The Heat Equation (Parabolic PDEs)**
   - Physical setup: temperature diffusion
   - Explicit method (forward in time, centered in space)
   - Stability constraint (CFL condition, intuitive)
   - Implicit method (backward Euler): why it helps with stability

4. **The Wave Equation (Hyperbolic PDEs)**
   - Physical setup: vibrating string
   - Explicit finite difference scheme
   - Stability and the CFL condition
   - Visualizing the solution over time

5. **Laplace's and Poisson's Equations (Elliptic PDEs)**
   - Steady-state problems
   - The five-point stencil
   - Setting up and solving the linear system
   - Iterative solution methods (Jacobi, Gauss-Seidel on grids)

6. **Practical Considerations and Looking Ahead**
   - Mesh refinement and accuracy
   - Brief mention of finite element and finite volume methods
   - What comes next: the Graduate-level bootcamp
