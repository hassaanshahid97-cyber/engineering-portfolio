# Parametric UAV fuselage and landing gear configurator

**Mar 2026 to Jun 2026 · TMKT57 Product Modelling, Linköping University · team project**

[![Code](https://img.shields.io/badge/code-catia--v5--fuselage--configurator-181717?style=flat-square&logo=github)](https://github.com/hassaanshahid97-cyber/catia-v5-fuselage-configurator)

## The problem

Generating a new fuselage and landing gear configuration by hand in CAD is repetitive work that
scales badly. The aim was to remove the non-creative part of that loop so that the engineer spends
time on the decisions instead of the clicks.

## What was built

- A custom **VB.NET** GUI interfacing directly with the **CATIA V5 Interop API**
- An **eight-stage PowerCopy workflow** that generates bulkheads, frames, longerons and skin along
  the fuselage skeleton
- Dynamic computation of centre of gravity and landing gear X-stations from payload inputs
- Configuration save and load from a local database, so a library of standard layouts can be built up

## Inputs and outputs

| User inputs | Generated model |
|---|---|
| Fuselage length, cross-section, nose and tail style | Skeleton, bulkheads, frames, longerons, skin |
| Number of frames, spacing | Internal structure instantiated by PowerCopy |
| Payload mass and station, landing gear type and wheel arrangement | CG position, landing gear X-stations, gear geometry |

## Skills demonstrated

CAD API automation, parametric and knowledge-based modelling, GUI design for engineering users, and
the judgement of where to automate and where to leave the engineer in control.
