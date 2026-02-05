# bashops

`bashops` is a collection of **defensive, production-style Bash utilities** for Linux operations.
The project focuses on **system health, local security auditing, safe automation, and reporting**, following patterns commonly used in real-world ops and security teams.

This repository is intentionally **not offensive** and does not perform exploitation, brute force, or remote attacks.
Its goal is to provide **reliable, auditable, and predictable automation** for Linux environments.

---

## Why this project exists

Many Bash repositories contain isolated scripts with:
- no shared conventions
- no logging standards
- no documentation
- unsafe defaults

`bashops` was created to explore **what production-grade Bash looks like** when treated as a small internal toolset instead of ad-hoc scripts.

The focus is on:
- clarity over cleverness
- defensive automation
- explicit behavior
- minimal dependencies
- documentation-first design

---

## Target audience

This project is useful for:
- Linux system administrators
- DevOps / Platform engineers
- Security engineers (defensive / blue team)
- Students learning real-world Bash practices
- Anyone maintaining Linux machines or servers

---

## Design principles

- **Predictable interfaces**  
  Every script supports `--help`. Many support `--json`.

- **Human and machine readable output**  
  Default output is readable. Structured output is available when needed.

- **Defensive by default**  
  No destructive action without explicit intent.
  Support for `--dry-run` where applicable.

- **Minimal dependencies**  
  Avoids external tools when possible. No mandatory `jq`.

- **Fail fast and loud**  
  Uses strict Bash mode: `set -euo pipefail`.

---

## Repository structure

```text
bashops/
├─ scripts/        # Executable operational tools
├─ lib/            # Shared Bash libraries
├─ docs/           # Design and security documentation
├─ tests/          # Automated tests (BATS)
├─ examples/       # Example outputs and reports
├─ Makefile        # Development helpers
└─ .github/        # CI configuration

