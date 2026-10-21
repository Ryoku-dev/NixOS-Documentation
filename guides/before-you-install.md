[← Back to the handbook](../README.md)

# Before you install

A few minutes of preparation can save hours of confusion later, especially if your current computer still has Windows and everything you care about on it.

## Step 1. Decide what you're installing

There are two different jobs:

- **Installing NixOS** replaces or adds an operating system. Depending on the options you choose, this may erase a disk.
- **Installing Ryoku onto NixOS** changes an existing NixOS configuration. Our recommended installer does **not** partition disks or change your bootloader.

Don't mix these two up. If you're still on Windows, you need a working NixOS installation first, unless you're deliberately testing the separate Ryoku installer ISO.

## Step 2. Back up your important files

Copy your photos, documents, projects, browser recovery information and anything else you cannot replace onto a separate drive or trusted backup service. Check that you can actually open a few files from the backup.

> **Important:** An extra partition on the same drive is not an independent backup. The Ryoku pre-release ISO can erase the disk you select in its installer.

## Step 3. Check your computer

Ryoku on NixOS currently targets modern **64-bit x86 PCs** with **UEFI** firmware. The port supports Hyprland and Niri Wayland sessions.

| Part | What to know |
| --- | --- |
| Processor | 64-bit x86 (`x86_64`), not an ARM laptop |
| Memory | 4 GB is the stated minimum, 8 GB or more is more comfortable |
| Storage | At least 32 GB for the installer target, preferably 64 GB or more |
| Graphics | Needs functioning Linux graphics support with modern rendering |
| Firmware | UEFI. The current installer ISO has Secure Boot limitations |

These are the published project requirements, not a guarantee that every GPU or laptop works perfectly. If unsure, test the operating system before replacing your main installation.

## Step 4. Choose a sensible first experiment

- **Safest for learning:** Try ordinary NixOS in a virtual machine or on a spare computer. Graphics-heavy Wayland desktops may be slower or behave differently in a VM.
- **Best for a real desktop:** Use a dedicated spare SSD so the Windows drive can remain untouched.
- **Existing flake-based NixOS:** Go straight to the [Ryoku guided installer](install-on-nixos.md).
- **Experimental Ryoku ISO:** Read the [specific ISO warning](install-from-iso.md) first.

## Step 5. Know how to get help

Keep a second device handy so you can read troubleshooting instructions if your desktop cannot open. Join the [Ryoku Discord](https://discord.gg/xvr69NRsmt) if you need help from other users.

## Next

Ready and already on NixOS? Follow [Install on NixOS](install-on-nixos.md). Still on Windows? Use the [official NixOS manual](https://nixos.org/manual/nixos/stable/#sec-installation) to install the operating system before moving on.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
