# Unit 9: Boundary Value Problems

## Subtopics

1. **Initial Value Problems vs. Boundary Value Problems**
   - What makes a BVP different from an IVP?
   - Physical motivation: steady-state temperature, beams, etc.
   - Why BVPs are harder to solve numerically

2. **The Shooting Method**
   - Turning a BVP into an IVP
   - Guessing the missing initial condition
   - Using root-finding to adjust the guess
   - Strengths and limitations

3. **Finite Difference Method for BVPs**
   - Discretizing the domain into a grid
   - Replacing derivatives with finite differences
   - Setting up the resulting linear system
   - Solving the system: tridiagonal matrices

4. **Convergence and Accuracy**
   - How the solution improves as we refine the grid
   - Truncation error in finite differences for BVPs
   - Checking your solution

5. **Nonlinear Boundary Value Problems (Brief Introduction)**
   - What changes when the ODE is nonlinear
   - Iteration (Newton's method for systems, conceptual)
   - A simple example
