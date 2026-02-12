# Numerical Analysis Bootcamp — Undergraduate Level
## Project State

**Last updated:** 2026-02-12

---

## Project Overview

A "theoretical minimum" style Numerical Analysis Bootcamp at the undergraduate level. The bootcamp is organized as 10 Units (like chapters in a textbook), progressing from the very basics of numerical computing all the way to partial differential equations.

### Design Principles
- **Breadth over depth** — cover the essential landscape, not every detail
- **Beginner-friendly** — conceptual explanations first, minimal heavy math
- **Emphasize understanding** — detailed prose, worked examples, intuition before formulas
- **LaTeX documents** — each unit is a standalone `main.tex` with professional formatting

### Document Style
Each `main.tex` follows a consistent template:
- **Preamble:** `article` class, 12pt, a4paper, with `amsmath`, `tcolorbox`, `booktabs`, `fancyhdr`, `titlesec`, `hyperref`
- **Color scheme:** `primaryblue` (0,71,171), `accentred` (180,40,40), `darkgreen` (0,120,60)
- **Custom tcolorbox environments:** `keyconcept` (blue), `example` (green), `warning` (red), `takeaway` (yellow/orange)
- **Title page** with unit number, title, and short description
- **Table of contents** after title page
- **6 sections** per unit (each on its own page via `\newpage`)
- **Unit Summary** section at the end (unnumbered, added to TOC)
- **Header:** "Numerical Analysis Bootcamp" (left), "Unit N: Title" (right)
- **Footer:** page number centered

---

## Unit Structure (10 Units)

| # | Folder | Topic | Status |
|---|--------|-------|--------|
| 01 | `01-Foundations-of-Numerical-Computing/` | Errors, floating-point, stability, conditioning, Big-O, convergence | **DONE** |
| 02 | `02-Root-Finding/` | Bisection, fixed-point, Newton-Raphson, secant method | **DONE** |
| 03 | `03-Systems-of-Linear-Equations/` | Gaussian elimination, pivoting, LU, condition number, Jacobi/Gauss-Seidel | **DONE** |
| 04 | `04-Interpolation/` | Lagrange, Newton divided differences, error, Runge's phenomenon, splines | **DONE** |
| 05 | `05-Curve-Fitting-and-Least-Squares/` | Least squares, linear/polynomial regression, normal equations | **DONE** |
| 06 | `06-Numerical-Differentiation/` | Finite differences, step size, Richardson extrapolation | **DONE** |
| 07 | `07-Numerical-Integration/` | Trapezoidal, Simpson, Romberg, Gaussian quadrature | **DONE** |
| 08 | `08-Ordinary-Differential-Equations/` | Euler, Runge-Kutta, systems of ODEs, stability | **TODO** |
| 09 | `09-Boundary-Value-Problems/` | Shooting method, finite differences for BVPs | **TODO** |
| 10 | `10-Partial-Differential-Equations/` | Heat, wave, Laplace equations, finite differences in 2D | **TODO** |

---

## What Each Folder Contains

Every unit folder has:
- `subtopics.md` — outline of the 5–6 subtopics for that unit (created for ALL 10 units)
- `main.tex` — full LaTeX document with all content (created for units 01–07 so far)

---

## Completed Units — Summary of Content

### Unit 1: Foundations of Numerical Computing (~717 lines)
1. What Is Numerical Analysis? — exact vs. approximate, role of the computer
2. Number Representation & Floating-Point — binary, IEEE 754, machine epsilon, rounding
3. Sources of Error — truncation vs. round-off, absolute/relative error, significant digits
4. Error Propagation — arithmetic error growth, catastrophic cancellation
5. Stability and Conditioning — well/ill-conditioned problems, stable/unstable algorithms, condition number
6. Big-O Notation and Convergence — order of approximation, linear vs. quadratic convergence

### Unit 2: Root Finding (~736 lines)
1. The Root-Finding Problem — what roots are, graphical intuition, Abel-Ruffini theorem
2. The Bisection Method — IVT, interval halving, guaranteed linear convergence
3. Fixed-Point Iteration — x = g(x), cobweb diagrams, contraction mapping
4. Newton's Method — tangent line derivation, quadratic convergence, failure modes
5. The Secant Method — derivative-free, golden ratio convergence order
6. Comparison & Practical Considerations — speed vs. reliability, stopping criteria, hybrids

