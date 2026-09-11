# Twin Rotor Aerodynamical System (TRAS) control laboratory rig

**Dec 2022 to Jul 2023 · control systems and dynamics, Institute of Space Technology**

<img src="../images/proj_tras.jpg" width="300" alt="Twin Rotor Aerodynamical System rig">

## What it is

A laboratory plant for high-order nonlinear control experiments whose dynamic behaviour resembles a
helicopter, including significant cross-coupling between the two axes. Built from scratch as a
teaching and research rig.

## Build

| Subsystem | Implementation |
|---|---|
| Mechanics | Beam pivoted for horizontal and vertical rotation, with a counterbalance arm |
| Actuation | Main and tail rotors driven by DC motors, fixed angle of attack |
| Sensing | Pivot encoders for angles, speed sensors for rotor angular velocities |
| Control | Aerodynamic forces controlled by varying rotor speeds, not blade pitch |

## Why it is interesting

The plant is nonlinear, high order and strongly cross-coupled: a change in main rotor speed produces
a yaw moment as well as pitch. It is the standard hard case for system identification and
multivariable control design, and building the rig meant owning the sensing and the identification
as well as the controller.
