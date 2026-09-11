# Aero vehicle performance study, Boeing C-17 Globemaster III

**Aero vehicle performance, Institute of Space Technology · November 2023 to January 2024 · graded 90 of 100**

| | |
|---|---|
| **Context** | Complete flight envelope performance analysis of a heavy military transport |
| **Inputs** | Published geometry, engine data, standard atmosphere models |

## Scope

| Segment | Analysis performed |
|---|---|
| Steady level flight | Thrust and power required against available, maximum and minimum speed, absolute and service ceiling |
| Accelerated flight | Energy height and specific excess power across the envelope |
| Turning flight | Load factor limits, sustained and instantaneous turn rate, corner speed |
| Climbing flight | Rate and angle of climb, time to altitude |
| Take-off | Ground roll, rotation, obstacle clearance distance |
| Landing | Approach, flare, ground roll with reverse thrust |

## Approach

Every result is traced back to its governing equation and the assumption behind it, rather than to a
spreadsheet cell. For a transport aircraft, the interesting part is where the assumptions stop being
safe: drag polar validity at high lift coefficient, thrust lapse with altitude, and the ground effect
and reverse thrust models that dominate field performance.

## What I would do differently

- **Bound the inputs.** Published geometry and engine data carry uncertainty that never appears in the
  results. Carrying a plus or minus band through to field length would be more useful than a single
  number.
- **Validate against operational data.** Published take-off field lengths for the real aircraft are a
  free check on the whole chain.

## Relevance

Aircraft performance from first principles across the full envelope, which is the analysis layer that
sits under every conceptual design decision in the rest of this portfolio.

[Back to portfolio](../README.md)
