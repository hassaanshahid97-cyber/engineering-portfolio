# Hardware-in-the-loop and Iron Bird validation framework

**Jun 2024 to Aug 2024 · Design Engineer, Simulation and Test, NaqCoDE Technologies, Islamabad**

## Objective

Establish a real-time testing framework to validate autonomous UAV flight control, aerodynamic
derivatives and hardware reliability before anything flew.

## Architecture

| Layer | Implementation |
|---|---|
| Flight controller | Pixhawk 6X running ArduPlane |
| Physics | X-Plane engine coupled over MAVLink, real time |
| Iron Bird rig | Digital servos and rotary encoders on representative control surfaces |
| Instrumentation | Actuator latency and response rate measurement against MATLAB and Simulink models |
| Vision | NVIDIA Jetson vision node integrated into the loop |

## Results

- Measured actuator latencies and response rates, compared against the Simulink model of the same
  actuator, so model and hardware were reconciled rather than assumed equal
- Validated critical stability derivatives, including **C_L alpha** and **C_m q**, under gust
  conditions
- Produced a repeatable rig procedure for validating a control law before flight test

## Skills demonstrated

Hardware- and software-in-the-loop integration, real-time systems, flight control validation, test
rig design and instrumentation.