### Unit 3: Systems of Linear Equations (~825 lines)
1. Why Linear Systems Matter — ubiquity, matrix form Ax = b
2. Gaussian Elimination — forward elimination, back substitution, full 3×3 example
3. Pivoting Strategies — zero/small pivots, partial pivoting, 4-digit arithmetic disaster example
4. LU Decomposition — A = LU, factor once solve many, cost analysis
5. Measuring Error — vector/matrix norms, condition number, digit-loss rule
6. Iterative Methods — Jacobi, Gauss-Seidel, diagonal dominance, direct vs. iterative

### Unit 4: Interpolation (~733 lines)
1. What Is Interpolation? — interpolation vs. approximation vs. fitting, why polynomials
2. Lagrange Interpolation — basis polynomials, explicit formula, worked example
3. Newton's Divided Differences — recursive table, Newton form, adding points efficiently
4. Interpolation Error — error formula, worked bound, Runge's phenomenon
5. Spline Interpolation — piecewise polynomials, cubic splines, boundary conditions
6. Choosing a Strategy — polynomials vs. splines, node spacing, decision guide

### Unit 5: Curve Fitting and Least Squares (~750 lines)
1. The Curve Fitting Problem — interpolation vs. fitting, noisy data, overdetermined systems
2. Least Squares: The Core Idea — residuals, sum of squared residuals, why squared, projection geometry
3. Linear Least Squares — fitting a line, normal equations derivation, full worked example with residuals, general form A^T A a = A^T y
4. Polynomial Least Squares — Vandermonde matrix, quadratic fit example, overfitting vs. underfitting, degree selection guidelines
5. Linearizable Models — exponential fit (y=ae^{bx}), power-law fit (y=ax^b), logarithmic fit, bacteria growth and Kleiber's law examples, transformation summary table
6. Goodness of Fit — residual analysis (patterns, what to look for), R^2 derivation and interpretation, full R^2 worked example, when R^2 misleads, assessment checklist

### Unit 6: Numerical Differentiation (~720 lines)
1. Why Approximate Derivatives? — when exact derivatives are unavailable, connection to earlier units, building blocks for DEs
2. Finite Difference Formulas — Taylor series derivations, forward/backward/central differences, comparison table, worked example (e^x, 60x accuracy gain from central)
3. Accuracy and Step Size — truncation vs. round-off tension, optimal h derivation (sqrt(eps) for forward, eps^{1/3} for central), step-size sweep table showing sweet spot and degradation
4. Higher-Order Derivatives — second derivative 3-point stencil, h^2 denominator sensitivity, stencil table, five-point fourth-order formula
5. Richardson Extrapolation — cancelling leading error term, general formula, central difference example (500x improvement), connection to Romberg integration
6. Pitfalls and Practical Tips — noise amplification (1/h factor), differentiation is ill-conditioned vs. integration is well-conditioned, optimal h summary table, practical checklist

### Unit 7: Numerical Integration (~780 lines)
1. Why Numerical Integration? — integrals without antiderivatives, data/black-box integrands, well-conditioned contrast with differentiation
2. The Trapezoidal Rule — geometric idea (trapezoids), composite formula with weight pattern, worked example on e^{-x^2}, O(h^2) error
3. Simpson's Rule — parabolic approximation, 1-4-1 weights, composite formula, same data gives 100x better accuracy, O(h^4) error, bonus order from symmetry, even-n requirement
4. Comparing Quadrature Rules — degree of exactness table (midpoint through Boole), convergence comparison table (trapezoidal vs Simpson at n=2..64), midpoint rule as alternative
5. Romberg Integration — trapezoidal + Richardson extrapolation, even-powers-only error expansion, Romberg table walkthrough (O(h^2) to O(h^8)), built-in error estimates, efficiency via reuse
6. Gaussian Quadrature — optimal node+weight selection, degree of exactness 2n-1, Legendre polynomials, 1/2/3-point node tables, interval mapping, two worked examples (100x better than trapezoidal), when to use Gauss vs equally-spaced

---

## Next Step

**Unit 8: Ordinary Differential Equations** — awaiting user's "go ahead" to begin writing `main.tex`.

Subtopics (from `subtopics.md`):
1. The Initial Value Problem
2. Euler's Method
3. Improved and Modified Euler Methods
4. Runge-Kutta Methods
5. Systems of ODEs and Higher-Order Equations
6. Step Size and Stability

---

## Workflow

The user reviews each unit, then says "go ahead with the next section" to proceed. Units are written one at a time, sequentially.
