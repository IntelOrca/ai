---
name: do-issue
description: Work on a GitHub issue until it is complete without human-in-the-loop.
disable-model-invocation: true
---

# Goal

Given a GitHub issue, you must work on it until it is complete
Complete means having merged in a branch which fixes the issue allowing the issue to be closed
You do not need to create a pull request unless the user requested one

# How

- You can never ask the user questions. Do not use the question tool, and never end a turn with a question.
- When you cannot decide, choose the option that is (a) reversible and (b) does not change the test or verification apparatus. Record the alternatives and your reasoning under a "Decisions" heading in the branch or PR description, then continue.
- Stop and end your turn only when no option satisfies both conditions. Write up what you tried, what you ruled out and your best hypothesis, so a human can unblock you in one read. Never wait on input.
- Break the problem down with sub agents to avoid context rot
- Once finished, spin off a sub agent to review the changes and provide feedback
- Implement all feedback from the review sub agent
