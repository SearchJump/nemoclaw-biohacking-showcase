# Security design and evidence

[Back to the project overview](../README.md)

The security model assumes that agent output can be mistaken or influenced by untrusted content. Prompts communicate responsibilities; authorization comes from tool exposure, runtime policy, authenticated identities, and deterministic action checks.

## Boundary map

| Boundary | Intended enforcement | Evidence and limitation |
| --- | --- | --- |
| Agent filesystem and network | OpenShell policy around the reasoning runtime | Configuration declarations were tested; actual platform allow/deny behavior still requires target-machine validation |
| External actions | Narrow MCP capabilities plus the broker's action contract | Local MCP and action-authorization tests passed; live agent integration remains pending |
| Credentials | Separate integration credentials and endpoint-bound credential delivery | Separation exists in the design; deployed secret delivery must be verified |
| Device ingestion | Authenticated source identity, schema checks, and provenance | Local input and source-binding tests passed; trusted-source identity does not attest sensor accuracy |
| Agent interaction | Selected specialist sessions, scoped context, and restricted tool exposure | Declared controls exist; specialists share a runtime and are not independent hostile tenants |
| Persistent records | Broker-controlled storage and transactional state changes | Local identity, revision, and lifecycle tests passed; tamper-proof storage is not claimed |
| Dashboard output | Plain-text rendering, restricted browser policy, and separate owner authorization | Local HTTP/static checks and browser captures completed; persuasive or incorrect prose remains possible |

## Untrusted content

Measurements, notes, references, past recommendations, and specialist replies are inputs. They cannot grant new capabilities or alter owner-controlled policy.

The action interface does not accept general-purpose network destinations, shell commands, or arbitrary calendar payloads from model text. Proposal fields must satisfy the broker's contract. Local tests check that injected prose does not become an executable calendar payload.

That boundary limits consequences. It does not establish that prompt injection is solved or that every generated recommendation is correct. Real-model adversarial evaluation remains necessary.

## Bounded autonomy

The design allows routine, permitted calendar actions without requesting approval for each one. The broker checks activity eligibility, time limits, availability, task ownership, and allowed state transitions.

| Situation | Expected handling |
| --- | --- |
| Suitable routine activity | Plan it within owner-controlled limits |
| Too many activities or unsuitable timing | Defer the activity |
| Calendar availability is unknown | Wait rather than assuming a free slot |
| A previous write has an uncertain outcome | Reconcile the existing task identity before repeating the write |
| An externally edited or deleted event | Preserve the external change; do not silently overwrite or recreate it |
| User records a skipped activity | Record the outcome; this does not automatically delete a calendar event |
| Requested destructive or unrelated operation | Reject it or leave it outside the exposed tools |

Calendar titles and action parameters come from controlled templates. Private health commentary belongs in the private report. Recovery alerts do not automatically cancel appointments already written.

## Residual risks

- A manipulated coordinator can still choose among its permitted capabilities and produce misleading prose.
- Specialist separation inside one runtime is weaker than separate operating-system isolation for every agent.
- An authenticated exporter can submit inaccurate measurements under its own identity.
- Authorized context can be processed by the configured inference provider.
- The broker has its own filesystem, network, and credential boundaries; the agent sandbox does not automatically enforce them.
- No medical-device certification, guaranteed emergency alerting, multi-user tenant isolation, encrypted database engine, or tamper-proof audit is claimed.

See [validation status](validation.md) for the checks performed and the checks still pending. Exact policies, credentials, endpoints, and attack fixtures are kept in the private implementation.
