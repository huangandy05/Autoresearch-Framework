# Experiment brief

Replace the placeholders before running trials. Commands run from the repo root.

## Problem and setup

- Objective: <what to improve>
- Context: <references and relevant files in src/>
- Setup command: <dependencies and reproducible environment setup>
- Baseline: <source of the implementation in experiments/000-baseline/>
- Editable scope: <files/behavior allowed inside each new trial folder>

## Fixed evaluation

- Evaluation command: <command using evaluate/ and a {trial_dir} argument>
- Tests and datasets: <paths in evaluate/; sources, versions, acquisition steps>
- Settings: <seeds, sample sizes, resource limits, and other fixed controls>
- Metric: <name, how to extract it from output, and minimize/maximize>
- Improvement rule: <comparison and tie-breakers; exact ties retain the incumbent>
- Per-trial timeout: <maximum evaluation duration>

## Operation

- Mode: <user-directed or autonomous>
- Autonomous budget: <trial count and/or elapsed-time limit; required in this mode>
- Constraints: <additional requirements, or none>
