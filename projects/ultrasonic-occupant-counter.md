# Ultrasonic occupant counter

**Instrumentation project, Institute of Space Technology · February to July 2024**

| | |
|---|---|
| **What it does** | Counts people entering and leaving a space in real time and maintains a live occupancy number |
| **Hardware** | Arduino UNO, paired ultrasonic sensors |

## Implementation

**Direction from ordering.** Two ultrasonic beams a fixed distance apart. The **order** in which the
beams break gives direction of travel, which a single sensor cannot resolve at any sample rate.

**Logic written against the failure cases.** The naive counter works on the happy path and fails on
everything else, so the state machine handles:

- a stationary object parked inside a beam, which otherwise latches the count
- two people crossing simultaneously in opposite directions
- a person who enters the first beam and reverses without crossing
- debounce and timeout on both channels

## Why it is in this portfolio

It is a small project with the habit that matters in it: the specification is the edge cases, and the
happy path is the easy part. The same instinct appears at a larger scale in the
[calibrated error bound](physics-informed-surrogates.md) work, where the interesting behaviour is in
the tail of the distribution and not in the mean.

## Relevance

Embedded instrumentation, sensor fusion at small scale, and state machine design against real failure
modes.

[Back to portfolio](../README.md)
