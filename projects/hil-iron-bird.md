# Hardware-in-the-loop and Iron Bird validation framework

**Design Engineer, Simulation and Test, NaqCoDE Technologies, Islamabad · June to August 2024**

| | |
|---|---|
| **Context** | Industry role, autonomous UAV flight control validation |
| **My role** | Built the real-time framework end to end: architecture, rig, instrumentation and model comparison |
| **Stack** | Pixhawk 6X, ArduPlane, MAVLink, X-Plane, MATLAB and Simulink, NVIDIA Jetson |
| **Status** | Delivered and used for pre-flight validation |

> **Takeaway for a supervisor:** the output of a rig is not a model that matches. It is knowing by how
> much the model and the hardware disagree, in which direction, and whether that gap matters for the
> control law.

---

## 1. Problem

Flying an autonomous UAV to find out whether its control law works is expensive and slow, and the
failure modes that matter, actuator lag and gust response, are exactly the ones a desktop simulation
gets wrong. The task was to build a real-time framework that validates flight control, aerodynamic
derivatives and hardware reliability **before** anything flies.

---

## 2. Architecture

```
   X-Plane physics engine
            |  MAVLink, real time
   Pixhawk 6X running ArduPlane
            |  PWM
   Iron Bird rig: digital servos, rotary encoders
            |  measured angle and timing
   MATLAB and Simulink actuator and airframe models
            |
   NVIDIA Jetson vision node in the loop
```

| Layer | Implementation |
|---|---|
| Flight controller | Pixhawk 6X running ArduPlane |
| Physics | X-Plane coupled over MAVLink, real time, hardware in the loop |
| Rig | Physical Iron Bird with digital servos on representative surfaces and rotary encoders on the output shafts |
| Instrumentation | Actuator latency and response rate measured directly, not inferred from command |
| Vision | NVIDIA Jetson node integrated so the perception path sees the same simulated world |

---

## 3. What the rig measured

**Actuator latency and response rate.** Commanded deflection against measured deflection, timed on the
encoder. The measured response was then compared against the MATLAB and Simulink model of the same
actuator. Model and hardware were **reconciled**, not assumed equal, which is the entire reason to
build the rig rather than trust the data sheet.

**Stability derivatives under gust.** Critical derivatives including **C_L alpha** and **C_m q** were
validated under gust conditions inside the closed loop, where the autopilot is reacting to the
disturbance rather than the model being evaluated open loop.

**Hardware reliability.** Servos and linkages run at flight duty cycle for extended periods on the
bench, where a failure costs a servo instead of an airframe.

---

## 4. Why this matters for autonomy

An autonomous landing or a gust rejection law is only as good as the actuator model underneath it. A
20 ms discrepancy in servo lag is invisible in a desktop simulation, changes the phase margin of the
inner loop, and shows up as an oscillation on approach. Measuring it on the bench moves that discovery
from the flight line to the lab.

---

## 5. What I would do differently

- **Automate the sweep.** Latency was measured at representative settings. A scripted frequency sweep
  would give a Bode plot of the actuator rather than a handful of step responses, which is what the
  control designer actually wants.
- **Log everything, in one clock.** Rig, autopilot and simulator each keep their own time. A single
  synchronised log would remove the manual alignment step and the error that comes with it.
- **Fault injection.** The rig validates the nominal system. Injecting a stuck surface or a saturated
  servo is where a hardware-in-the-loop bench earns its cost.

---

## 6. Relevance to a master thesis

Model validation against measured hardware, real-time simulation, and the discipline of chasing a
model-hardware discrepancy instead of tuning it away. Directly relevant to thesis work in flight
systems simulation, autonomy validation, or any project where a model has to be trusted enough to
make a decision.

[Thesis readiness](../docs/thesis-readiness.md) · [Back to portfolio](../README.md)
