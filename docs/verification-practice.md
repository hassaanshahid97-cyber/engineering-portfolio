# How I verify

[Back to portfolio](../README.md)

A solver is not correct because it runs, a surrogate is not accurate because one seed says so, and a
design is not better because one number improved. This page collects the verification practice that
runs through the projects in this portfolio, with the specific instances that back it.

---

## 1. Verify the tool before trusting the answer

Two independent routes, because one route can be wrong in a way that agrees with itself.

<img src="../figures/surrogates/fig_verification.png" width="560" alt="Observed order of accuracy from the method of manufactured solutions">

**Route one, exact solution.** For the nonlinear steady conjugate heat transfer problem, a Kirchhoff
transform gives an exact solution against which the solver can be compared directly. An exact
solution catches errors of formulation that a convergence study cannot.

**Route two, manufactured solutions.** A manufactured solution is substituted into the governing
equation, the residual becomes a source term, and the solver must then recover the manufactured
field at the theoretical order of accuracy. Observed here:

| Quantity | Observed order | Expected |
|---|---|---|
| Spatial | **2.00** | 2 |
| Temporal | **0.95** | 1 |

An observed order that matches theory is strong evidence that the discretisation, the boundary
conditions and the time integration are all implemented as intended. A code that produces plausible
pictures but the wrong order is a code with a bug.

**In CFD, the equivalent is the model comparison and the mesh study.** In the rear spoiler study the
k-epsilon and k-omega SST results were compared at Re = 588,000 on a 3.2 million element mesh
resolved to y+ < 5, before any conclusion was drawn about the spoiler. Turbulence model choice
changes separation behaviour at the rear of a bluff body, which is precisely where the spoiler does
its work, so taking the first model's answer would have been a coin flip presented as a result.

[Preprint case study](../projects/physics-informed-surrogates.md) ·
[RANS case study](../projects/vehicle-aero-rans-spoiler.md)

---

## 2. Report the variance, not the best run

<img src="../figures/surrogates/fig_seeds.png" width="560" alt="Seed-to-seed variability of field error across replicated runs">

Neural network training is stochastic. A single reported error is a sample from a distribution, and
the literature convention of reporting the run that worked hides the spread.

Four surrogate configurations were trained at **matched architecture and optimiser budget**, three
seeds each, twelve runs in total. That design separates two different things that are usually
conflated:

- the **mean effect** of adding a physics residual to the loss
- its effect on **run-to-run variance**

The headline result lives in the second one: the physics residual cut the seed-to-seed standard
deviation of field error from 12.42 K to 0.27 K, a **factor of about 45**. At a single seed that finding is invisible, and the
reported benefit would have been mostly luck.

Matched budget matters as much as replication. Comparing a physics-informed model trained longer
against a baseline trained less is not a comparison of the physics term.

---

## 3. Calibrate the claim, then test the calibration in closed loop

<img src="../figures/surrogates/fig_allowance.png" width="560" alt="Split-conformal allowance and the resulting violation rate">

An error metric on a held-out set is not a safety statement. The question a decision rule actually
asks is: how large an allowance do I need so that I violate the limit no more often than I promised?

The surrogate was placed inside a scheduler as a hard constraint. Used directly, the accurate
surrogate broke the limit on **14.4 per cent** of manoeuvres against a nominal 5 per cent. A **split-conformal** allowance restored it, to 5.8 per cent. The key
point of method is that the violation rate was **measured in the closed loop**, with the surrogate
driving the decision, not estimated from open-loop error statistics and assumed to carry over.

The conclusion is quotable and uncomfortable, which is why it is worth reporting: an accurate
surrogate is not automatically a safe one.

---

## 4. Make the result re-checkable by someone who does not trust you

Reproducibility is not a badge, it is the part of the work that survives you leaving the project.

| Practice | Instance |
|---|---|
| Full study reproduces from a clean checkout | **under two core-hours** |
| Every quantitative claim in the manuscript re-checked against stored results by a script | **104 of 104** |
| Code, data, figures and licence published together | MIT for code, CC BY 4.0 for the manuscript |
| Seeds, configurations and budgets recorded rather than described | in the repository |

The audit script matters more than the wall clock. It reads the manuscript's numbers and compares
them against the stored result files, so a figure regenerated after a code change cannot silently
disagree with the text. Writing it took an afternoon and caught the class of error that is otherwise
found by a reviewer.

[Code and audit script](https://github.com/hassaanshahid97-cyber/scramjet-pinn-surrogate)

---

## 5. State the cost with the gain

A design result with only the benefit in it is an advertisement.

| Change | Gain | Cost |
|---|---|---|
| Trailing-edge rear spoiler | near-neutral lift became genuine downforce, C_L = **-0.094** | **5.7 per cent** drag penalty |
| NACA 2415 wing section on the heavy-lift UAV | zero-lift pitching moment cut **53 per cent** | section and structural consequences carried through sizing |
| Physics residual in the surrogate loss | variance cut by a factor of about **45** | extra terms to evaluate, and the residual must be non-dimensionalised or it dominates |

---

## 6. Reconcile model and hardware instead of tuning until they agree

On the Iron Bird rig, actuator latency and response rate were **measured** on the physical servos and
compared against the MATLAB and Simulink model of the same actuator. The useful output of a rig is
not a model that matches, it is knowing by how much and in which direction it does not, and whether
that gap matters for the control law.

Stability derivatives, including C_L alpha and C_m q, were validated under gust conditions in that
same loop rather than taken from a handbook estimate and trusted.

[Iron Bird case study](../projects/hil-iron-bird.md)

---

## The checklist I actually use

1. Does the solver reproduce an exact solution, and does it hit the theoretical order on a
   manufactured one?
2. Is the mesh or time step converged, and was that shown rather than asserted?
3. If the method is stochastic, how many seeds, and what is the spread?
4. Is the comparison budget-matched, so the difference is the thing I changed?
5. Does the uncertainty statement hold in the loop where the number is actually used?
6. Can someone re-run this from a clean checkout, and does a script confirm the text matches the
   results?
7. Is the cost of the improvement stated next to the improvement?

---

[Back to portfolio](../README.md)
