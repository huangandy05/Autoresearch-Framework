# AutoResearch

A minimal starter for agent-driven research. Each trial lives in its own folder;
Git is optional and is not used to manage experiments.

## Structure

| Path | Contents |
| --- | --- |
| `AGENTS.md` | Entry point for coding agents |
| `program/` | Operating rules and the experiment brief |
| `src/` | Shared context, references, and stable helper code |
| `evaluate/` | Fixed testing scripts, datasets, and evaluation settings |
| `experiments/` | Baseline and separate implementations for each trial |
| `logs/` | Ideas, results, summaries, and evaluation output |

## Set up

1. Copy this folder, or publish it as a repository and clone it.
2. Put relevant reference material and existing helper code in `src/`.
3. Put your standard tests and datasets in `evaluate/`. Record dataset sources,
   versions, acquisition steps, and fixed settings in the experiment brief.
4. Put your starting implementation in `experiments/000-baseline/`.
5. Fill in [program/experiment.md](program/experiment.md), including reproducible
   setup and evaluation commands that accept a trial folder.
6. Ask an agent to read [AGENTS.md](AGENTS.md) and follow the selected mode.

**User-directed:** the agent proposes ideas; you select which it implements.
**Autonomous:** the agent proposes and tests ideas within your trial/time budget.

Completed trials are preserved. Evaluation inputs and settings stay fixed across
trials; logs identify the best implementation. No runner or dependencies are bundled.
