# Unit 8: Ordinary Differential Equations (Initial Value Problems)

## Subtopics

1. **The Initial Value Problem**
   - What is an ODE?
   - Initial conditions and the IVP
   - Why most ODEs can't be solved by hand
   - The idea of stepping forward in time

2. **Euler's Method**
   - The simplest ODE solver
   - Derivation from the tangent line
   - Step-by-step algorithm
   - Local and global truncation error

3. **Improved and Modified Euler Methods**
   - The idea of predictor-corrector
   - Heun's method (improved Euler)
   - Why using a midpoint or correction helps

4. **Runge-Kutta Methods**
   - The classical 4th-order Runge-Kutta (RK4)
   - Why RK4 is the workhorse of ODE solving
   - Step-by-step algorithm
   - Intuition for the weighted average of slopes

5. **Systems of ODEs and Higher-Order Equations**
   - Converting a higher-order ODE to a system of first-order ODEs
   - Applying Euler and RK4 to systems
   - Simple examples (e.g., harmonic oscillator)

6. **Step Size and Stability**
   - What happens when the step size is too large?
   - Stability regions (intuitive picture)
   - Adaptive step size control (brief overview)
   - Stiff equations: a first look
