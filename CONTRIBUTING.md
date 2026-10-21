# Contributing to the Ryoku on NixOS handbook

[← Back to the handbook](README.md)

These guides are for everyone, including someone who has never used Linux.

## What makes a good guide?

- Write like the reader is coming from Windows or something like Linux Mint/ ZorinOS, without sounding patronising.
- Explain **what a command does** and **what it changes** before asking anyone to run it.
- Warn clearly about disk erasure, `sudo`, reboots etc and steps that are difficult to undo.
- Keep guides short, with useful links instead of repeating the same explanation everywhere.
- When a project specific behaviour changes, verify it in the [Ryoku on NixOS source repository](https://github.com/Ryoku-dev/Ryoku-on-NixOS).
- Never use Arch, Fedora, Void, Ubuntu logic and filepaths and assume it works on NixOS.

## Add or edit a topic

1. Edit the relevant Markdown file in guides/ or add a new one.
2. Link it in the main README.md topic.
3. Check its links, commands, and warnings.
4. Make sure the guide links back to ../README.md.

This repo is written entirely in markdown with a few assets located in /assets.

## Getting help

If an instruction is outdated, report it in the [NixOS documentation repository](https://github.com/Ryoku-dev/NixOS-Documentation/issues). For a bug in Ryoku itself, use the [NixOS port issues](https://github.com/Ryoku-dev/Ryoku-on-NixOS/issues).
