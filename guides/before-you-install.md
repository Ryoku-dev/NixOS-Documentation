[← Back to the handbook](../README.md)

# Before you install

A few minutes of preparation can save hours of confusion later, especially if your current computer still has Windows and everything you care about on it.

## Step 1. Decide what you're installing

There are two different jobs:

- **Installing NixOS** replaces or adds an operating system. Depending on the options you choose, this may erase a disk.
- **Installing Ryoku onto NixOS** changes an existing NixOS configuration. Our recommended installer does **not** partition disks or change your bootloader.

Don't mix these two up. If you're still on Windows, you need a working NixOS installation first, unless you're using the separate Ryoku installer ISO.

## Step 2. Back up your important files

Copy your photos, documents, projects, browser recovery information and anything else you cannot replace onto a separate drive or trusted backup service as if you are completely erasing Windows, these files will be gone forever unless you are formatting in NTFS which is only recommended for experienced users and isn't covered here in any of this documentation.

> **Important:** An extra partition on the same drive is not an independent backup. The Ryoku ISO will erase the disk you select in its installer. Manual partitioning can be done via Disk Manager on Windows and a TTY session before the .iso installation.

## Step 3. Check your computer

Ryoku on NixOS currently targets modern **64-bit x86 PCs** with **UEFI** firmware. The repo supports Hyprland and Niri Wayland sessions. Below are the recommended specs for a PC/ Laptop to be able to run Ryoku at 1080p with animations, blur etc with enough headroom to comfortably do other things on the PC. NixOS' recommended specs are alot lower however, Ryoku is a full feature rich shell that was made for modern and powerful PC's.

| Part | Minimum | Recommended |
| --- | --- | --- |
| Processor | R3 2200G, i3 8th Gen | R5 5500G, i5 10th Gen |
| Memory | 8GB DDR4 | 16GB DDR4 |
| Storage | 64GB SSD | 128GB SSD |
| Graphics | GTX 1060, RX 560 | GTX 1660, Raedon 680M |
| Firmware | UEFI | UEFI |



## Step 4. Choose a sensible first experiment

- **Safest for learning:** Try ordinary NixOS in a virtual machine or on a spare computer. Graphics heavy Wayland desktops may be slower or behave differently in a VM.
- **Best for a real desktop:** Use a dedicated spare SSD so the Windows drive can remain untouched if you intend on dual booting.
- **Existing flake-based NixOS:** Go straight to the [Ryoku guided installer](install-on-nixos.md).
- **Ryoku ISO:** Read the [.iso install](install-from-iso.md) first.

## Step 5. Know how to get help

Keep a second device handy like a mobile phone etc so you can read troubleshooting instructions if your desktop cannot open. Join the [Ryoku Discord](https://discord.gg/xvr69NRsmt) if you need help from the projects developers, maintainers and contributors.

## Next

Ready and already on NixOS? Follow [Install on NixOS](install-on-nixos.md). Still on Windows? Use the [official NixOS manual](https://nixos.org/manual/nixos/stable/#sec-installation) to install the operating system before moving on.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
