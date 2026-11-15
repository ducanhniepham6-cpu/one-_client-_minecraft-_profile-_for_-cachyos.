# CachyOS setup notes: Bedwars 1.8.9

These notes cover the environment around OneClient on CachyOS/Arch. They do not promise that OneClient supports every legacy loader/OptiFine combination, and they do not bundle Java or Minecraft files.

## OneClient package

Use the official [OneClient 2.10.2 release](https://github.com/Polyfrost/OneLauncher/releases/tag/oneclient-2.10.2) or [latest releases](https://github.com/Polyfrost/OneLauncher/releases/latest). Select an asset that matches your architecture; the release page lists x86_64 Linux AppImage/Flatpak assets and AppImage signature files. Use the release's instructions rather than an assumed Flatpak application ID or third-party mirror.

For an AppImage, inspect its exact downloaded name, then make that file executable and run it:

```bash
ls -1 ~/Downloads/*AppImage
chmod +x ~/Downloads/<downloaded-appimage>.AppImage
~/Downloads/<downloaded-appimage>.AppImage
```

## Java 8

Minecraft 1.8.9 is a legacy version and typically needs Java 8. First prefer a Java runtime managed/selected by OneClient for the specific instance, if available. Otherwise, check CachyOS's current supported package source and verify the installed runtime before assigning its path. Java 8 packages may not be present in the standard repositories, so this guide intentionally does not claim that `sudo pacman -S jre8-openjdk` will work.

Read-only checks:

```bash
java -version
arch
```

Set Java per-instance in the launcher where possible; avoid changing the global Java alternative solely for Minecraft.

## Instance and loader

1. Create a dedicated instance named `Bedwars 1.8.9 - Clean`.
2. Try vanilla 1.8.9 first and save any launch error.
3. Before adding Forge or OptiFine, confirm that OneClient supports the exact version/loader workflow you intend to use. This documentation repo cannot add that support to OneClient.
4. Preserve the vanilla instance as a rollback; do not install unknown jars into the global game directory.

## Graphics and CachyOS

- Start with the normal GPU driver and OpenGL configuration; do not force Vulkan for Minecraft 1.8.9.
- Disable shaders for the baseline, start with about 6 chunks, and reduce particles.
- Change one setting at a time and record results using `bedwars-performance-checklist.md`.
- Begin with launcher-default JVM arguments. `config/java-opts.txt` contains only a small optional test set, not a guaranteed performance tweak.
- Keep enough RAM available for CachyOS and the desktop; increasing heap is not automatically an FPS improvement.

## Safety and rollback

Check server policy before every optional mod. Verify its exact 1.8.9 release, loader, dependencies, official source and published integrity data. Keep mods/config isolated to this instance. Exclude input automation, hidden-information overlays, reach/aim changes, packet manipulation, and anti-cheat bypasses.
