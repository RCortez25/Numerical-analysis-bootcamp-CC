# Unit 4: Interpolation

## Subtopics

1. **What Is Interpolation?**
   - The problem: passing a curve through known data points
   - Interpolation vs. approximation vs. curve fitting
   - When and why we interpolate

2. **Lagrange Interpolation**
   - Construction of the Lagrange basis polynomials
   - Building the interpolating polynomial
   - Worked examples
   - Uniqueness of the interpolating polynomial

3. **Newton's Divided Differences**
   - Divided difference tables
   - Newton's interpolating polynomial
   - Adding new data points efficiently
   - Connection to Lagrange form

4. **Interpolation Error**
   - How good is our polynomial?
   - The error formula (intuitive understanding)
   - Runge's phenomenon: why high-degree polynomials can misbehave

5. **Spline Interpolation**
   - The idea: piecewise polynomials instead of one global polynomial
   - Linear splines
   - Cubic splines: smoothness conditions
   - Why splines avoid Runge's phenomenon

6. **Choosing an Interpolation Strategy**
   - Polynomials vs. splines: trade-offs
   - Effect of data spacing
   - Practical guidelines
