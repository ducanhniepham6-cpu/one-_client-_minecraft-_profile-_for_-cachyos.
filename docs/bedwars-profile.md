# Bedwars Visual Profile for Minecraft 1.8.9 on CachyOS

A practical, **visual-only** setup plan for a separate OneClient Minecraft 1.8.9 instance. It emphasizes stable startup, readable visuals, and conservative CachyOS settings. It does not include mod binaries or implement a custom Minecraft client.

## Goal and boundaries

- Keep Bedwars in its own instance so existing worlds and configurations are not affected.
- Start from a vanilla 1.8.9 baseline, then test optional graphics/HUD mods one at a time.
- Verify exact 1.8.9 version, loader, official download source, and the target server's rules for each mod.
- Exclude automation, hidden-information overlays, combat advantages, packet manipulation, and anti-cheat bypasses.

## Requirements and profile files

- Minecraft 1.8.9
- Java 8 selected for the instance
- CachyOS/Arch-based Linux, x86_64 assets where applicable
- `config/bedwars-profile.yaml` is a project template only; OneClient does not import it directly.
- `config/java-opts.txt` contains conservative optional JVM settings; begin with launcher defaults.

## Related guides

- [Quick start on CachyOS](quickstart-cachyos.md)
- [Mod verification policy](bedwars-mod-list.md)
- [Recommended installation order](recommended-mod-order.md)
- [Compare the three profiles](profile-comparison.md)

## Visual goals

Prefer clarity without clutter: readable crosshair, minimal HUD overlap, reduced particles, and steady frame pacing. Avoid stacking multiple mods that draw the same HUD element. Do not assume a feature is allowed just because it is client-side; check the server's rules.

## Three profiles

- **Clean Bedwars:** vanilla baseline; recommended first.
- **Visual Bedwars:** add only individually verified visual/HUD mods that the server permits.
- **Tournament Safe:** vanilla or only explicitly approved mods; if policy is unclear, use vanilla.

See [profile comparison](profile-comparison.md) for settings and promotion checks.
