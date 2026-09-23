# Mobile Media Service Continuity

**Status: In Progress — 3 of 5 baseline runs completed**

A small field study of background media playback across a repeatable real-world route.

## Why I did this

For a while, I occasionally noticed YouTube Premium background playback stop after leaving home while listening through my Powerbeats Pro. I never knew why. More recently, the behavior seemed to disappear.

While learning about Field Quality Assurance, I became interested in a simple question: could I still reproduce it?

Rather than assume a cause, I designed a repeatable route and documented only what I could directly observe.

## Research question

Does an active media session remain usable while an iPhone moves through a repeatable real-world route under normal connectivity settings?

## Test setup

- **Device:** iPhone 15 Pro
- **Audio:** Powerbeats Pro
- **Service:** YouTube Premium background playback
- **Route:** ~2-mile out-and-back walk
- **Runs planned:** 5
- **Wi-Fi:** On
- **Cellular Data:** On
- **Low Power Mode:** Off
- **VPN:** Off

Each run follows the same route and uses five fixed physical landmarks:

**A → B → C → D → E → D → C → B → A**

The test does not attempt to identify specific Wi-Fi or cellular transitions. Without network diagnostics or protocol-level data, those events cannot be established from observation alone.

## Method

Each run begins indoors with background playback active and follows the same out-and-back route under the baseline settings above. Playback is observed throughout the route for:

- Interruption
- Buffering
- Playback degradation
- Automatic recovery
- Required user intervention

Runs are classified as:

- **PASS** — no perceptible interruption or degradation
- **OBSERVED INTERRUPTION** — a customer-visible playback issue occurs
- **INVALID RUN** — the planned procedure or conditions are not maintained

For any observed issue, the goal is to record what happened, where it happened, how long it lasted, and whether playback recovered without intervention.

### Observation vs. interpretation

A central rule of the project is to separate what was observed from what might explain it.

**Observation:**  
> Playback stopped for approximately four seconds between landmarks B and C and resumed automatically.

**Unsupported interpretation:**  
> The iPhone failed its Wi-Fi-to-cellular handoff.

Without diagnostic data, the second statement cannot be established from the first.

## Methodology reference

The structure of this project was informed by public GSMA TS.11 field-testing methodology, particularly its emphasis on defined conditions, repeatable procedures, observations, and documented results.

This project does not reproduce GSMA testing or claim conformance with a GSMA test procedure.

## Baseline results

Three of five planned baseline runs have been completed.

| Run | Date | Duration | Playback | Result |
|---|---|---:|---|---|
| R01 | 2026-09-19 | ~40 min | 0:00–39:55 | PASS |
| R02 | 2026-09-19 | ~38 min | ~1:09–1:49 hr | PASS |
| R03 | 2026-09-21 | ~37 min | 0:00–35:23 | PASS |

Across all three completed runs, continuous background audio playback was maintained throughout the complete out-and-back route. No perceptible interruption, buffering, or playback degradation was observed.

## Interim finding

Under the defined baseline conditions, the original playback behavior has not been reproduced across three completed runs.

This does not establish that playback will never fail or that every underlying connectivity transition occurred without issue. It means only that no customer-visible interruption was observed during the completed runs.

Two baseline runs remain.

## Limitations

This is a small observational field study, not an instrumented network test.

The project does not capture signal strength, Cell IDs, network transitions, protocol logs, or other diagnostic data. It therefore cannot determine why playback remains continuous or attribute an interruption to a specific network, device, application, or accessory behavior.

Results apply only to the device, service, route, settings, and runs documented here.

## Supporting evidence

Detailed run data is available in the [FQA-001 test evidence workbook](./FQA-001-test-evidence.xlsx), including:

- Test plan and baseline conditions
- Field log
- Individual run details
- Battery levels
- Media used during each run
- Observations and results
- Planned test iterations

The workbook will be updated as the remaining baseline runs are completed.

## Next step

Complete the remaining two baseline runs before deciding whether a follow-up test is warranted.
