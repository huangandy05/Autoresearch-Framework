# Research rules

Read [experiment.md](experiment.md). Resolve missing setup details before trials.
Keep `src/`, `evaluate/`, the baseline, and completed trials unchanged during runs.
Never tune tests, datasets, seeds, settings, or metrics to favor a candidate.
If controls must change, stop and agree a new baseline with the user.

## Modes

- **User-directed:** write numbered hypotheses in `logs/ideas.md`, then wait for
  user selection. Implement and evaluate only selected ideas.
- **Autonomous:** require a trial-count or elapsed-time budget, then propose,
  implement, and evaluate ideas until it is exhausted. Failed trials count.
  Baseline setup is excluded; trial work starts the clock. If both limits are
  set, stop at the first reached. Stop an active evaluation at the time limit.

## Loop

1. Evaluate `experiments/000-baseline/` using the brief's fixed command. Record it
   as the initial best. Do not proceed if baseline setup or evaluation fails.
2. Give each hypothesis a new folder: `experiments/001-short-name/`, then `002-…`.
   Copy the current best implementation by default; record the parent if different.
   Change only the brief's permitted files inside that new folder.
3. Run the same evaluation with the new trial path, honoring its timeout and any
   remaining run budget. Write output to `logs/<trial-id>.log`.
4. Append to `logs/results.md`: trial, parent, hypothesis, score, outcome, summary.
   Outcomes: baseline, better, worse, tie, failed. Failures/timeouts have no score.
5. Compare with the best using the brief's rule. Retain the incumbent on exact
   ties. Preserve every completed trial folder, including failed candidates.
6. Update `logs/summary.md` with the best folder/score, findings, trials used, and
   elapsed time. Continue only within the selected ideas or autonomous budget.

Create log files when needed; keep entries concise and append results, never erase
history. On resume, read the logs, verify the best folder, and continue numbering.
Do not restart a consumed budget without a new user instruction. Use no Git
branches, resets, or per-trial repositories; folders preserve the experiments.
