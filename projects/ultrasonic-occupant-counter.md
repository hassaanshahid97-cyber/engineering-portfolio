# Ultrasonic occupant counter

**Feb 2024 to Jul 2024 · instrumentation project, Institute of Space Technology**

## What it does

Counts people entering and leaving a space in real time and maintains a live occupancy number.

## Implementation

- Arduino UNO with **paired ultrasonic sensors**, so direction of travel is resolved from the order
  in which the two beams break
- Nested logic to handle the cases that break a naive counter: a stationary object inside the beam,
  two people crossing simultaneously, and a person who enters the beam and reverses
- Real-time bidirectional counting with debounce and timeout handling

## Skills demonstrated

Embedded instrumentation, sensor fusion at a small scale, and writing logic against the failure
cases rather than the happy path.
