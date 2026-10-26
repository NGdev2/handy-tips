# Claude Code: moving fast through long conversations

These tips apply when Claude Code runs in **fullscreen** mode (`"tui": "fullscreen"` in `~/.claude/settings.json`). In that mode Claude scrolls the conversation itself, so the terminal's own scrollbar and keys (Wave's `Shift+Home`, `Shift+PageUp`, `Ctrl+F` search) don't reach it.

Run `/tui` to check which mode is active.

## Keys on my laptop (ASUS TUF F15, French keyboard)

PgUp, PgDn, Home and End have no keys of their own. They are second labels on the arrow keys and work while holding `Fn`. Plain arrows only go through the prompt history.

| Key | Arrow key + `Fn` | Number pad (Num Lk **off**) |
|---|---|---|
| PgUp | `Fn` + `↑` | `9` |
| PgDn | `Fn` + `↓` | `3` |
| Home | `Fn` + `←` | `7` |
| End (labelled **FIN**) | `Fn` + `→` | `1` |

## Jumping

| Action | Keys |
|---|---|
| Scroll up / down half a screen | `Fn` + `↑` / `Fn` + `↓` |
| Jump to the start of the conversation | `Ctrl` + `Fn` + `←` (or `Ctrl` + numpad `7`) |
| Jump to the latest message and follow new output again | `Ctrl` + `Fn` + `→` (or `Ctrl` + numpad `1`) |

Without the keyboard:
- While scrolled up, a **dim row at the top** shows the last prompt above the view. Click it to jump to that prompt.
- A **Jump to bottom** button appears at the bottom edge while scrolled up. Scrolling all the way down also resumes following.

## Faster mouse wheel

Run `/scroll-speed` inside Claude:
- Scroll while the dialog is open to feel the speed.
- `←` / `→` to change it (up to 10), `r` to reset, `Enter` to save.
- `3` feels like `vim`; 5–10 is good for long sessions.

It saves to `~/.claude/settings.json`. The environment variable `CLAUDE_CODE_SCROLL_SPEED` sets the same value (up to 20).

## Transcript mode: fastest for very long sessions

Press `Ctrl+o` to enter, `q` or `Esc` to leave.

| Key | Action |
|---|---|
| `g` / `G` | Top / bottom |
| `{` / `}` | Previous / next prompt (jumps between my messages) |
| `/` then `n` / `N` | Search, then next / previous match |
| `Space` / `b` | One page down / up |
| `[` | Copy the whole conversation into the terminal's normal scrollback, so the terminal's own search works on it |

Source: https://code.claude.com/docs/en/fullscreen.md
