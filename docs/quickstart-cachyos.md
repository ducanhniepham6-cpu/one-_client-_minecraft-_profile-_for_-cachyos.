# CachyOS quick start: OneClient + Minecraft 1.8.9

This guide sets up a separate Minecraft 1.8.9 Bedwars instance on CachyOS. This repository is documentation and configuration guidance only: it does not install a client, distribute Minecraft/Java/mod binaries, or provide an importable OneClient profile. The YAML under `config/` is a template, not an input format supported by OneClient.

## 1. Download OneClient from its official release

Open the [OneLauncher 2.10.2 release](https://github.com/Polyfrost/OneLauncher/releases/tag/oneclient-2.10.2) or the [latest releases page](https://github.com/Polyfrost/OneLauncher/releases/latest). For x86_64 Linux, choose the AppImage or Flatpak asset listed on the release page. Do not use a package for a different architecture. The release includes AppImage signature assets; follow the project's official verification instructions if verifying a signature.

For an AppImage downloaded to `~/Downloads`, first inspect the actual filename, then run it (replace the example name with the exact asset name you downloaded):

```bash
ls -1 ~/Downloads/*AppImage
chmod +x ~/Downloads/<downloaded-appimage>.AppImage
~/Downloads/<downloaded-appimage>.AppImage
```

Do not install an assumed Flatpak application ID from a command copied elsewhere; use the Flatpak asset/installation instructions on the official release page.

## 2. Create an isolated instance

In OneClient, create a separate cluster/instance for **Minecraft 1.8.9**, named for example `Bedwars 1.8.9 - Clean`. Use a dedicated game directory if the launcher offers it. Do not overwrite or migrate an existing instance for this first test.

Select Java 8 for this instance if OneClient offers a managed or user-selected runtime. Confirm the selected runtime in the launch log. CachyOS package availability and package names can vary; do not assume `jre8-openjdk` is available from the standard repositories or change the system-wide Java default blindly. See [CachyOS setup notes](cachyos-setup.md).

## 3. Establish a clean baseline

1. Launch the unmodded instance and reach the main menu.
2. If the launcher cannot create or start 1.8.9, stop here and save its error/log; do not install random loaders or jars to work around it.
3. Check the rules of your Bedwars server before using any third-party client-side mod.
4. Note FPS, frame pacing, resolution, and launcher/game errors in the performance checklist.
5. Close the game normally and retain the log if startup fails.

Do not start by importing an unknown client or modpack. Add only a verified mod, one at a time, and retest after each change.

## 4. Add optional visual mods cautiously

Use `bedwars-mod-list.md` as a verification policy, not as confirmation that a named mod is current, compatible, or server-approved. Before installing, verify that the exact official release:

- explicitly supports Minecraft 1.8.9;
- matches the instance's actual loader and dependencies;
- has features permitted by your server's current rules;
- comes from the official project/provider page.

Keep the clean instance as a rollback. Do not bypass a failed checksum/signature check.

## 5. CachyOS graphics and performance

- Use the normal driver stack appropriate to your GPU; test the game's default OpenGL path first. Do not force Vulkan for this legacy game.
- Keep shaders off while establishing the baseline.
- Start around 6 chunks and reduced particles; tune using the same scene and checklist.
- Start with default JVM arguments. Only test the short optional arguments in `config/java-opts.txt` if needed; revert if startup or frame pacing worsens.
- Avoid overlapping HUD mods.

## Troubleshooting

- **Wrong Java:** select Java 8 for this instance and confirm the executable/version in the game log.
- **Launcher cannot start 1.8.9:** retain the error and verify OneClient's documented support for that game/loader combination before proceeding. This repo does not implement legacy-version support.
- **Crash after adding a mod:** remove the last added mod from this dedicated instance and inspect its crash report/log.
- **AppImage does not start:** confirm executable permission and architecture; use only the official release asset and its published instructions.
- **No FPS improvement:** compare against defaults, then change render distance and effects one at a time.

## Project links

- [OneClient 2.10.2 release](https://github.com/Polyfrost/OneLauncher/releases/tag/oneclient-2.10.2)
- [Latest OneClient releases](https://github.com/Polyfrost/OneLauncher/releases/latest)
- [Recommended default profile](bedwars-default-profile.md)
- [Mod verification checklist](bedwars-mod-list.md)
- [CachyOS setup notes](cachyos-setup.md)
- [Performance checklist](bedwars-performance-checklist.md)
