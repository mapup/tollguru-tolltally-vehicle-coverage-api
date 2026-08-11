# TollGuru Vehicle Coverage API - Wiki Repository

## Overview
This repository provides vehicle coverage data for TollGuru and TollTally services. It acts as a reference/metadata layer defining which vehicle types are supported across different regions. 

## Purpose
Defines "vehicle coverage" in the context of TollGuru and TollTally:
- Supported vehicle types
- Region-wise vehicle coverage
- Default vehicle type configuration

## Documentation

Please refer to the Wiki for detailed documentation:

➡ Wiki: https://github.com/mapup/tollguru-vehicle-coverage-toll-api/wiki

## Setup

Run this once after cloning (and once per new git worktree):

```bash
./hooks/install.sh
```

It points `core.hooksPath` at `hooks/` and installs [gitleaks](https://github.com/gitleaks/gitleaks)
if it is missing, so a `pre-commit` scan blocks any commit containing a secret. The wiring
lives in `.git/config`, which is not tracked, so cloning gets you the hook files but not the
hook — hence the one command. Re-running is a no-op.

Verify it took:

```bash
git config --get core.hooksPath   # -> hooks
gitleaks version
```

The `gitleaks` GitHub Actions workflow scans full history as the backstop for any clone that
never ran the installer. Emergency bypass for a single commit: `GITLEAKS_SKIP=1 git commit ...`



