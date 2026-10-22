# SheepTerm for Linux

A native terminal client for network engineers: **SSH and local shells** in tabs and split panes, with per-vendor
output highlighting, saved hosts, snippets and optional end-to-end encrypted sync through *your own* Google Drive.
It is the Linux sibling of [SheepTerm for macOS](https://github.com/bestonehxh/SheepTerm) and
[SheepTerm for Windows](https://github.com/bestonehxh/SheepTerm-Windows), and shares their terminal emulator, SSH client
and data formats: hosts, settings, `known_hosts` and the encrypted password vault sync between all three.

## At a glance

- **Vendor-aware highlighting** for switches, routers and firewalls.
- **SSH and local shell** with saved hosts and groups, ProxyJump, password retry and Try Again after a failure.
- **Split panes** to keep several sessions visible.
- **Password vault** protected by your passphrase, and **Safe Paste** that shows a multi-line or risky paste before it is sent.
- **Optional Google sign-in** for passphrase-encrypted sync through your own Drive, with the Mac and Windows apps.
- Native **GTK4** app written in Swift: X11 and Wayland, no Electron, no installer.

[Website & screenshots](https://sheepterm.com/) · [macOS download](https://github.com/bestonehxh/SheepTerm/releases/latest) · [Windows download](https://github.com/bestonehxh/SheepTerm-Windows/releases/latest) · [Linux download](https://github.com/bestonehxh/SheepTerm-Linux/releases/latest)

This is the first Linux line (0.1). Serial consoles, web tabs and the AI panel are not in the Linux build yet.

## Download

| Platform | Download | Requirements |
|---|---|---|
| 🍎 macOS | [**Latest release**](https://github.com/bestonehxh/SheepTerm/releases/latest) | macOS 26.4 (Tahoe) or later, Apple Silicon |
| 🪟 Windows | [**Latest release**](https://github.com/bestonehxh/SheepTerm-Windows/releases/latest) (portable zip) | Windows 10 / 11, 64-bit (x64) |
| 🐧 Linux | [**Latest release**](https://github.com/bestonehxh/SheepTerm-Linux/releases/latest) (portable tar.gz) | x86_64 or arm64 (aarch64), GTK 4 |

Go to the [latest release](https://github.com/bestonehxh/SheepTerm-Linux/releases/latest) and download the archive for
your machine: `SheepTerm-<version>-<build>-linux-x86_64.tar.gz` for most PCs, or `...-linux-aarch64.tar.gz` for ARM
(Raspberry Pi 5, Ampere, Snapdragon laptops). `SHA256SUMS.txt` next to them lists the checksums.

```sh
tar xzf SheepTerm-*-linux-x86_64.tar.gz
cd SheepTerm-*-linux-x86_64
./SheepTerm
```

Unpack it **somewhere of your own** (your home folder, `~/Apps`). No installer, no root, nothing written outside that folder.

### Requirements

GTK 4 from your distribution, nothing else: the Swift runtime is linked in and the fonts ship in `Resources/`.

| Distribution | Package |
|---|---|
| Ubuntu 24.04+ / Debian 13+ | `sudo apt install libgtk-4-1` |
| Fedora 40+ | `sudo dnf install gtk4` |
| Arch / Manjaro | `sudo pacman -S gtk4` |

Ubuntu 24.04 LTS (x86_64) is the tested baseline; other distributions with GTK 4.14 or newer and glibc 2.39 or newer
should work: please open an issue if yours does not.

## Portable, and where your data lives

Everything SheepTerm stores goes into a `Data/` folder **beside the `SheepTerm` executable**: hosts, settings, snippets,
`known_hosts`, session logs and the encrypted password vault. Copy or move the whole folder to take it all with you (it must
stay writable). Passwords are never stored in clear text; the vault needs your passphrase.

## Keys

Linux terminal conventions: **Ctrl+Shift+C / V** copy and paste, **Ctrl+Shift+F** find, **Ctrl+Shift+K** quick connect,
**Ctrl+Shift+T** new terminal tab, **Ctrl+Shift+W** close tab, **Shift+PageUp / PageDown** scrollback, **F10** the File menu.

## Licences

SheepTerm for Linux includes, with their licences in the `Licenses/` folder of the download:

- Inter and JetBrains Mono fonts - SIL Open Font License 1.1
- Lucide icons - ISC License; Phosphor icons - MIT License
- swift-crypto (BoringSSL) and swift-asn1 - Apache License 2.0
- The Swift runtime and Foundation - Apache License 2.0 with Runtime Library Exception

The application itself is (c) its author; see the release notes for details. Feedback and bug reports: open an issue on this repository.
