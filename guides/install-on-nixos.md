[← Back to the handbook](../README.md)

# Install Ryoku on NixOS

This is the recommended route when **NixOS is already installed** and you use a **flake-based NixOS configuration**.

> **Not on NixOS yet?** Go to [Before you install](before-you-install.md). Running this command in PowerShell or Command Prompt on Windows will not install Ryoku.

## Before touching anything

1. Make sure your NixOS machine can connect to the internet.
2. Have a working backup of your NixOS configuration and important personal files.
3. Confirm that your `/etc/nixos` configuration uses a `flake.nix`. If you use a custom flake elsewhere, use the advanced option in the upstream guide.
4. Open a terminal. It is the app where you type commands, a bit like PowerShell on Windows.

## Open the guided installer

Paste this command **without `sudo`**:

```bash
nix run github:aethctl/Ryoku-on-NixOS/main#install
```

**What it does:** Nix downloads the Ryoku installer from the maintained NixOS port and opens an interactive setup screen. It does not format your disk.

The installer asks you to choose:

- **Window manager:** Hyprland or Niri. Both control where app windows appear.
- **Browser:** Chromium or Firefox.
- **Shell:** Fish or Zsh. This mostly affects the experience inside the terminal.
- **Optional apps:** Extra tools you can choose to include or leave out.

Use the arrow keys to move, **Enter** to continue, **Space** to tick options, and **Esc** to go back. Read the final review before continuing.

## Want to preview first?

You can open the installer in dry-run mode:

```bash
nix run github:aethctl/Ryoku-on-NixOS/main#install -- --dry-run
```

**What it does:** The installer shows the configuration changes its backend proposes instead of applying its normal final transaction.

## What changes on your computer?

The installer integrates the Ryoku flake input and module into your existing NixOS setup, writes its managed `ryoku.nix`, updates the lock file and builds a new NixOS generation. It only switches when the build succeeds. It keeps installer configuration backups under `/var/backups/ryoku-nixos/`.

The installer does **not** choose a new disk layout, wipe Windows, replace your bootloader or take over your GPU driver configuration.

## After installation

When the build and switch succeed, log out and choose **Hyprland** or **Niri** from your login screen, then sign in. You should see Ryoku's desktop and panels.

If anything looks unfamiliar, follow [Your first 10 minutes](first-boot.md). If the session fails to open, use [troubleshooting](troubleshooting.md).

## Non-standard setups

Custom flake paths and multi-host installations need different arguments. See the port's [authoritative NixOS guide](https://github.com/Ryoku-dev/Ryoku-on-NixOS/blob/main/docs/nixos.md) rather than copying somebody else's machine name into a command.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
