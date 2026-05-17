# delightful-shell

Terminal workspace configuration: tmux, zsh additions, persistent tmux auto-attach, and iTerm2 smart-open.

## Source of Truth

This repo is the source of truth for its own tooling. Most files are functional shell configuration; only the tmux status bar palette depends on Delightful colors.

## Validate

```sh
bash -n tmux-auto-attach.sh
bash -n smart-open
test -x tmux-auto-attach.sh
test -x smart-open
```

For `tmux.conf`, inspect syntax and key bindings manually unless tmux is available for a live load check.

## Editing Rules

- Keep each file independently installable.
- Never claim this repo owns the Starship prompt config; that belongs to `delightful-starship`.
- Preserve user-local shell safety: docs should source snippets or copy individual files, not replace whole dotfiles.
- Keep `smart-open` conservative: if a path cannot be resolved, exit quietly.

## Screenshots

Screenshots can show the full terminal stack, but alt text and captions must say whether the image is demonstrating tmux, Starship, or the combined terminal experience.
