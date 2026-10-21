[← Back to the handbook](../README.md)

# Words explained simply

You do not need a computer science degree to read a Linux guide. Here are the words most likely to get in your way.

## NixOS

The operating system underneath Ryoku. Think of it as the part that does the job Windows normally does.

## Ryoku

The desktop environment and connected tools you see and interact with on top of NixOS.

## Terminal

An app where you type commands instead of clicking through menus. **PowerShell** is a similar idea on Windows.

## Command

A written instruction for your computer. `pwd`, for example, asks the terminal to show the folder you're in.

## Package

An application or another piece of software. Firefox is a package, but background tools can be packages too.

## Configuration

The settings that describe what your computer should have and how it should behave.

## Declarative

You describe the end result you want rather than manually applying each change one at a time. NixOS then works towards that declared result when you rebuild.

## Flake

A Nix project definition that connects configuration and dependency versions. The `flake.nix` file says what to build, and `flake.lock` records the specific dependency revisions used.

## Rebuild

A NixOS process that turns your configuration into an actual system setup.

## Generation

A saved version of your NixOS system configuration. Generations can be useful when returning to a setup that worked, but **they are not backups of your personal files**.

## Window manager

The part that arranges and moves windows. Ryoku supports **Hyprland** and **Niri**.

## Wayland

The display system used by Ryoku. It helps applications draw their windows and interact with your mouse and keyboard.

## Shell

Depending on context, either the **terminal's command interpreter** (such as Fish or Zsh) or the **graphical Ryoku shell** that draws desktop components. Same word, different jobs. Naturally, computers thought this would be clear.

## RyoStore

A catalogue of Ryoku themes and customisation products. It is not the same thing as NixOS's package manager.

## ISO

An image file used to make bootable installation media, usually a USB drive.

## Bootloader

The menu or program that starts the operating system when you turn your PC on.

## Root / sudo

Administrator-level access. `sudo` runs a command with elevated permissions. Don't paste an unknown `sudo` command simply because an online comment recommends it.

## More questions?

Read the [FAQ](faq.md) or head back to [Start here](start-here.md).

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
