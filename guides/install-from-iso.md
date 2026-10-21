[← Back to the handbook](../README.md)

# Installing from a USB drive

The Ryoku on NixOS bootable ISO is a **pre-release testing route**, not the everyday recommendation for someone who has never installed Linux.

> **Disk-erasing warning:** The current Ryoku installer ISO erases the **selected disk** and does not offer manual partitioning. If you pick your Windows drive, you can lose Windows and everything stored on it.

## Should you use the Ryoku ISO?

Use it only if you understand disk selection, have a tested backup and are comfortable testing a pre-release installer. For a beginner who wants to preserve an existing Windows setup, starting with the standard NixOS installer and later adding Ryoku is a more conservative approach.

## If you deliberately want to test it

1. Visit the [Ryoku on NixOS releases page](https://github.com/Ryoku-dev/Ryoku-on-NixOS/releases) and read the release notes for the ISO you choose.
2. Download the installation image and follow its published verification instructions when available.
3. Write the image to a disposable USB drive using a trusted imaging tool. **Writing an image overwrites the chosen USB drive.**
4. Boot the target PC from that USB drive using your computer's boot menu.
5. Carefully confirm the **exact drive model and capacity** in the installer before allowing any disk operation.

These are orientation steps, not an assurance that the pre-release installer works on every machine. Don't use a disk containing files you cannot afford to lose.

## What is UEFI?

UEFI is the firmware that starts your computer before Windows or Linux loads. It's not an app you install. The current Ryoku release targets UEFI computers, not old legacy BIOS boot modes.

## What about Secure Boot?

Secure Boot is a firmware protection feature. Ryoku's current ISO has limitations with its unsigned bootloader unless keys have been set up appropriately. Do not disable security settings on an existing important machine just to experiment without understanding the consequences.

## Stuck already?

Return to [Before you install](before-you-install.md) and use the regular NixOS route. You can still get the same Ryoku desktop after installation.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
