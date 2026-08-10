---
'astro': patch
---

Fixes the dev server refusing to start with "Another astro dev server is already running" after a Docker container restart. The lock file now verifies the recorded port is still listening, so stale lock files left behind by container restarts with PID reuse are correctly detected and cleaned up.
