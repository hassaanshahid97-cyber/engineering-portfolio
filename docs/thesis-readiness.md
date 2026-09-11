# Master thesis readiness, January to June 2027

[Back to portfolio](../README.md)

---

## The practical facts first

| | |
|---|---|
| **Scope** | Master thesis, 30 hp, Linköping University, M.Sc. Aeronautical Engineering |
| **Period** | January 2027 to June 2027, full time, 20 weeks |
| **Location** | Based in Linköping. Able to work on site anywhere in Sweden, and open to Scandinavia and Denmark |
| **Language** | English fluent, IELTS 7.5, CEFR C1. Swedish A2 and improving, studying SFI at Linköping kommun. Comfortable in a Swedish-speaking workplace as long as technical work is in English |
| **Coursework finished before the thesis starts** | Machine Learning for Mechanical Engineering, Computational Fluid Dynamics, Gas Turbine Engines, Aircraft Systems Engineering Project, Model-based System-of-Systems Engineering, Prototype Realization |
| **Security and confidentiality** | Willing to work under NDA and to publish a redacted thesis where the host requires it |
| **What I bring on day one** | A finished, sole-authored study of the same shape as a thesis: problem posed, solver written and verified, surrogate trained, results calibrated, manuscript submitted |

---

## Four directions I am ready for

Each one states honestly what I have already done, and what I would have to learn in the first weeks.
No direction below claims readiness I cannot evidence.

---

### 1. Scientific machine learning for physics-informed inverse problems

**Examples:** synthetic aperture radar imaging, electromagnetic scattering, non-destructive
evaluation, any ill-posed reconstruction with a PDE forward model.

**Why me.** This is the loop I have already closed end to end, on a different physics:
a verified PDE forward model, a learned surrogate trained in JAX with automatic differentiation,
and a calibrated statement of how far the reconstruction can be trusted. Specifically:

- Non-dimensionalised residuals and hard-constrained initial conditions, so **no loss weight needed
  tuning**, which is the failure mode that sinks most physics-informed work
- **Twelve replicated runs** to separate a mean effect from a variance effect
- A **split-conformal** allowance validated in closed loop, not assumed
- Full study reproduces in **under two core-hours**

**What I would ramp up in the first three weeks.** Electromagnetic wave scattering formulations and
the SAR imaging chain, which I have read into but not yet worked with. Ill-posedness and
regularisation theory beyond what I applied in the conjugate heat transfer setting. GPU programming
for the forward solve: I have trained on GPU but have not written high-performance kernels.

**What a supervisor gets in 20 weeks.** A verified forward model, a surrogate with measured
seed-to-seed variance rather than a single reported number, and a bound whose coverage is checked
rather than claimed.

[Evidence: physics-informed surrogates case study](../projects/physics-informed-surrogates.md)

---

### 2. Surrogate modelling and uncertainty quantification for propulsion and thermal limits

**Examples:** real-time limit protection, digital twins of hot structures, life usage monitoring,
fast models inside a control loop.

**Why me.** The preprint is exactly this problem in miniature. The surrogate was placed inside a
scheduler as a hard constraint, and the interesting result is negative and useful: an accurate
surrogate was **not** a safe one until a calibrated allowance was added. I also have the propulsion
side: a Brayton cycle tool with compressor and turbine maps, benchmarked against manufacturer test
data for the AMT Olympus HP 230N, and a second-by-second mission simulator built around it.

**What I would ramp up.** Industrial life and damage models. Real-time and embedded deployment
constraints, where my experience is the Iron Bird rig rather than certified software.

**What a supervisor gets in 20 weeks.** A surrogate with a defensible error budget, and an honest
answer to "how wrong is this allowed to be before the limit protection stops protecting".

[Evidence: gas turbine code](../projects/uav-gas-turbine-code.md) ·
[surrogates](../projects/physics-informed-surrogates.md)

---

### 3. Machine learning applied to CFD

**Examples:** reduced order models for external aerodynamics, data-driven turbulence closure
augmentation, surrogate-assisted shape optimisation.

**Why me.** I have both halves and they rarely appear together in a student. On the CFD side:
steady RANS at Re = 588,000 on a **3.2 million element** near-wall mesh at y+ < 5, with a k-epsilon
against k-omega SST comparison run before any geometry conclusion was drawn, and grid and time-step
convergence studies. On the ML side, the preprint. I am taking Computational Fluid Dynamics and
Machine Learning for Mechanical Engineering in the year before the thesis.

**What I would ramp up.** Large training data pipelines from CFD, which is an engineering problem of
its own. Adjoint methods, which I understand in principle and have not implemented.

**What a supervisor gets in 20 weeks.** A model trained on data whose own numerical error is known,
because the convergence study came first.

[Evidence: RANS spoiler study](../projects/vehicle-aero-rans-spoiler.md)

---

### 4. Simulation, model validation and test for flight systems

**Examples:** hardware- and software-in-the-loop frameworks, model validation against rig or flight
data, autonomy validation before flight test.

**Why me.** I have built the rig. A Pixhawk 6X running ArduPlane closed onto the X-Plane physics
engine over MAVLink, on an Iron Bird with digital servos and rotary encoders, with measured actuator
latency reconciled against the MATLAB and Simulink model rather than assumed equal, and stability
derivatives validated under gust. I also hold an EASA UAS A1/A3 remote pilot licence and have flown
the aircraft I designed.

**What I would ramp up.** Certification-grade process, DO-178C style software assurance, and formal
requirements management, where my experience is student and startup practice rather than industrial.

**What a supervisor gets in 20 weeks.** Someone who will notice when the model and the hardware
disagree, and will chase the discrepancy rather than tune it away.

[Evidence: HIL Iron Bird case study](../projects/hil-iron-bird.md)

---

## What I am not claiming

Stated plainly, because a supervisor finding this out in week six is worse than reading it now.

- I have **not** worked with synthetic aperture radar data or electromagnetic solvers. I have read
  into the area and named it as a target, which is not the same thing.
- I have **not** written GPU kernels or run on an HPC cluster. My work reproduces on a laptop in two
  core-hours by design, which is a different skill from scaling up.
- My **C++** is working knowledge, used for the degree project tool. My production language is Python.
- I have **not** worked inside a certified aerospace software process.
- My finite element work is coursework level. My finite volume work is not.

Everything in the portfolio that I do claim is linked to code, a manuscript, a report or a flying
aircraft.

---

## How to reach me

[hassaanshahid97@gmail.com](mailto:hassaanshahid97@gmail.com) ·
[LinkedIn](https://www.linkedin.com/in/hassaan-shahid-b1b285280) ·
[hassaanshahid97-cyber.github.io](https://hassaanshahid97-cyber.github.io)

Happy to send the full CV, transcripts, the preprint, or a short call to talk through whether the
problem you have in mind is a fit.
