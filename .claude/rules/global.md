# Global rules — always loaded

Moved from `docs/conventions.md` DOC-001 / DOC-002 / DOC-003 on 2026-04-24 during handoff-system-v2 Phase 5.

---

## DOC-001. LLM-first docs

**Applies when:** editing files under `docs/`.
**Rule:** keep `docs/` concise, scannable, and optimized for LLM retrieval.

```md
Use short sections, flat bullets, and tables instead of narrative prose.
```

**Why:** repo docs are for session continuity and quick lookup, not human-oriented long-form reading.

**Sources:** `AGENTS.md`, handoff-system-v2 migration.
**Related:** DOC-002, DOC-003.

---

## DOC-002. Session start

**Applies when:** starting any session in this repo.
**Rule:** live state is injected automatically by `.claude/hooks/session_start.py` (SessionStart hook). Read other `docs/` files on demand per the layout listed in `CLAUDE.md`.

```md
No manual "read handoff.md first" step — the hook injects state from
docs/state.md + git log + working tree into each session's context.
```

**Why:** advisory "read first" directives drift. The hook makes the flow deterministic.

**Sources:** handoff-system-v2 migration plan §8.
**Related:** DOC-001.

---

## DOC-003. Convention changes

**Applies when:** adding or revising a persistent repo convention.
**Rule:** record the convention in `.claude/rules/<topic>.md` (with `globs:` frontmatter if path-scoped) or in this file (if always-applicable). Add a pointer row to `docs/conventions.md` under the same numeric ID so `§N` cross-references stay stable.

```md
1. Write the rule body in .claude/rules/
2. Add/keep a numbered pointer in docs/conventions.md Quick Reference
3. Update the "Related" field on adjacent conventions if relevant
```

**Why:** a stable schema + path-scoped loading makes convention lookup deterministic and cheap.

**Sources:** `AGENTS.md`, handoff-system-v2 migration plan §9.
**Related:** DOC-001, DOC-002.
