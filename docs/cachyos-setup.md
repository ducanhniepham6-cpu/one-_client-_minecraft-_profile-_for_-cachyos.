# CachyOS setup guide for Bedwars 1.8.9

This guide is designed for Arch-based Linux systems such as CachyOS. It focuses on a stable Bedwars-friendly Java 8 + OptiFine setup.

## 1) Install Java 8

```bash
sudo pacman -Syu
sudo pacman -S jre8-openjdk
```

If your system uses an alternative Java 8 package name, install the supported package for your architecture.

## 2) Install Java 8 launcher support

If your launcher requires a Java path override, point it to the Java 8 binary in the installation directory.

Example:

```bash
/usr/lib/jvm/java-8-openjdk/bin/java
```

## 3) Install OptiFine 1.8.9

Download the correct OptiFine 1.8.9 jar and install it through your preferred launcher or through the standard OptiFine installer flow.

## 4) Use a clean mod folder

Keep a clean profile folder, such as:

```text
.minecraft/versions/1.8.9-Bedwars-Visual/
```

Only install the whitelisted mods from `docs/bedwars-mod-list.md`.

## 5) Recommended launch configuration

Use the settings in `config/java-opts.txt` as the base. Keep the profile minimal and stable.

## 6) GPU and desktop recommendations

- Use the stable Mesa stack
- Prefer OpenGL over excessive shader-heavy pipelines for Bedwars
- Avoid running extra desktop compositing effects while playing
- Disable unnecessary visual overlays

## 7) Validate the profile

Before using it in competitive play:
- test FPS stability
- test click response
- test server compatibility
- test whether your HUD remains readable during combat

## 8) Avoid common mistakes

- do not install every mod on the internet
- do not stack multiple HUD mods with duplicate overlay features
- do not enable shader packs or heavy effects while playing PvP
- do not use any mod that alters input, movement, or line-of-sight behavior

## 9) Recommended default profile name

- `Bedwars Visual 1.8.9`
- `Clean Bedwars`
- `Tournament Safe`
