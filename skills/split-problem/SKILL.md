---
name: split-problem
description: Derot the context, split time-consuming problem into parallel sub agents with fresh context.
disable-model-invocation: true
---

1. Stop current approach immediately — do not continue iterating in place.
2. Summarize what's been tried, what failed, and why, in 3-5 bullets.
3. Decompose the remaining problem into 2-4 independent, bounded sub-problems (each should be completable without needing the others' intermediate state).
4. Delegate each sub-problem to a fresh subagent, passing only the summary + that sub-problem's scope (not full history).
5. Synthesize results from all subagents into a single resolution before resuming.
