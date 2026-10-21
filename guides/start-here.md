[← Back to the handbook](../README.md)

# Start here

Welcome to **Ryoku on NixOS**. This guide assumes you have never used Linux and you do not have to memorise commands or even use a Terminal that much

## What exactly is Ryoku?

Think of your computer as three parts:

- **NixOS** is the operating system. It does the job Windows, MacOS or other Linux disro does, it starts the computer, manages hardware and runs programs.
- **Ryoku** is the desktop you use on top of NixOS, the panels, app launcher, settings, wallpapers and connected tools.
- **Your configuration** is a set of instructions telling NixOS what your system should contain.

Ryoku on NixOS is not a Windows application. You cannot double-click an `.exe` file to install it on Windows.

## Pick the path that describes you

### “I'm using Windows right now”

Start with [Before you install](before-you-install.md). It will guide you on how to back up your files and decide whether to try NixOS on a spare drive, a spare computer or with a virtual machine.

For most first time users, the safest learning route is to install ordinary NixOS first, then add Ryoku once NixOS is working and configured with a flake. See the [official NixOS installation manual](https://nixos.org/manual/nixos/stable/#sec-installation) for the operating-system installation steps.

### “NixOS is already installed on my PC”

If you already have **flake-based NixOS**, use our [guided Ryoku installer](install-on-nixos.md). It adds Ryoku to the system you have without removing anything.

If you do not know whether your NixOS configuration uses a flake, read the [glossary](glossary.md) before running anything.

### “Ryoku is installed but I'm lost”

Open [Your first 10 minutes](first-boot.md). It walks through the desktop, settings and launcher without assuming you know Linux keyboard shortcuts.

### “Something has gone wrong”

Use [Fix common problems](troubleshooting.md) first. If a recent update or rebuild is responsible, read [Go back to a working system](recovery.md).

## Where to go next

Continue to [Before you install](before-you-install.md), or explore [all the unfamiliar words](glossary.md) at your own pace.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
