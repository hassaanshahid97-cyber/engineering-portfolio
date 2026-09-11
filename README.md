<div align="center">

# Engineering Portfolio

**Hassaan Shahid** · M.Sc. Aeronautical Engineering, Linköping University · Linköping, Sweden

Scientific machine learning · CFD and aerodynamics · aircraft conceptual design · flight systems and UAV test

[![Site](https://img.shields.io/badge/site-hassaanshahid97--cyber.github.io-0b5394?style=flat-square)](https://hassaanshahid97-cyber.github.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-hassaan--shahid-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hassaan-shahid-b1b285280)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--7403--8933-a6ce39?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0009-0003-7403-8933)
[![Licence](https://img.shields.io/badge/text%20%26%20figures-CC%20BY%204.0-lightgrey?style=flat-square)](LICENSE)

</div>

---

This repository is the index to my engineering work: what the problem was, what method was used,
what came out of it, and where the code or report lives. Projects with their own codebase link to a
dedicated repository. Projects whose deliverable was a report, a rig or an aircraft are documented
here with methods, numbers and figures.

---

## Index

### Scientific machine learning and numerical methods

| Project | Year | Summary | Detail |
|---|---|---|---|
| Physics-informed surrogates with calibrated error bounds | 2026 | Sole-authored preprint. Verified conjugate heat transfer solver, JAX surrogates, seed-replicated ablation, split-conformal safety bound. Physics residual cut seed-to-seed error variance by a factor of 46. | [page](projects/physics-informed-surrogates.md) · [repo](https://github.com/hassaanshahid97-cyber/scramjet-pinn-surrogate) · [DOI](https://doi.org/10.5281/zenodo.21788995) |
| Micro gas turbine design and performance code | 2024-25 | B.Sc. degree project, nominated Best Final Year Project. Generic C++ and NPSS tool for UAV turbojet design and mission performance, benchmarked on the AMT Olympus HP 230N. | [page](projects/uav-gas-turbine-code.md) · [repo](https://github.com/hassaanshahid97-cyber/uav-gas-turbine-performance-tool) · [DOI](https://doi.org/10.5281/zenodo.21805835) |

### CFD and aerodynamics

| Project | Year | Summary | Detail |
|---|---|---|---|
| Vehicle aerodynamics and rear spoiler design, RANS | 2026 | Turbulence model comparison at Re = 588,000 on a 3.2M+ element near-wall mesh. Spoiler bought downforce for a 5.7 per cent drag penalty. | [page](projects/vehicle-aero-rans-spoiler.md) |
| Shock structure in a convergent-divergent nozzle | 2023 | ANSYS Fluent study of oblique and normal shock interaction in internal compressible flow. Reviewed and approved by fluid dynamics faculty. | [page](projects/cd-nozzle-shock-analysis.md) |

### Aircraft conceptual design

| Project | Year | Summary | Detail |
|---|---|---|---|
| SKYLIGHT new midsize aircraft | 2026 | Sizing, drag polars, weights and FAR Part 25 envelopes for a 252-passenger airliner at Mach 0.77 and 212,957 kg MTOW. | [page](projects/skylight-midsize-airliner.md) |
| Heavy-lift electric UAV, SAE Brasil AeroDesign | 2026 | Constraint optimisation over thrust to weight and wing loading. Static margin held positive through mid-air release of a 1.0 kg glider. | [page](projects/sae-heavy-lift-uav.md) |
| EH-5963 wide-body design study | 2023-24 | Full conceptual design cycle for a 530-passenger Mach 0.86 aircraft using Raymer's RDS, Datcom and CATIA V5. | [page](projects/eh-5963-widebody.md) |
| Aero vehicle performance study, Boeing C-17 | 2023-24 | Performance across steady, accelerated, turning and climbing flight, take-off and landing. Graded 90 of 100. | [page](projects/c17-performance-study.md) |

### Design automation

| Project | Year | Summary | Detail |
|---|---|---|---|
| Parametric UAV fuselage and landing gear configurator | 2026 | VB.NET GUI driving the CATIA V5 API through an eight-stage PowerCopy workflow that builds internal structure from payload inputs. | [page](projects/parametric-uav-configurator.md) · [repo](https://github.com/hassaanshahid97-cyber/catia-v5-fuselage-configurator) |

### Flight systems, controls and test hardware

| Project | Year | Summary | Detail |
|---|---|---|---|
| Hardware-in-the-loop and Iron Bird framework | 2024 | Pixhawk 6X and ArduPlane coupled to X-Plane over MAVLink, on a rig with digital servos and rotary encoders. Stability derivatives validated under gust. | [page](projects/hil-iron-bird.md) |
| Twin Rotor Aerodynamical System control rig | 2022-23 | Helicopter-like laboratory plant: high-order, nonlinear, strongly cross-coupled, instrumented for system identification and control. | [page](projects/twin-rotor-aerodynamical-system.md) |
| Ultrasonic occupant counter | 2024 | Real-time bidirectional counter on an Arduino UNO with paired sensors and nested logic for stationary objects and simultaneous movement. | [page](projects/ultrasonic-occupant-counter.md) |

### Competition and built aircraft

| Project | Year | Summary | Detail |
|---|---|---|---|
| Stellar-X surveillance UAV | 2024-25 | Electric surveillance UAV, 5.0 kg MTOW, 1.69 m span, 26.5 m/s cruise, 50 min endurance. CAD, aerostructural simulation and flight test. | [page](projects/stellar-x-surveillance-uav.md) |
| Orbit-X composite UAV | 2024-25 | Carbon fibre high-wing monoplane, NACA 0015, 2.4 kg MTOW, 38 m STOL, servo-actuated payload drop, Level 1 automation on Pixhawk. | [page](projects/orbit-x-composite-uav.md) |
| KIRA-9 propeller-driven UAV | 2024 | Single-engine high-wing competition aircraft in carbon fibre and XPS foam with custom wing spars. Built and flown. | [page](projects/kira-9-uav.md) |

---

## Capability map

| Area | Tools and methods |
|---|---|
| Scientific machine learning | JAX with automatic differentiation, physics-informed neural networks, surrogate modelling, conformal prediction, seed-replicated experiment design |
| Numerical methods | Finite volume, finite element, method of manufactured solutions, grid and time-step convergence, Kirchhoff transform verification |
| CFD | ANSYS Fluent, RANS, k-epsilon and k-omega SST, near-wall meshing at y+ < 5, compressible and shock-dominated flow |
| Aircraft design | Constraint and sizing analysis, drag polars, weight build-up, FAR Part 25 envelopes, Raymer RDS, Datcom, stability and control |
| Propulsion | Brayton cycle modelling, NPSS, compressor and turbine maps, mission performance simulation |
| CAD and automation | SOLIDWORKS, CATIA V5 and its API, 3DEXPERIENCE, VB.NET automation, PowerCopy workflows |
| Flight systems and test | Pixhawk 6X, ArduPlane, MAVLink, X-Plane, NVIDIA Jetson, hardware- and software-in-the-loop, actuator latency measurement, flight test |
| Manufacturing | Carbon fibre composites, XPS foam, additive manufacturing, UAV build and maintenance |
| Languages | Python (NumPy, SciPy, JAX), C++, MATLAB, Simulink, VB.NET, LaTeX, Git |

---

## Competitions and credentials

- Winner, National Design-Build-Fly Competition, 2023 and 2024
- Runner-up, UCP Taakra AeroDesign Competition, 2023
- Nominated, Best Final Year Project 2025, Institute of Space Technology
- EASA UAS A1/A3 Open Subcategory remote pilot licence, valid to 2031
- Certified Engineer, Aerospace, Sveriges Ingenjörer, SeQF level 6
- Certified SOLIDWORKS Associate: Design (CSWA), xDesign, Additive Manufacturing and Sustainability
- Registered aeronautical engineer, Pakistan Engineering Council
- Member, Royal Aeronautical Society and AIAA (young professional)

<div align="center">
<img src="images/award_ndbfc18.jpg" width="330" alt="National Design-Build-Fly Competition"> <img src="images/award_ndbfc17.jpg" width="200" alt="National Design-Build-Fly Competition">
</div>

---

## Contact

Linköping, Sweden · [hassaanshahid97@gmail.com](mailto:hassaanshahid97@gmail.com) ·
[LinkedIn](https://www.linkedin.com/in/hassaan-shahid-b1b285280) ·
[GitHub](https://github.com/hassaanshahid97-cyber) ·
[ORCID 0009-0003-7403-8933](https://orcid.org/0009-0003-7403-8933)

Open to master thesis projects from January 2027, research internships and graduate roles in
scientific machine learning, CFD, simulation and flight systems.

---

Text and figures in this repository are released under [CC BY 4.0](LICENSE). Code in the linked
project repositories is released under the MIT licence unless stated otherwise. Coursework figures
are my own work unless a source is cited on the project page.
