# Biometric data, uncertainty, and recovery signals

[Back to the project overview](../README.md)

The project treats health observations as records with explicit provenance and quality. Numerical processing is separate from specialist interpretation.

## Data handling requirements

| Concern | Design behavior |
| --- | --- |
| Measured value | Preserve the observation with its unit, timestamp, source, and measurement context |
| Missing measurement | Keep it unknown; do not insert a healthy-looking default |
| Invalid measurement | Identify or reject invalid data and exclude unusable observations from calculations |
| Stale observation | Retain its history and mark its quality rather than silently presenting it as current |
| Units and timestamps | Validate and normalize supported representations deterministically |
| Duplicate event | Reuse the event identity; distinguish a repeat from a conflicting revision |
| Device or method change | Keep incompatible streams separate rather than silently merging them |
| Repeated cumulative total | Avoid adding repeated daily snapshots together |
| Overlapping intervals | Detect ambiguity instead of double-counting the same period |
| Baseline coverage | Track available evidence and return insufficient data when coverage is inadequate |

The integration boundary is device-independent where practical. A real wearable still needs an adapter and acceptance checks against its actual export behavior. A supported data type does not guarantee a particular device supplies it.

## From observations to recommendations

| Layer | Responsibility |
| --- | --- |
| Observations | Record what was measured, when, by which source, and with what quality |
| Deterministic processing | Normalize compatible values and aggregate them with explicit semantics |
| Personal baselines and trends | Calculate summaries from eligible historical observations |
| Quality and uncertainty | Preserve missingness, staleness, ambiguity, and limited coverage |
| Recovery heuristic | Flag defined patterns for planning purposes |
| Specialist interpretation | Discuss possible associations using the supplied evidence |
| Action authorization | Allow, defer, or reject a proposed activity within policy |

An LLM does not invent the numerical baseline or supply absent measurements. Exact formulas, thresholds, and tuning parameters remain in the private implementation.

## Stress is not a single sensor reading

The design distinguishes self-reported stress from biometric recovery patterns. It uses relevant consumer-device observations, including comparable HRV and resting-heart-rate data when available, to support a scheduling heuristic. It does not diagnose stress, illness, or autonomic dysfunction.

An agent may describe an observed association and acknowledge uncertainty. The system does not establish that an activity caused a physiological change or that a recommendation treats a condition.

## What the demo shows

The screenshot fixture contains 32 days of fabricated HRV and resting-heart-rate observations. A constructed deviation produces a recovery-attention state and a non-diagnostic alert. Sleep and step measurements are absent and remain **Unknown**. The fixture demonstrates software behavior, not physiological accuracy or clinical effectiveness.

[View the labelled screenshots](screenshots.md) · [Read validation scope](validation.md)
