# Shock structure in a convergent-divergent nozzle

**Compressible aerodynamics, Institute of Space Technology · September to November 2023**

<img src="../figures/misc/proj_nozzle.jpg" width="360" alt="Shock structure in the convergent divergent nozzle">

| | |
|---|---|
| **Context** | Computational investigation of internal compressible flow in an indigenously designed nozzle |
| **Tools** | ANSYS Fluent, density-based compressible solver |
| **Review** | Method and results reviewed and approved by fluid dynamics faculty |

## 1. Objective

Study the formation and interaction of **oblique and normal shocks** inside a convergent-divergent
nozzle at off-design pressure ratio, and their effect on the flow state from inlet through throat to
exit.

## 2. Method

- Density-based compressible solver in ANSYS Fluent, appropriate to a shock-dominated internal flow
- Shock formation and propagation traced through the divergent section
- Flow parameters analysed region by region: inlet, throat, exit, including total pressure loss across
  the shock system
- Results reviewed and approved by fluid dynamics faculty before submission

## 3. Outcome

A clear picture of how the oblique and normal shock system sets the exit condition, and of how far the
design departs from ideal isentropic expansion when it is operated away from its design pressure
ratio.

## 4. What I would do differently

- **A mesh convergence study in the shock region.** Shock position is grid sensitive, and shock
  position is the whole result.
- **Sweep the pressure ratio.** One off-design condition shows the shock system exists. A sweep would
  show where it moves and where the nozzle becomes unusable, which is the design-relevant answer.

## 5. Relevance

Compressible and shock-dominated flow, and the habit of tying a computed field back to the
one-dimensional theory that should predict it. Foundation for gas turbine and high-speed propulsion
work.

[Back to portfolio](../README.md)
