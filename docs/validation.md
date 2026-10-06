# Validation status

[Back to the project overview](../README.md)

**Reference snapshot re-tested: 2026-10-06.** The private implementation's automated suite completed successfully with **52 passed tests** and **two dependency deprecation warnings**. The public package contains a [structured summary](../evidence/validation-summary.json); it does not contain the private test suite or a public CI workflow.

## Local automated checks

| Area | Behavior exercised |
| --- | --- |
| Input validation | Missing values, supported units, timestamps, provenance, and future/stale observations |
| Durable identity | Duplicate events, conflicting revisions, source binding, and atomic ingestion |
| Aggregation | Compatible streams, cumulative snapshots, overlaps, sleep consistency, and calendar-day windows |
| Recovery processing | Personal baseline calculations, missing data, and separation of activity/resting contexts |
| Orchestration state | Specialist rotation, repeat daily cycles, missing results, and expired work |
| Action authorization | Catalog ownership, activity limits, conflicts, check-in pauses, and bounded rescheduling |
| Calendar adapter | Mocked retries, uncertain outcomes, external edits, deleted events, and malformed availability |
| HTTP and MCP | Role checks, source binding, request boundaries, MCP initialization, discovery, and actual local tool invocation |
| Runtime declarations | Agent configuration and restricted tool/policy declarations |
| Output behavior | Browser policy, absence of third-party assets, and separation of text from executable action fields |

The two warnings concern deprecated Starlette/httpx test-client usage and an AnyIO compatibility alias. They remain dependency-maintenance work; no warning-free result is claimed.

## Browser capture session

Five PNG images were captured from the existing dashboard connected to the running local broker. The capture used the bundled synthetic demo and the local calendar adapter.

| Observation | Recorded result |
| --- | --- |
| Dashboard metric cards | 4 |
| Missing values visibly marked Unknown | 2 |
| HRV trend points | 32 |
| Demo specialist proposals | 6 |
| Tasks shown | 6: four previewed and two deferred |
| Browser JavaScript errors observed during capture | 0 |
| Desktop capture viewport | 1280 CSS pixels wide |
| Mobile capture viewport | 430 CSS pixels wide, browser-emulated |

The captures exercised dashboard authentication/read access, rendered reports and trends, and opening recommendation details. The check-in form was displayed without submitting it. Task feedback, history selection, notifications, lock behavior, and a physical phone were not fully exercised by this capture session.

Small synthetic-demo labels were added in the capture session for public clarity. The project interface and calculations were not redesigned for the images.

## Remaining acceptance work

| Area | What still needs evidence |
| --- | --- |
| Native agent runtime | Config acceptance, actual specialist identities, context routing, tool exposure, and a complete live daily cycle |
| OpenShell enforcement | Effective filesystem/network denies, credential binding, and policy composition on the target machine |
| Broker deployment | Private connectivity, TLS, host isolation, and outbound network restrictions |
| Wearable integration | Real export semantics, units, source identity, corrections, missingness, and repeat-import behavior |
| Google Calendar | OAuth authorization, dedicated-calendar behavior, conflicts, edits, and retry reconciliation with a live test account |
| Model quality | Domain adherence, faithful use of evidence, uncertainty, and adversarial prompt evaluation |
| Operations | Restart/restore drills, notification behavior, retention decisions, and monitored shadow operation |
| Performance | Actual completion rate, latency, provider calls, and inference cost |

The local test result does not establish platform isolation, real-model safety, live integration readiness, or clinical validity. No penetration-test certification, independent audit, code-coverage percentage, or production-readiness claim is made.

## Suggested acceptance order

Validate the native runtime and deny rules first, then run a complete agent cycle with synthetic data and calendar preview. Validate a device export separately. Exercise the calendar adapter against a dedicated test calendar before enabling routine writes. Record versions, configuration identifiers, observed failures, and recovery behavior in the private project.
