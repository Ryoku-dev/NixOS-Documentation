# Contributing to the Ryoku on NixOS handbook

[← Back to the handbook](README.md)

These guides are for everyone, including someone who has never used Linux.

## What makes a good guide?

- Write as though the reader is coming from Windows, without talking down to them.
- Explain **what a command does** and **what it changes** before asking anyone to run it.
- Warn clearly about disk erasure, `sudo`, reboots, and steps that are difficult to undo.
- Keep guides short, with useful links instead of repeating the same explanation everywhere.
- When a project-specific behaviour changes, verify it in the [Ryoku on NixOS source repository](https://github.com/Ryoku-dev/Ryoku-on-NixOS).
- Never substitute Arch Linux commands for NixOS equivalents.

## Add or edit a topic

1. Edit the relevant Markdown file in `guides/` or add a new one.
2. Link it in the main `README.md` topic index.
3. Check its links, commands, and warnings.
4. Make sure the guide links back to `../README.md`.

There are no website builds or npm dependencies. GitHub renders Markdown itself.

## Getting help

If an instruction is outdated, report it in the [NixOS documentation repository](https://github.com/Ryoku-dev/NixOS-Documentation/issues). For a bug in Ryoku itself, use the [NixOS port issues](https://github.com/Ryoku-dev/Ryoku-on-NixOS/issues).
