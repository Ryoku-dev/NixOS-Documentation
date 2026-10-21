[← Back to the handbook](../README.md)

# Questions people have actually asked

## Can I install Ryoku from Windows by opening an `.exe`?

No. Ryoku on NixOS is a Linux desktop, not a Windows application. If you're on Windows, read [Before you install](before-you-install.md) first.

## Will it delete Windows?

The **guided Ryoku installer for an existing NixOS system** does not format disks or install a new operating system. The separate .iso erases the disk you select. These are different processes. See [The installer USB](install-from-iso.md).

## Do I have to know how to code?

No. You can use the desktop and personalise much of it through Ryoku Hub and RyoStore. Understanding a few configuration basics becomes useful when you want to manage system packages or customise NixOS itself.

## What is a flake, and why does the installer need one?

A flake describes your Nix configuration and records the revisions of its dependencies. The guided Ryoku installer currently targets an **existing flake-based NixOS installation**. Read [Words explained simply](glossary.md).

## Is NixOS the same as Arch Linux?

No. Ryoku aims to provide the same desktop experience on both, but Arch uses Pacman and its own system tools while NixOS uses Nix packages and declarative system configurations.

## Which is better, Hyprland or Niri?

Neither is universally better. Both are tiling window managers, and Ryoku supports both. Choose whichever layout you prefer, then learn it gradually.

## Can I use NVIDIA graphics?

The port aims to support supported Linux graphics hardware, including NVIDIA systems, but a particular card and driver setup may need additional NixOS configuration. The guided Ryoku installer does not take ownership of your existing graphics driver configuration. Check your hardware before assuming everything will work.

## Can I undo an update?

NixOS often keeps older system generations that can be selected during boot or used for recovery. They're not a substitute for personal file backups. Read [Recovery](recovery.md).

## How do I update Ryoku?

For a standard installer managed setup, use `ryoku update`. See [Updates and rebuilds](updates.md) for what that does and when to use NixOS rebuild commands instead.

## Where can I ask for help?

Use the [Ryoku Discord](https://discord.gg/xvr69NRsmt) (recommended) or [open an issue](https://github.com/Ryoku-dev/Ryoku-on-NixOS/issues) with your hardware, steps to reproduce and an exact error message. Hide passwords, tokens and other private information from screenshots and logs.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
