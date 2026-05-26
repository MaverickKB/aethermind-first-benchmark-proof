# AetherMind First Benchmark: Public Metrics Proof Packet

This directory is a redacted public proof packet for the first VM-isolated AetherMind continuity-layer benchmark. It contains recorded operational metrics and artifact-presence proof only. It does not include mechanisms, prompts, terminal logs, visual evidence records, agent answer text, inspected file lists, absolute paths, or setup internals.

## What This Packet Shows

- 90 official preserved benchmark runs.
- 3 agent surfaces: Agent Surface A, Agent Surface B, and Agent Surface C.
- 2 public conditions: `baseline` and `continuity_enabled`.
- 3 task variants, with 5 repeats per agent/condition/task cell.
- 90/90 Connection/preflight successes.
- 90/90 agent exit successes.
- 90/90 complete required artifact packets.
- 90/90 visual evidence captured and reviewed as valid, retained privately.

## Headline Recorded Metrics

Across the official 90-run packet, the continuity-enabled condition recorded lower mean elapsed time and higher mean file/artifact mentions than the baseline condition:

- Mean elapsed seconds: baseline 6344.33, continuity-enabled 4580.38.
- Relative mean elapsed change: -27.8%.
- Mean file/artifact mentions: baseline 5.29, continuity-enabled 6.76.
- Relative mean file/artifact mention change: +27.8%.

## Files

- `per_run_metrics_redacted.csv`: one row per official run, with raw numeric metrics preserved and sensitive identifiers removed.
- `aggregate_metrics_by_condition.csv`: aggregate metrics for baseline versus continuity-enabled conditions.
- `aggregate_metrics_by_agent_condition.csv`: aggregate metrics split by agent and condition.
- `aggregate_metrics_by_task_condition.csv`: aggregate metrics split by task variant and condition.
- `headline_deltas.csv`: direct baseline versus continuity-enabled mean deltas.
- `artifact_presence_redacted.csv`: required artifact-presence booleans for each public run ID.
- `source_record_digests_redacted.csv`: SHA-256 digests of the private copied metrics and manifest records backing each public row.
- `benchmark_matrix_redacted.json`: public-safe benchmark structure.
- `evidence_integrity_counts.json`: public-safe integrity counts and excluded material classes.
- `methodology_redacted.md`: public-safe description of how the benchmark was run.
- `redaction_report.md`: what was removed and why.

## Scope

This packet proves the recorded run metrics and evidence-preservation counts for the first benchmark. Private raw evidence remains preserved separately for audit.
