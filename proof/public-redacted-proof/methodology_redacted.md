# Redacted Methodology

The benchmark compared agent onboarding behavior on a fixed demo repository under two public conditions: a baseline condition and a continuity-enabled condition.

Each official run used the same VM-isolated benchmark shape:

1. Restore the benchmark environment to the controlled starting state.
2. Use the same fixed demo repository bytes.
3. Start a fresh agent run for one agent, one condition, one task variant, and one repeat.
4. Preserve recorded operational metrics and required evidence artifacts.
5. Record screen evidence privately and mark whether visual evidence was valid.
6. Export public-safe numeric metrics without raw logs, prompts, answer text, setup details, paths, or mechanism-bearing files.

The public matrix contains 3 agents, 2 conditions, 3 task variants, and 5 repeats per cell, for 90 official runs.

The public packet includes run-status, elapsed-time, event-line, tool-signal, command-signal, file/artifact mention-count, artifact-completeness, and screen-evidence-validity metrics. It excludes answer quality scoring and mechanism details.
