[← Back to the handbook](../README.md)

# Apps and software

Installing an application on NixOS is a little different from double-clicking a Windows `.exe` installer.

## Where do apps come from?

- **Ryoku's selected applications:** The guided installer can enable or disable supported optional tools through its NixOS configuration.
- **Nixpkgs:** A large collection of software packaged for NixOS.
- **Flatpak:** A separate app packaging system used by many desktop applications, when Flatpak support is enabled.
- **Ryostore:** Mainly Ryoku customisations such as themes, bars and launchers. Don't assume every store item is a system package.

## What is a package?

A package is simply an app or a piece of software your choose to download. NixOS stores packages in managed locations so different system generations can use compatible sets.

## How do I keep an app installed?

For applications you want managed along with your operating system, use your NixOS configuration found in `etc/nixos/configuration.nix` by default. Typical system package additions looks like this:

```nix
environment.systemPackages = with pkgs; [
  firefox
  obs-studio
  other apps etc.
];
```

**What it means:** “Include Firefox and other installed apps whenever NixOS builds this configuration.” This is an example, not an instruction to paste this block into ant file. If your configuration already defines `environment.systemPackages`, add an item to its existing list rather than defining the option twice.

After editing a system configuration, a rebuild activates the change. See [Commands that matter](commands.md) for the rebuild commands.

## How is this different from Windows?

On Windows, apps are often installed one by one using setup programs. On NixOS, you can describe the apps you want in your configuration and recreate that selection when rebuilding the system.

You don't have to master the Nix programming language on day one. Use Ryoku's installed apps and learn one change at a time.

## Need a particular app?

Search the [official NixOS package search](https://search.nixos.org/packages) before trusting commands from unrelated tutorials. Some applications need extra hardware support, services or configuration.

## Next

Understand [updates](updates.md), or look up the unfamiliar words in the [glossary](glossary.md).

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
