---
name: finalise
description: Finalise a session with a review -> fix -> commit -> push.
disable-model-invocation: true
---

1. /review using a sub agent
2. When sub agent returns, fix all reported issues
3. /commit
4. Push commits
5. Clean up after yourself, e.g. remove any temp. files
6. Summarise all work to the user
