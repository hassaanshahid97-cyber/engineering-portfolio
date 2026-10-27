# Master thesis readiness, from January 2027

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
| **What I bring on day one** | A finished, sole-authored study of the same shape as a thesis: problem posed, solver written and verified, surrogate trained, results calibrated, manuscript under review. A second sole-authored paper in preparation |

---

## Four directions I am ready for

Each one states honestly what I have already done, and what I would have to learn in the first weeks.
No direction below claims readiness I cannot evidence.

---

### 1. Robust design margins and uncertainty quantification

**Examples:** turning uncertainty into design margins, probabilistic and sensitivity analysis,
robust design optimization, surrogate-assisted design under constraints.

**Why me.** Both of my papers are about this question. In Paper 1 a coolant scheduler that optimised
against a surrogate broke its stress limit in **14.4 per cent** of decisions, because the optimiser
seeks out the surrogate's optimistic errors; a split-conformal margin brought this to **5.8 per cent**
against a 5 per cent target, and a margin calibrated only near the constraint boundary failed at
13.2 per cent. In Paper 2 a calibrated margin held **0.952** coverage over 1000 Monte Carlo flights
under guidance feedback, and I measured how much each main uncertainty moved the outcome.

**What I would ramp up.** Industrial robustness tools such as optiSLang, and the geometric and
material scatter of manufactured components.

[Evidence: surrogates case study](../projects/physics-informed-surrogates.md) ·
[entry guidance](../projects/reentry-guidance.md)

---

### 2. Gas turbine performance, test data and model-based correction

**Examples:** performance calculation and correction, comparing thermodynamic models with test data,
mission and cycle studies, low-order compressor models.

**Why me.** My degree project was a C++ and NPSS design and performance code with compressor and
turbine maps, benchmarked against manufacturer test data for the AMT Olympus HP 230N, with a
second-by-second mission simulator built around it. At NaqCoDE I compared models with rig data in real
time and traced each mismatch to the model, the sensors or the data link. Coursework: Turbo Machinery,
Thermodynamics and Gas Turbine Engines.

**What I would ramp up.** Field performance test procedures (ASME PTC 22, ISO 2314) in practice,
industrial test databases, and FMU-based engine models.

[Evidence: gas turbine code](../projects/uav-gas-turbine-code.md) ·
[HIL rig](../projects/hil-iron-bird.md)

---

### 3. CFD and heat transfer

**Examples:** turbomachinery and cooling flows, conjugate heat transfer, CFD methodology and
validation, reduced-order and ML-assisted models.

**Why me.** Steady RANS at Re = 588,000 on a **3.2 million element** near-wall mesh at y+ < 5, with a
k-epsilon against k-omega SST comparison and convergence studies before any conclusion. A transient
conduction solver for a 1 mm Inconel 718 wall, verified against exact and manufactured solutions.
B.Sc. Heat Transfer, Thermodynamics, Fluid Mechanics and Compressible Aerodynamics, with heat transfer,
aerodynamics, propulsion and instrumentation labs.

**What I would ramp up.** CFX and Star-CCM+, IR thermography and PIV in a lab, and adjoint methods,
which I understand in principle and have not implemented.

[Evidence: RANS spoiler study](../projects/vehicle-aero-rans-spoiler.md) ·
[surrogates](../projects/physics-informed-surrogates.md)

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

- I have **not** used IR thermography, PIV or electromagnetic solvers, and have not taken part in an
  industrial field performance test.
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

Happy to send the full CV, transcripts, either paper, or a short call to talk through whether the
problem you have in mind is a fit.
