# delightful-shell

Terminal workspace config — tmux, zsh, and utilities with Delightful colors.

## Source of Truth

This repo IS the source of truth for its own content. It's ~90% functional tooling (keybinds, aliases, auto-attach) and ~10% Delightful colors (tmux status bar hex values). When this repo and the monorepo copy differ, this repo wins.

## Key Files

- `tmux.conf` — Status bar (Delightful colors), keybinds, session config
- `zshrc-snippet` — Shell aliases, PATH config, Starship init
- `tmux-auto-attach.sh` — Auto-attach/create tmux sessions on terminal launch
- `smart-open` — URL/file opener utility

## Conventions

- Only ~8 hex values in tmux.conf are color-dependent. Everything else is functional config.
- Each file is independently installable — users pick what they want.
