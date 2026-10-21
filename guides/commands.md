[← Back to the handbook](../README.md)

# Commands that matter

You do **not** need to type all of these. This is a reference for when a guide tells you to use one.

> **Read first:** Commands can change your system. Anything using `sudo` has elevated privileges. Only run a command when you know what machine and configuration it applies to.

## Directory & Files

```bash
pwd
```
pwd means "print working directory" and prints out the current directory your terminal is in.

```bash
ls
```
ls means "list" and lists all files within its current directory.

```bash
cat 
```
cat means "paste whats in this file" and the entire file you specify in the terminal gets printed.

```bash
cd
```
cd means "change directory' and moves your terminal to the directory you list.

## See your system history

```bash
sudo nixos-rebuild list-generations
```
Lists the system generations NixOS knows about.

## Check a flake

```bash
nix flake check /etc/nixos
```
Runs flake checks. It can take time and may build packages. It does not activate a new operating system generation.

## Build without activating

```bash
sudo nixos-rebuild build --flake /etc/nixos#my-host
```
Builds the named NixOS configuration. Replace `my-host` with your real configuration name which is `nixos` by default. The build itself does not activate that system.

## Test without changing the default boot generation

```bash
sudo nixos-rebuild test --flake /etc/nixos#my-host
```
Activates the named configuration for testing, but does not make it your default boot choice. **This still changes the live running system**, so save your work first.

## Apply a configuration

```bash
sudo nixos-rebuild switch --flake /etc/nixos#my-host
```
Builds and activates the named configuration and makes it the default for later boots. Read [Updates and rebuilds](updates.md) before using it.

## Update Ryoku on an installer-managed system

```bash
ryoku update
```
Uses the Ryoku Nix update backend. Custom local path flake setups follow a different update path.

## Inspect Ryoku's shell if something is broken

```bash
systemctl --user status ryoku-shell.service
```
Shows whether the Ryoku shell service is running.

```bash
journalctl --user -u ryoku-shell.service -b --no-pager -n 80
```
Shows recent Ryoku shell log messages from this boot. These commands only inspect state.

## Where to learn more

The [NixOS manual](https://nixos.org/manual/nixos/stable/) explains the system in more depth. Our [glossary](glossary.md) translates unfamiliar words.

---

[← All topics](../README.md) · [Still stuck? Get help](troubleshooting.md)
