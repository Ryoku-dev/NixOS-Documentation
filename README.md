<div align="center">

<img src="assets/ryoku-nix-logo-white-transparent.svg" alt="力と美" width="260" />

<br />

**力と美のために**  ·  For the sake of power and beauty

### Your Ryoku on NixOS handbook

Everything you need to go from *“What even is NixOS?”* to feeling at home on Ryoku.
No previous Linux experience required.

[**Get started →**](guides/start-here.md) &nbsp; · &nbsp; [**Install Ryoku →**](guides/install-on-nixos.md) &nbsp; · &nbsp; [**Fix a problem →**](guides/troubleshooting.md)

</div>

---

## Where should I start?

You don't need to read everything. Choose the card that sounds like you.

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>✦ I'm new to Linux</h3>
      Coming from Windows? Learn what NixOS is, what Ryoku does, and how to prepare without risking your files.
      <p><a href="guides/start-here.md"><strong>Start from zero →</strong></a></p>
    </td>
    <td width="33%" valign="top">
      <h3>⌘ I already use NixOS</h3>
      Got a working flake-based NixOS installation? This is the simplest supported route to the Ryoku desktop.
      <p><a href="guides/install-on-nixos.md"><strong>Install Ryoku →</strong></a></p>
    </td>
    <td width="33%" valign="top">
      <h3>◇ I need help</h3>
      Something disappeared, broke, or won't launch? Start with safe checks instead of reinstalling everything.
      <p><a href="guides/troubleshooting.md"><strong>Find a solution →</strong></a></p>
    </td>
  </tr>
</table>

## Explore the guides

Each guide is short, linked to related topics, and written for someone who might never have opened a Linux terminal before.

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>01 &nbsp; Getting started</h3>
      <p><a href="guides/start-here.md"><strong>Start here ↗</strong></a><br />What NixOS and Ryoku actually are.</p>
      <p><a href="guides/before-you-install.md"><strong>Before you install ↗</strong></a><br />Backups, hardware, and choosing a safe route.</p>
      <p><a href="guides/install-on-nixos.md"><strong>Install Ryoku on NixOS ↗</strong></a><br />A guided installation, explained step by step.</p>
      <p><a href="guides/install-from-iso.md"><strong>Installer USB and ISO ↗</strong></a><br />What to know before experimenting with a fresh install.</p>
    </td>
    <td width="50%" valign="top">
      <h3>02 &nbsp; Getting comfortable</h3>
      <p><a href="guides/first-boot.md"><strong>Your first 10 minutes ↗</strong></a><br />Find apps, settings, and the essentials.</p>
      <p><a href="guides/personalise.md"><strong>Make Ryoku yours ↗</strong></a><br />Wallpapers, colours, bars, and launchers.</p>
      <p><a href="guides/applications.md"><strong>Apps and software ↗</strong></a><br />How installing apps differs from Windows.</p>
      <p><a href="guides/glossary.md"><strong>Words explained simply ↗</strong></a><br />Flakes, rebuilds, generations, and other new terms.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>03 &nbsp; Keeping things running</h3>
      <p><a href="guides/updates.md"><strong>Updates and rebuilds ↗</strong></a><br />What an update changes and how to apply one.</p>
      <p><a href="guides/recovery.md"><strong>Return to a working system ↗</strong></a><br />Understanding previous NixOS generations.</p>
      <p><a href="guides/troubleshooting.md"><strong>Fix common problems ↗</strong></a><br />Useful checks and what to share when asking for help.</p>
    </td>
    <td width="50%" valign="top">
      <h3>04 &nbsp; Quick answers</h3>
      <p><a href="guides/commands.md"><strong>Commands that matter ↗</strong></a><br />A few commands you'll actually use, with explanations.</p>
      <p><a href="guides/faq.md"><strong>Frequently asked questions ↗</strong></a><br />Straight answers about Windows, graphics, updates, and more.</p>
      <p><a href="CONTRIBUTING.md"><strong>Help improve these docs ↗</strong></a><br />How to make a guide clearer or report an outdated step.</p>
    </td>
  </tr>
</table>

## Your first journey

**Coming from Windows?** Here's a simple order to follow. Click one step at a time.

**[1. Understand the basics](guides/start-here.md)** → **[2. Prepare safely](guides/before-you-install.md)** → **[3. Install](guides/install-on-nixos.md)** → **[4. Explore your desktop](guides/first-boot.md)**

> [!IMPORTANT]
> **Installing Ryoku on an existing NixOS system is not the same as installing NixOS from a USB drive.** The guided Ryoku installer does not partition your disks. The current pre-release Ryoku installer ISO **erases the disk you select** and does not support manual partitioning. If you're using Windows, read [Before you install](guides/before-you-install.md) before touching a drive.

## What makes NixOS different?

| Windows | Ryoku on NixOS |
| :--- | :--- |
| The Start menu opens your apps | The Ryoku app launcher opens your apps |
| Settings controls your system | Ryoku Hub controls much of your desktop, while NixOS manages system configuration |
| Many programs use `.exe` installers | Apps can be included in your NixOS configuration or installed through supported package systems |
| Windows updates change the installed system | NixOS builds new **generations**, making many system changes easier to reverse |

New terms? [The glossary explains them without assuming you're a developer.](guides/glossary.md)

## Project and support

[**Ryoku on NixOS**](https://github.com/Ryoku-dev/Ryoku-on-NixOS) · [**Main Ryoku project**](https://github.com/Ryoku-dev/ryoku) · [**Report a bug**](https://github.com/Ryoku-dev/Ryoku-on-NixOS/issues) · [**Community Discord**](https://discord.gg/xvr69NRsmt)

This handbook explains the beginner experience. For detailed technical behaviour, the [maintained NixOS port guide](https://github.com/Ryoku-dev/Ryoku-on-NixOS/blob/main/docs/nixos.md) is the reference.

<div align="center">

---

<sub>Beauty on the surface. Clarity underneath.</sub>

</div>
