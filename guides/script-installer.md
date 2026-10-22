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

# Installing from a USB drive

The Ryoku on NixOS bootable ISO that automatically installs NixOS aswell as the entire Ryoku shell and comes preinstalled with premade NixOS configs and flake.nix inputs and they are heavily commented to make editing extremely easy.

    Disk-erasing warning: The current Ryoku installer ISO erases the selected disk and does not offer manual partitioning unless you do it manually in a TTY session first or use Disk Manager on Windows. If you pick your Windows drive without partitioning first, you will lose Windows and everything stored on it.

How to get the .iso

    Visit the Ryoku on NixOS releases page and read the release notes for the ISO you choose.
    Download the installation image and follow its published verification instructions when available.
    Make sure the SHA256/ hash matches if you want to be extra safe
    Write the image to a disposable USB drive using a trusted imaging tool such as Rufus. Writing an image wipes any data on the USB drive.
    Boot the target PC from that USB drive using your computer's boot menu.
    Carefully confirm the exact drive model and capacity in the installer before allowing any disk operation.
    Select your options
    Install
    Reboot ensuring the USB isnt set to the highest boot priority or just remove the USB entirely to avoid this

What is UEFI?

UEFI is the firmware that starts your computer before Windows, MacOS, BSD or Linux loads. It's not an app you install. The current Ryoku release targets UEFI computers, not old legacy BIOS boot modes.
What about Secure Boot?

Secure Boot is a firmware protection feature. Ryoku's current ISO has limitations with its unsigned bootloader unless keys have been set up appropriately. Turning off Secure Boot before booting the .iso is the correct way to boot it.
Stuck already?

Return to Before you install and use the regular NixOS route. You can still get the same Ryoku desktop after installation.

## After installation

When the build and switch have succeeded, log out and choose **Hyprland** or **Niri** from your login screen, then sign in. You should see Ryoku's desktop and panels.

If anything looks unfamiliar, follow [Your first 10 minutes](first-boot.md). If the session fails to open, use [troubleshooting](troubleshooting.md).

## Non-standard setups

Custom flake paths and multi host installations need different arguments. See the repos [authoritative NixOS guide](https://github.com/Ryoku-dev/Ryoku-on-NixOS/blob/main/docs/nixos.md) 

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
