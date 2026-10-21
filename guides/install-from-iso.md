[← Back to the handbook](../README.md)

# Installing from a USB drive

The Ryoku on NixOS bootable ISO that automatically installs NixOS aswell as the entire Ryoku shell and comes preinstalled with premade NixOS configs and flake.nix inputs and they are heavily commented to make editing extremely easy.

> **Disk-erasing warning:** The current Ryoku installer ISO erases the **selected disk** and does not offer manual partitioning unless you do it manually in a TTY session first or use Disk Manager on Windows. If you pick your Windows drive without partitioning first, you will lose Windows and everything stored on it.

## How to get the .iso

1. Visit the [Ryoku on NixOS releases page](https://github.com/Ryoku-dev/Ryoku-on-NixOS/releases) and read the release notes for the ISO you choose.
2. Download the installation image and follow its published verification instructions when available.
3. Make sure the SHA256/ hash matches if you want to be extra safe
4. Write the image to a disposable USB drive using a trusted imaging tool such as Rufus. **Writing an image wipes any data on the USB drive.**
5. Boot the target PC from that USB drive using your computer's boot menu.
6. Carefully confirm the **exact drive model and capacity** in the installer before allowing any disk operation.
7. Select your options
8. Install
9. Reboot ensuring the USB isnt set to the highest boot priority or just remove the USB entirely to avoid this

## What is UEFI?

UEFI is the firmware that starts your computer before Windows, MacOS, BSD or Linux loads. It's not an app you install. The current Ryoku release targets UEFI computers, not old legacy BIOS boot modes.

## What about Secure Boot?

Secure Boot is a firmware protection feature. Ryoku's current ISO has limitations with its unsigned bootloader unless keys have been set up appropriately. Turning off Secure Boot before booting the .iso is the correct way to boot it.

## Stuck already?

Return to [Before you install](before-you-install.md) and use the regular NixOS route. You can still get the same Ryoku desktop after installation.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
