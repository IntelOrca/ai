---
name: plan-issue
description: Create a plan with the user for a new feature or change as a github issue
disable-model-invocation: true
---

# Goal

To create a new GitHub issue with a detailed plan of the user's requirements for a new feature or change. The issue body should contain enough information for another agent to work on end-to-end without a human in the loop.

# How

Do not investigate bugs, you are just raising an issue for it
Use the grilling skill
Search other GitHub issues to check for similar or dependencies
Once user confirms they are happy with plan, create new issue on GitHub repo
Do not artificially wrap issue body text
Once GitHub issue is created, your goal is complete. Do not follow up with any more questions or work
Example end to conversation:

> [#6 New issue title](https://github.com/org/repo/issues/6) has been created.
