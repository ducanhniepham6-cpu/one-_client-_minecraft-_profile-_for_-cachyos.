# Bedwars Visual Profile for Minecraft 1.8.9 on CachyOS

This repository contains a Bedwars-focused launcher profile plan for Minecraft 1.8.9, tuned for Linux/CachyOS and built around visual clarity instead of unfair advantages.

The goal is simple:
- Stable Minecraft 1.8.9 runtime
- Clearer PvP visuals and better readability in Bedwars
- No cheat features such as ESP, reach, aimbot, auto-click, or auto-block
- Lightweight configuration that keeps FPS high on modern Linux machines

This project is intentionally inspired by the visual readability ideas behind client-side PvP visual mods, but it does not copy, ship, or redistribute the original mod or any proprietary code. The focus is on a clean, safe profile for Bedwars and personal play.

## What this profile includes

- Minecraft 1.8.9
- Java 8 runtime
- OptiFine 1.8.9 as the base visual layer
- Performance and clarity-oriented mod additions
- Bedwars-only preset with explicit mod whitelist and blacklist
- CachyOS/Linux tuning recommendations

## Recommended target stack

- Minecraft: 1.8.9
- Loader: OptiFine / Forge-compatible setup, depending on the server requirement
- Java: Java 8 (not Java 17+ for 1.8.9)
- OS: CachyOS / Arch-based Linux
- GPU: Mesa / Vulkan or OpenGL suitable drivers
- Priority: FPS, clean HUD, readable nametags, strong contrast, low input delay

## Safety rules

This project does not include:
- Auto-clickers
- Aim assist
- Reach hacks
- ESP / player wall hacks
- Auto-block / macro scripts
- Server-breaking or anti-cheat bypass features

A Bedwars visual profile should improve readability and comfort, not grant unfair game advantages.

## Quick install approach

### 1) Install Java 8

On CachyOS / Arch:

```bash
sudo pacman -Syu
sudo pacman -S jre8-openjdk
```

If your system prefers OpenJDK 8 alternative packages, use the distro-supported Java 8 package that matches your install.

### 2) Install OptiFine for 1.8.9

Download the correct OptiFine build for 1.8.9 and install it using your usual launcher or modloader flow.

### 3) Install the profile mods

Use the allowed list from `docs/bedwars-profile.md`.

### 4) Start with the Clean Bedwars profile

Use the preset in `config/bedwars-profile.yaml` as the default profile and adjust memory values if your machine differs.

## File overview

- `docs/bedwars-profile.md` – recommended profile details, whitelist, blacklist, tuning advice
- `config/java-opts.txt` – JVM tuning for 1.8.9 on Linux
- `config/bedwars-profile.yaml` – structured profile configuration
- `.gitignore` – standard local-editor ignores

## Recommended JVM settings

Use the values in `config/java-opts.txt` as the starting point. Tweak only after testing real FPS and stability.

## Recommended profile names

- `Clean Bedwars`
- `Visual Bedwars`
- `Tournament Safe`

Each profile should stay intentionally minimal and avoid stacking too many visual mods that can conflict with PvP readability.

## Important note about compatibility

The exact mod list may need to be adjusted depending on:
- server anti-cheat requirements
- whether the server uses Forge or vanilla+OptiFine
- your GPU driver stack and Mesa version
- whether you are using a third-party launcher or vanilla launcher

This repository provides the structure and safe defaults, not a guarantee of server-side compatibility.

## License

This project is intended for personal configuration and safe client tuning documentation. It is not a cheat client, exploit pack, or anti-cheat bypass tool.

---

For the detailed Bedwars strategy and visual profile, see: `docs/bedwars-profile.md`.
