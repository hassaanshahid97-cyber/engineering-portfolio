# Micro gas turbine design and performance code

**Sep 2024 to Jul 2025 · B.Sc. degree project, Institute of Space Technology · nominated Best Final Year Project 2025**

[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.21805835-blue?style=flat-square)](https://doi.org/10.5281/zenodo.21805835)
[![Code](https://img.shields.io/badge/code-uav--gas--turbine--performance--tool-181717?style=flat-square&logo=github)](https://github.com/hassaanshahid97-cyber/uav-gas-turbine-performance-tool)

Supervisor: Dr M. Naeem (PhD, Cranfield). Co-author: Muhammad Bilal Sabir.

## The gap

Micro turbojets give tactical and surveillance UAVs the power-to-weight ratio and throttle response
they need, but the open literature lacks an accessible model that unifies thrust, RPM, specific fuel
consumption and aerodynamic drag for a validated engine under realistic mission conditions.

## What the tool does

- Estimates lift, drag and flight performance from wetted-area build-up, skin-friction coefficients
  and Oswald efficiency
- Computes thrust, TSFC, RPM and fuel flow across altitude, Mach number and throttle setting
- Simulates ground roll, transition, climb, cruise, payload drop and descent, phase by phase and
  second by second
- Animates the trajectory with live thrust, drag, rate of climb and fuel readouts
- Cross-checks against AMT Olympus HP 230N manufacturer test data and engine maps

## Benchmark engine

| Parameter | Value |
|---|---|
| Static thrust at sea level | 230 N |
| Maximum RPM | 108,500 rpm |
| Idle RPM | approx. 35,000 rpm |
| Compressor pressure ratio | approx. 3.8 |

## Stack

Self-contained C++ and NPSS tool with a MATLAB implementation, built to run offline so that
propulsion evaluation needs no external service. Modular architecture: atmospheric model, aerodynamic
vehicle design build-up, engine cycle, mission simulator.
