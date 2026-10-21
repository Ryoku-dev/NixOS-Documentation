[← Back to the handbook](../README.md)

# Go back to a working system

NixOS generations are one of the nicest things about the platform. If a new system configuration causes trouble, an older generation may still work.

## What is a generation?

Picture a row of saved operating-system setups. A generation remembers which system packages and settings were built together. It isn't a replacement for backing up your personal files.

## If the desktop still works

If you can open a terminal, first record what changed. You can see system generations with:

```bash
sudo nixos-rebuild list-generations
```

**What it does:** Lists known NixOS system generations. It does not change the system.

You can often restore a previous system configuration using the appropriate NixOS generation or bootloader entry. The exact recovery command depends on how the current machine is set up.

## If you cannot reach the desktop

1. Shut down safely if possible.
2. On startup, open your machine's **boot menu** or the NixOS bootloader menu.
3. If previous NixOS generations are offered, choose the last one you know worked.
4. Once logged in, inspect the recent changes before doing another system rebuild.

The menu's appearance and keys vary by bootloader. Do not assume every NixOS installation uses the same bootloader.

## What a generation cannot fix

A previous generation does not restore accidentally deleted personal photos, an erased partition or data on a failed drive. Keep real backups separately.

## Avoid these panic fixes

Don't run commands that delete the Nix store, remove boot entries, wipe configuration folders or erase old generations just because a web post suggests it. Those may eliminate useful recovery options.

## Need help collecting evidence?

Read [Fix common problems](troubleshooting.md) and share the exact error, your last change and whether an older generation works. Redact tokens, passwords and private information from logs.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
