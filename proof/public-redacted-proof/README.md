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

Across the official 90-run packet, the continuity-enabled condition recorded
stronger scored orientation coverage, lower wall-clock harness elapsed time,
and higher file/artifact mentions than the baseline condition.

Scored orientation lift:

- Concept coverage: 25.49 -> 31.07, +21.9%.
- Runtime / permission gate coverage: 3.44 -> 5.47, +58.7%.
- Output / context boundary coverage: 1.89 -> 4.84, +156.5%.
- File-grounding mentions: 5.29 -> 6.76, +27.7%.
- Strict JSON / required-shape success: 97.8% -> 100.0%.
- Tool calls: 22.18 -> 20.71, -6.6%.
- Answer length: 6289 -> 6191 chars, -1.6%.

Raw operational metrics:

- Mean elapsed seconds: baseline 6344.33, continuity-enabled 4580.38.
- Relative mean elapsed change: -27.8%.
- Mean file/artifact mentions: baseline 5.29, continuity-enabled 6.76.
- Relative mean file/artifact mention change: +27.8%.

Elapsed seconds are wall-clock harness elapsed time, not a clean measure of
active agent work time.

## Files

- `per_run_metrics_redacted.csv`: one row per official run, with raw numeric metrics preserved and sensitive identifiers removed.
- `aggregate_metrics_by_condition.csv`: aggregate metrics for baseline versus continuity-enabled conditions.
- `aggregate_metrics_by_agent_condition.csv`: aggregate metrics split by agent and condition.
- `aggregate_metrics_by_task_condition.csv`: aggregate metrics split by task variant and condition.
- `headline_deltas.csv`: direct baseline versus continuity-enabled mean deltas.
- `scored_orientation_summary.csv`: scored overall continuity lift summary.
- `scored_orientation_summary.json`: scored lift summary with matrix notes and interpretation.
- `scored_orientation_by_agent_surface.csv`: scored lift summary by redacted agent surface.
- `scored_orientation_by_task_variant.csv`: scored lift summary by task variant.
- `artifact_presence_redacted.csv`: required artifact-presence booleans for each public run ID.
- `source_record_digests_redacted.csv`: SHA-256 digests of the private copied metrics and manifest records backing each public row.
- `benchmark_matrix_redacted.json`: public-safe benchmark structure.
- `evidence_integrity_counts.json`: public-safe integrity counts and excluded material classes.
- `methodology_redacted.md`: public-safe description of how the benchmark was run.
- `redaction_report.md`: what was removed and why.

## Scope

This packet proves the recorded run metrics and evidence-preservation counts for the first benchmark. Private raw evidence remains preserved separately for audit.
