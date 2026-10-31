# ViteSniffer downloads

**Grab the latest build here:** https://github.com/AshCash247/vitesniffer-releases/releases/latest

## What this repo is

Binary distribution only. Source lives in a private repository.

Every tagged release ships two artifacts:

- `ViteSnifferSetup-x.y.z.exe` — a small bootstrap installer (0.2 MB, needs .NET 8 Desktop Runtime). Downloads the main app from the ViteSniffer server, verifies SHA-256, extracts to `%LOCALAPPDATA%\ViteSniffer`, creates shortcuts, launches.
- `ViteSniffer-x.y.z.zip` — the main app build, obfuscated with Obfuscar. Verifies against the SHA-256 printed in the release notes.

## Verifying integrity

Every release has SHA-256 hashes in the release notes. On your machine:

```powershell
Get-FileHash .\ViteSnifferSetup-1.0.0.exe -Algorithm SHA256
Get-FileHash .\ViteSniffer-1.0.0.zip -Algorithm SHA256
```

Compare against the release notes. If they don't match, don't run the file.

## What ViteSniffer does

Windows packet sniffer for PS5 and Xbox parties. Routes your console through the PC, captures the STUN handshake during party voice, drops each peer into a live table with IP, geo, ISP and the gamertag it resolves to. ARP MITM routing, Npcap capture, WinDivert lag switch, device scanner, Xbox companion with signed SISU auth.

Full feature list and status at the main site.

## Source code

Private. This repo contains **binaries only**.
