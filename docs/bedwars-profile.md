# Bedwars Visual Profile (Minecraft 1.8.9)

This document describes the safest and most effective way to build a Bedwars-oriented visual profile for Minecraft 1.8.9 on Linux/CachyOS.

## Design principles

1. Stability first
2. Clear PvP readability
3. Performance-friendly on modern systems
4. No cheat features or unfair automation
5. Minimal mod conflicts

## Recommended runtime

- Minecraft: 1.8.9
- Java: Java 8
- Loader: OptiFine or minimal Forge-compatible setup
- OS: CachyOS / Arch Linux

## Visual goals

The profile should improve:
- crosshair visibility
- item clarity and cooldown readability
- armor and health visibility
- scoreboard readability
- low-latency, non-overwhelming HUD
- block and sword animations that remain crisp during fast fights

## Allowed mods / safe visual layer

The following are examples of safe visual or utility mods that are commonly used in 1.8.9 setups. This is a guideline, not a required list.

- OptiFine 1.8.9
- BetterFps
- Keystrokes Mod
- Armor Status HUD
- ItemPhysic Lite
- Custom Crosshair mod
- Minimal HUD tweak pack
- Low-overhead UI enhancement mods

## Explicit blacklist

The following are not allowed in this profile:
- auto-clicker / auto-hit tools
- auto-block macros
- aim assist
- reach hacks
- ESP / wall hacks
- force-field overlays that reveal hidden players
- packet manipulation or fake movement clients

## Recommended Bedwars-specific configuration

### Profile A: Clean Bedwars

Best for everyday play.

- OptiFine enabled
- Simple HUD, minimal overlays
- Clear scoreboard and health bars
- Reduced particles and minimal shader clutter
- Keep the UI lightweight

### Profile B: Visual Bedwars

Best for players who want stronger readability.

- More contrast on health and armor indicators
- Bigger item labels / better cooldown clarity
- Slightly more visible crosshair and nametags
- Conservative effects only

### Profile C: Tournament Safe

Best for server compatibility and minimal risk.

- Only essential visual mods
- No experimental or hidden feature mods
- Strict whitelist only
- Prefer minimal effects while preserving clarity

## Suggested installation flow

1. Install Java 8 on CachyOS
2. Install OptiFine 1.8.9
3. Install only the approved visual HUD/mod list
4. Disable experimental shaders and heavy animations
5. Test FPS, click response, and PvP readability
6. Keep a backup of the mod folder and config files

## CachyOS tuning tips

- Use the default stable Mesa driver stack
- Avoid excessive shader packs for PvP
- Keep particle and fog settings conservative
- Prefer a stable OpenGL pipeline over high-end shader-heavy setup
- Disable unnecessary desktop compositing during play if needed

## Notes

This profile is meant to improve clarity, not automate or cheat. It should be used responsibly and only within the rules of your server.

---

See also: `config/bedwars-profile.yaml` and `config/java-opts.txt`.
