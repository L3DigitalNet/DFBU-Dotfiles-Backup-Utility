# CLAUDE.md — DFBU (DotFiles Backup Utility)

**Session startup:** state is injected by the SessionStart hook (see `.claude/hooks/session_start.py`).

**Document layout (read on demand):**
- `docs/handoff/state.md` — live state + active incidents (auto-injected, do not read directly)
- `docs/handoff/deployed.md` — deployment truth
- `docs/handoff/architecture.md` — system graph
- `docs/handoff/conventions.md` — pattern library
- `docs/handoff/sessions/` — monthly session logs (grep by date)
- `docs/handoff/bugs/` — per-file bug KB (grep by service or tag)
- `docs/handoff/specs-plans.md` — pointer into `docs/specs/` and `docs/plans/`
