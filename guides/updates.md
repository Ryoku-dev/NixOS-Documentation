[← Back to the handbook](../README.md)

# Updates and rebuilds

Updates are less scary once you know what NixOS is doing behind the scenes.

## The simple version

A **rebuild** takes the settings you've declared, prepares the matching packages and activates that system setup. A **generation** is a saved version of that setup.

This doesn't mean every file on your computer is saved. Personal documents are not backed up by a NixOS generation.

## Updating Ryoku

On an ordinary installer managed Ryoku on NixOS setup, the native updater is:

```bash
ryoku update
```

**What it does:** The NixOS update backend advances the configured Ryoku flake input, builds a new system generation and switches to it if the process succeeds. It does not use Pacman, DNF, XBPS, APT or any non native NixOS package manager.

If your flake uses a local path the updater intentionally leaves that source alone. Such setups should update their local checkout and rebuild through their own workflow.

## Applying your own NixOS changes

For a typical flake stored in `/etc/nixos/flake.nix`, an example is:

```bash
sudo nixos-rebuild switch --flake /etc/nixos#my-host
```

Replace `my-host` with **your actual NixOS configuration name**. It isn't meant to be typed literally.

- `sudo` - run the command with administrator privileges.
- `nixos-rebuild` - build and activate a NixOS system configuration.
- `switch` - make the new configuration active now and use it by default on future boots.
- `--flake /etc/nixos#my-host` - choose the configuration to build.

> **WARNING** `switch` changes your active system. Make a configuration backup and review edits first. Builds may fail, which is useful feedback rather than a reason to blindly delete files.

## Previewing or testing

`nixos-rebuild build` builds a system without activating it. `nixos-rebuild test` activates a system without making it the default boot choice. These are useful for more cautious workflows. See the [official rebuild documentation](https://wiki.nixos.org/wiki/Nixos-rebuild).

## If an update causes a problem

Dont make unrelated changes. Go to [Recovery](recovery.md) and return to a known working generation if needed.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
