[← Back to the handbook](../README.md)

# Fix common problems

**Start here:** run `ryoku doctor` before trying anything else.

```bash
ryoku doctor --check
```

**What it does:** Checks your setup for common issues and reports what it finds. Run this first, since it may point you straight to the fix.

## Ryoku doesn't appear at the login screen

- Check that the guided installer completed its build and switch, not just the initial download.
- Confirm you're looking for the session choices at your display manager, such as Hyprland or Niri.
- If your login screen behaves unexpectedly, don't reinstall the whole operating system as your first step.

## Login returns immediately to the login screen

A session may be crashing before the desktop finishes loading. If you can switch to a text console (TTY) with ctrl + alt + F key, check the relevant user service and session logs rather than repeatedly signing in.

```bash
systemctl --user status ryoku-shell.service
```

**What it does:** Displays the current status of Ryoku's user-level shell service. It does not restart or modify it.

```bash
journalctl --user -u ryoku-shell.service -b --no-pager -n 80
```

**What it does:** Shows the latest 80 error log lines for Ryoku's shell service from the current boot. An error mentioning a QML file and line number can be particularly useful.

## Your compositor starts, but Ryoku doesn't

If Hyprland or Niri loads but you get a bare session without Ryoku, the Ryoku services may not be enabled. Try running:

```bash
systemctl --user enable --now ryoku-shell ryogami ryoku-session.target
sudo reboot
```

**What it does:** Enables and starts the Ryoku shell, Ryogami and the Ryoku session target for your user, then reboots so the session starts cleanly.

## The desktop loads, but a launcher or panel is missing

- Check the option you've selected in Ryoku Hub.
- If you recently installed a bar or launcher product, confirm that it is installed rather than merely visible in a catalogue.
- Reload the relevant Ryoku component only after checking the logs. On NixOS, avoid making manual copies into immutable Nix store paths.

## No sound or an audio device is missing

Check whether the device appears in your audio settings. USB headsets may fail for firmware or pairing reasons even if PipeWire is working. Avoid reinstalling audio services before checking whether the hardware is recognised.
If pipewire is failing the fix for that is 
```bash
systemctl --user restart pipewire pipewire-pulse wireplumber
```
Then just reset the affected apps after running this command.

## The display is black, flickering or wrong-sized

Graphics drivers, Wayland compatibility matter. Record the GPU model, monitor connection and whether the problem occurs in Hyprland, Niri or both.

## What to include in a useful report

1. NixOS version and GPU model.
2. Hyprland or Niri.
3. What you expected and what happened instead.
4. Whether this started after an update or a setting change.
5. The smallest relevant error excerpt, with private details removed.

Report issues in the [Ryoku on NixOS repository](https://github.com/Ryoku-dev/Ryoku-on-NixOS/issues) or ask in [Discord](https://discord.gg/xvr69NRsmt).

## Still stuck?

If it started immediately after a system update, go to [Recovery](recovery.md) before trying anything destructive.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
