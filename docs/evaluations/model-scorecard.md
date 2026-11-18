# Model scorecard — rule R1 (pensionableSalary)

> One run is a sample, not a benchmark. Synthetic data only — never paste secrets or real member data.

| | Model A | Model B |
|---|---|---|
| Model (name as shown in the picker) | Haiku 5.5 | |
| Harness · Mode · Permissions | Copilot · Interactive · Manual | Copilot · Interactive · Manual |
| Reasoning effort | medium | |
| Date | 2026-11-18 | |

## Scores

| Criterion | How to score | Model A | Model B |
|---|---|---|---|
| Correctness verified | Expected values that match the `node -e` output (x / 5) | /5 | /5 |
| Edge cases found | Which did it cover? franchise boundary · salary cap · part-time · below franchise → 0 · invalid factor (0 or > 1) · negative salary | | |
| Hallucinations | Invented functions, parameters, files or rules? List them (none = 👍) | | |
| Latency feel | fast / ok / slow | | |
| Cost / credits | Relative cost of the model (supported-models doc) — heavier model = more AI credits | | |

## Verification output

```text
Model A (Haiku 5.5), as pasted by the user (flattened; unverified as raw console output):
fullTimeSalary  partTimeFactor  result
17545           1               0          (salary equals the franchise, so the base is zero)
137801          1               120255     (one euro over the cap, so it is capped at 137,800)
50000           0               throws RangeError: partTimeFactor must be greater than 0 and at most 1

Model B: (paste the node -e output here)
```

## Verdict

- For **this kind of task** I would use: …
- Because: …
- Would I trust it **without** the `node -e` check? yes / no — why?
- To make this a real benchmark I would need: …
