# Codex Instructions for DFBU

**Session state:** detect layout first. V2: read `docs/state.md`, then this file, then conventions; V1: read `docs/handoff.md`, then this file, then conventions.

**Full conventions reference:** [`docs/conventions.md`](docs/conventions.md) - LLM-targeted pattern library. Every convention follows the six-field schema (Applies-when / Rule / Code / Why / Sources / Related) with a Quick Reference table at the top for O(1) lookup. Do not introduce new patterns without checking conventions first.

**Detailed review workflows:** [AGENTS.reviews.md](AGENTS.reviews.md) - read this only for review-related tasks (review planning, review sweeps, code/security/test/etc. reviews). The verbose per-review routing, defaults, and orchestrator notes live there.

## Repo Purpose

Linux desktop app for backing up and restoring dotfiles.

## Commands

```bash
uv sync
uv run pytest
uv run dfbu
```

## Stack

- PySide6 / Qt desktop UI
- `uv` for environment management
- `pytest` for tests
- Packaging assets live under `packaging/`
