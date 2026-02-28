# Shell — Delightful Config

Shared Starship prompt and zsh config using Delightful Design System colors. Works with any terminal (Ghostty, iTerm2, etc.).

Part of the [Delightful Design System](https://github.com/kylesnav/delightful-design-system).

## Contents

```
starship.toml       Starship prompt config using Delightful colors
zshrc-snippet       Zsh additions (starship, aliases, hooks)
smart-open          iTerm2 semantic history handler (Cmd+click files)
```

## Install

The fastest way to set up shell config (along with your terminal theme) is the [setup script](https://github.com/kylesnav/delightful-design-system/blob/main/scripts/setup-terminal.sh) in the monorepo.

Or install manually:

### Starship Prompt

```bash
brew install starship
cp starship.toml ~/.config/starship.toml
```

Add `eval "$(starship init zsh)"` to your `~/.zshrc`, or use the full `zshrc-snippet`.

### Zsh Snippet

Copy the snippet into your `~/.zshrc`, or source it:

```bash
source /path/to/zshrc-snippet
```

### smart-open (iTerm2)

Routes Cmd+click file paths to the right app: directories to Finder, HTML to Chrome, code files to VS Code (with line number support), images and PDFs to Preview.

```bash
cp smart-open ~/.local/bin/smart-open
chmod +x ~/.local/bin/smart-open
```

Then in iTerm2: Settings → Profiles → Advanced → Semantic History → "Run command...":

```
/Users/YOU/.local/bin/smart-open \1 \2 \5
```

## What's Included

### Starship Prompt

Two-line prompt using Delightful accent colors:

| Element | Color | Details |
|---------|-------|---------|
| `>` prompt character | Pink (`#f600a3`) | Red on error, cyan in vim mode |
| Directory | Bold foreground | Truncated to 3 levels |
| Git branch | Pink | |
| Git status | Gold | Modified, staged, untracked indicators |
| Node / Python / Rust | Green / Gold / Red | Shown when in a project directory |
| Command duration | Muted | Shown for commands over 2 seconds |
| Clock | Muted | Right-aligned, HH:MM |

### Zsh Snippet

| Feature | Details |
|---------|---------|
| Quick terminal hook | Auto-launches Claude Code on `Option+Space` (Ghostty 1.3+) |
| `AUTO_CD` | Type a directory name to cd into it |
| `CORRECT` | Spell correction for mistyped commands |
| History | 50k entries, shared across sessions, no duplicates |
| Tab completion | Case-insensitive, menu-selectable |
| `c` | Alias for `claude` |
| `cc` | Alias for `claude --dangerously-skip-permissions` |
| `cr` | Alias for `claude --resume` |

All aliases clear the command line before launching.

Tip: `touch ~/.hushlogin` to suppress the macOS "Last login" message.

## References

| Tool | Repo | Docs |
|------|------|------|
| Starship | [starship/starship](https://github.com/starship/starship) | [starship.rs](https://starship.rs) |
| Zsh | [zsh-users/zsh](https://github.com/zsh-users/zsh) | [zsh.sourceforge.io](https://zsh.sourceforge.io/Doc/) |

## Related

- [delightful-ghostty](https://github.com/kylesnav/delightful-ghostty) — Ghostty terminal theme
- [obsidian-delightful](https://github.com/kylesnav/obsidian-delightful) — Obsidian theme
- [delightful-design-system](https://github.com/kylesnav/delightful-design-system) — Full design system monorepo
