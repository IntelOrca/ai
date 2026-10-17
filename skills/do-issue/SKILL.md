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

- Once you start working on the issue, you can not ask the user questions
- Only when you hit a major blocker can you stop and wait for user
- Break the problem down with sub agents to avoid context rot
- Once finished, spin off a sub agent to review the changes and provide feedback
- Implement all feedback from the review sub agent
