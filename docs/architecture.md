# Architecture

## What This Is

Linux desktop application (PySide6/Qt) for backing up and restoring dotfiles. See `README.md` for full human-facing documentation.

## Stack

- **UI:** PySide6 (Qt 6)
- **Package manager:** uv
- **Testing:** pytest
- **Build:** See `packaging/`

## Commands

```bash
# Install (development)
uv sync

# Run tests
uv run pytest

# Run app
uv run dfbu
```
