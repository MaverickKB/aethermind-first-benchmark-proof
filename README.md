# AetherMind First Benchmark Report

AetherMind is a continuity layer for AI-assisted work. It is designed around a
simple problem: AI agents often return to projects as strangers, even when the
work itself has accumulated decisions, warnings, corrections, risks, and
evidence that should carry forward.

This repository publishes the public-safe results from AetherMind's first
VM-isolated onboarding benchmark. The raw evidence remains private; this report
contains only redacted operational metrics and proof artifacts.

## Benchmark Summary

The benchmark compared agent onboarding behavior on the same fixed demo
repository under two conditions:

- `baseline`: stock agent environment against the same repository bytes.
- `continuity_enabled`: same repository with AetherMind continuity available.

The test matrix:

| Measured Item | Result |
| --- | ---: |
| Official preserved runs | 90 |
| Agent surfaces tested | 3 |
| Conditions compared | 2 |
| Task variants | 3 |
| Repeats per cell | 5 |
| Connection/preflight success | 90/90 |
| Agent exit success | 90/90 |
| Required evidence packets preserved | 90/90 |
| Visual evidence captured and valid | 90/90 |

## Headline Result

Across the full 90-run benchmark packet, the continuity-enabled condition
recorded lower aggregate mean elapsed time and higher file/artifact engagement
than the baseline condition.

| Metric | Baseline Mean | Continuity-Enabled Mean | Relative Change |
| --- | ---: | ---: | ---: |
| Elapsed seconds | 6344.33 | 4580.38 | -27.8% |
| Event lines | 1046.27 | 1079.36 | +3.2% |
| Tool-call signals | 22.18 | 20.71 | -6.6% |
| Command signals | 31.07 | 32.29 | +3.9% |
| File/artifact mentions | 5.29 | 6.76 | +27.8% |

## What A Continuity Layer Means Here

A continuity layer is the part of a project or artifact that carries forward
working experience. It preserves the context a future agent needs to orient
quickly and act safely: mission, constraints, decisions, corrections, friction,
uncertainty, risk, and evidence.

This benchmark did not test hidden provider memory or generic chat recall. It
tested whether a project-level continuity condition changed onboarding behavior
under a preserved, repeatable run packet.

## Evidence Packet

The redacted proof packet is in [`proof/public-redacted-proof/`](proof/public-redacted-proof/).

It includes:

- per-run operational metrics;
- aggregate metrics by condition, task variant, and agent surface;
- headline deltas;
- evidence-preservation counts;
- source-record digests for private audit traceability;
- redacted methodology;
- a redaction report.

The same packet is also provided as a zip:

- [`proof/public-redacted-proof.zip`](proof/public-redacted-proof.zip)
- [`proof/public-redacted-proof.zip.sha256`](proof/public-redacted-proof.zip.sha256)

Zip SHA-256:

```text
a5857cd471aa65acb35b2568f64fd43788a383de4807002d0238731ff30e351d  public-redacted-proof.zip
```

## Public Scope

This repository intentionally does not include raw logs, recordings, prompts,
agent answers, inspected file lists, absolute paths, setup internals, private
condition details, or implementation mechanisms.

The result should be read as preliminary benchmark evidence: one preserved
90-run onboarding packet showing that the continuity-enabled condition changed
measured orientation behavior. The next evaluation step is answer-quality
scoring against the frozen rubric.
