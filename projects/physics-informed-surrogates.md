# Physics-informed surrogates with calibrated error bounds

**Jun 2026 to Aug 2026 · independent research · sole-authored preprint**

[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.21788995-blue?style=flat-square)](https://doi.org/10.5281/zenodo.21788995)
[![Code](https://img.shields.io/badge/code-scramjet--pinn--surrogate-181717?style=flat-square&logo=github)](https://github.com/hassaanshahid97-cyber/scramjet-pinn-surrogate)

## The question

A neural surrogate is only usable, rather than merely demonstrable, if two questions are answered.
How much of the reported accuracy survives a change of random seed, and how large an error allowance
does a decision rule need in order to stay safe. Both are usually left unanswered in the literature.

## What was done

| Step | Method |
|---|---|
| Problem | Parametric transient conjugate heat transfer, nonlinear, posed as the reference for a regeneratively cooled structure |
| Forward model | Finite volume PDE solver written from scratch |
| Verification, route 1 | Exact nonlinear steady solution obtained by Kirchhoff transform |
| Verification, route 2 | Method of manufactured solutions, observed order 2.00 in space and 0.95 in time |
| Surrogates | Four configurations trained in JAX at matched architecture and optimiser budget, three seeds each |
| Design | Non-dimensionalised residuals and hard-constrained initial conditions, so no loss weight needed tuning |
| Analysis | Mean effect of the physics residual separated from its effect on run-to-run variance |
| Safety | Surrogate used as a hard constraint inside a scheduler, then a split-conformal allowance applied |

## Results

- The physics residual cut the seed-to-seed standard deviation of field error by a **factor of 46**
  across twelve replicated runs. Most of its value was in variance, not in the mean.
- An accurate surrogate was shown **not** to be a safe one. Used directly as a hard constraint, the
  scheduler violated the limit more often than nominal.
- A **split-conformal** error allowance restored the nominal violation rate, measured in closed loop
  rather than assumed.
- **104 of 104** quantitative claims in the manuscript are re-checked against the stored results by
  an audit script shipped with the code.
- The full study reproduces in **under two core-hours**.

## Why it matters

This is the loop that any physics-informed surrogate needs before it is allowed near a decision:
a forward model you have verified two ways, a surrogate whose variability you have measured rather
than hoped about, and a bound whose coverage you have checked in closed loop.

## Stack

JAX and automatic differentiation, NumPy, SciPy, LaTeX. Code, data, figures and the audit script are
released under the MIT licence; the manuscript under CC BY 4.0.
