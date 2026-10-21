[← Back to the handbook](../README.md)

# Install Ryoku on NixOS

This is the recommended route when **NixOS is already installed** and you use a **flake-based NixOS configuration**.

## Before touching anything

1. Make sure your NixOS machine can connect to the internet, use tools like `nmtui, nmcli or iwctl` if not.
2. Have a working backup of your NixOS configuration and important personal files.
3. Confirm that your `/etc/nixos` configuration uses a `flake.nix`. If you use a custom flake in another directory, use the advanced option in the upstream guide.
4. Open a terminal. It is the app where you type commands, a bit like PowerShell on Windows.

## Open the guided installer

Paste this command **without `sudo`**:

```bash
nix run github:aethctl/Ryoku-on-NixOS/main#install
```

**What it does:** Nix downloads the Ryoku installer from the NixOS repo and opens an interactive setup screen. It does not format your disk.

The installer asks you to choose:

- **Window manager:** Hyprland or Niri. Both control where app windows appear.
- **Browser:** Chromium or Firefox.
- **Shell:** Fish or Zsh. This mostly affects the experience inside the terminal, this can be changed at any point with `chsh -s`
- **Optional apps:** Extra tools you can choose to include or leave out.

Use the arrow keys to move, **Enter** to continue, **Space** to tick options, and **Esc** to go back. Read the final review before continuing.

## What changes on your computer?

The installer integrates the Ryoku flake input and module into your existing NixOS setup, writes its managed `ryoku.nix`, updates the lock file and builds a new NixOS generation and it only switches to the new generation when the build succeeds. It keeps installer configuration backups under `/var/backups/ryoku-nixos/`.

## After installation

When the build and switch have succeeded, log out and choose **Hyprland** or **Niri** from your login screen, then sign in. You should see Ryoku's desktop and panels.

If anything looks unfamiliar, follow [Your first 10 minutes](first-boot.md). If the session fails to open, use [troubleshooting](troubleshooting.md).

## Non-standard setups

Custom flake paths and multi host installations need different arguments. See the repos [authoritative NixOS guide](https://github.com/Ryoku-dev/Ryoku-on-NixOS/blob/main/docs/nixos.md) 

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
