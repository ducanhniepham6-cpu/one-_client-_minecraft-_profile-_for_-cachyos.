# CachyOS quick start: OneClient + Minecraft 1.8.9

This guide sets up a separate Minecraft 1.8.9 Bedwars instance on CachyOS. It does not install a custom client or redistribute mods. `config/bedwars-profile.yaml` is a planning template, not a file OneClient imports directly.

## 1. Install OneClient

Open the [OneLauncher releases page](https://github.com/Polyfrost/OneLauncher/releases/latest) and download the Linux x86_64 AppImage or Flatpak asset that matches your system. Prefer the release page over third-party mirrors. The release page also provides `.sig` files for some assets; follow the project's published verification instructions if you verify signatures.

For an AppImage saved as `~/Downloads/OneClient.AppImage`:

```bash
chmod +x ~/Downloads/OneClient.AppImage
~/Downloads/OneClient.AppImage
```

The release assets are built for x86_64 Linux. If you have a different architecture, check the release assets before installing.

## 2. Make an isolated instance

In OneClient, create a new cluster/instance and set Minecraft to **1.8.9**. Give it a distinct name such as `Bedwars 1.8.9 - Clean`; use a dedicated game directory if the UI offers that option. This keeps the test profile separate from existing worlds, mods, and settings.

Start with the vanilla 1.8.9 instance once before adding mods. If the launcher offers Java runtime selection, choose a Java 8 runtime for Minecraft 1.8.9. Verify the selected Java executable/version in the launcher settings or game log instead of assuming the system default is Java 8.

## 3. Establish a clean baseline

1. Launch the unmodded instance and reach the main menu.
2. Join your intended Bedwars server and check that the server permits your planned client-side mods.
3. Note FPS, frame pacing, resolution, and any launcher/game errors.
4. Close the game normally and keep the generated logs if it fails.

Do not start by importing an entire unknown client or modpack. Add one trusted mod at a time and retest after each change.

## 4. Add the visual layer cautiously

Use `docs/bedwars-mod-list.md` as a compatibility checklist, not as proof that any named mod is current, safe, or allowed by your server. For each mod, confirm all of the following from the developer's official page:

- it explicitly has a Minecraft 1.8.9 build;
- it matches the instance's loader and other installed mods;
- its current server rules permit its features;
- the downloaded file comes from the official project/provider page.

Keep a copy of the clean `mods/` and `config/` directories. If OneClient shows a checksum for a download, do not bypass a failed verification.

## 5. CachyOS checks

- Use the GPU driver stack appropriate for your hardware; do not force Vulkan for Minecraft 1.8.9. Test the default OpenGL path first.
- Keep shader packs off while establishing the baseline.
- Start with a render distance of 6 chunks and reduced particles; tune based on actual frame pacing.
- Use the conservative JVM options in `config/java-opts.txt`, then compare with no custom flags if startup or stability worsens.
- Avoid running multiple overlapping HUD mods.

## Troubleshooting

- **Wrong Java:** check the instance's configured Java path and the game log; select Java 8 for this legacy version.
- **Crash after adding a mod:** remove the last added mod from this dedicated instance and retry; inspect the crash report and launcher log.
- **AppImage does not start:** confirm it is executable and x86_64-compatible; try the Flatpak asset from the same official release if appropriate.
- **No improvement in FPS:** remove custom JVM flags first, then lower render distance and effects one setting at a time.

## Project links

- [OneClient releases](https://github.com/Polyfrost/OneLauncher/releases/latest)
- [Profile plan](bedwars-profile.md)
- [Mod verification checklist](bedwars-mod-list.md)
- [CachyOS setup notes](cachyos-setup.md)
- [Profile comparison](profile-comparison.md)
