# Vehicle aerodynamics and rear spoiler design, RANS simulation

**Mar 2026 to Jun 2026 · TMMV08 Computational Fluid Dynamics, Linköping University**

## Objective

Steady-state RANS investigation of external vehicle aerodynamics, and evaluation of what a
trailing-edge rear spoiler actually buys once the drag penalty is counted.

## Setup

| Item | Value |
|---|---|
| Reynolds number | 588,000 |
| Mesh | over 3.2 million elements, near-wall resolved at y+ < 5 |
| Turbulence models compared | standard k-epsilon and k-omega SST |
| Solver | ANSYS Fluent, steady RANS |
| Convergence | grid and time-step convergence studies, residual and force monitors |

## Results

- The trailing-edge spoiler converted a near-neutral lift condition into genuine downforce,
  **C_L = -0.094**, for a **5.7 per cent** drag penalty.
- Turbulence model choice changed separation behaviour at the rear of the body, which is where the
  spoiler does its work, so the comparison was run before any geometry conclusion was drawn.

## Skills demonstrated

Near-wall meshing strategy, turbulence model selection and justification, convergence discipline,
and reporting an aerodynamic gain together with its cost rather than on its own.
