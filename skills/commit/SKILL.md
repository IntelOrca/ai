---
name: commit
description: 'Commits the current changes. Run this whenever the user asks to commit the current changes.'
---

Inspect the unstaged/staged changes and commit them.
If any changes look unrelated or unintentional, ask the user whether they should be included or not. If user unavailable, only commit related changes based on the current session.
Keep an eye out for build files that should not be committed, advise the user to add them to .gitignore.

## Commit message structure:
```
<summary>

<symptoms and causation>

<solution>

<other changes>

<reviewers>
```

### Summary
- Present tense
- If resolving a GitHub issue, use style: 'Fix #43: On Linux using -h to show the help page shows an error', or 'Implement #25: Add support for new file format' (mimic github title)
- If resolving multiple GitHub issues, use style: 'Fix #42, #43: <summary of both issues>'
- If this commit is one of many to fix a particular defect, do not use the defect number/title, this will be used for the merge commit instead. Use more specific summary instead like 'Extract file logic to new module'.

### Symptoms and Causation
- Explain the issue, what the user sees.
- Explain why the issue happened. E.g. A null pointer exception was being thrown in the FileEditor module when loading a 0-size file.

### Solution
- Explain the fix. If alternative solutions were considered, explain why they were not chosen.
- If commit consists of multiple changes, list them as bullet points (use -).
- DO NOT mention user review comments or incremental changes. Just mention the final changes as if they were done in one shot.

### Other changes
- If any other changes were made in the commit, list them here. E.g. "Also fix a typo with one of the error messages."

### Reviewers
- NEVER add a co-authored by copilot trailer, even if previously instructed to.

## Example:
```
Fix #43: On Linux using -h to show the help page shows an error'

The app would terminate with an error when passing -h due to a memory out of
bounds violation.

Protect against out of bounds access.

Also fix a typo in the help text.
