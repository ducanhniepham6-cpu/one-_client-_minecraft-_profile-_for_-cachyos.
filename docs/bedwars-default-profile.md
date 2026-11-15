# Bedwars default setup: OneClient 2.10.2 + CachyOS + Minecraft 1.8.9

## Deliverable and scope

This project is a **documented, visual-only setup plan and checklist**. It is not a custom Minecraft client, modpack installer, or directly importable OneClient profile. The YAML in `config/` is a human-readable template. No third-party mod is bundled or declared compatible without version/loader/server verification.

## Recommended first run: Clean Bedwars

1. Download OneClient from the [official 2.10.2 release](https://github.com/Polyfrost/OneLauncher/releases/tag/oneclient-2.10.2) or [latest releases](https://github.com/Polyfrost/OneLauncher/releases/latest); select an asset matching your system architecture.
2. In OneClient, create an isolated Minecraft **1.8.9** instance named `Bedwars 1.8.9 - Clean`.
3. Try launching the vanilla instance before adding mods. If the launcher does not offer 1.8.9 or fails to start it, save the error/log. Do not work around it by injecting an arbitrary jar.
4. Select Java 8 for this instance if the launcher supports that choice, then confirm the selected runtime from the game log. CachyOS package availability varies; do not assume a Java 8 package name or change the system default without checking.
5. Start with shaders off, reduced particles, and about 6 chunks. Leave JVM flags at launcher defaults initially.
6. Record performance using `bedwars-performance-checklist.md`; this becomes the baseline for later comparisons.

## Visual Bedwars: add only verified extras

Keep the clean instance as a rollback. For each optional visual/HUD feature, verify an official release explicitly supports Minecraft 1.8.9 and the instance's actual loader, inspect dependencies and documented behavior, and confirm the server permits it. Add one at a time. This project intentionally does not claim that OptiFine, BetterFps, or any named HUD mod is currently compatible with the user's exact OneClient setup.

Allowed design target: readability and comfort (compact HUD, legible crosshair, low visual clutter). Exclude input automation, aim/reach changes, ESP or hidden-information overlays, automated combat/bridging, packet manipulation, and anti-cheat bypasses.

## Tournament Safe

Use vanilla, or only features explicitly approved by the tournament/server staff. If the rule is unclear, disable the optional mod and ask staff.

## Ready-to-use checklist

- [ ] Official OneClient asset selected for the machine architecture.
- [ ] Separate vanilla 1.8.9 instance created and successfully launched.
- [ ] Java 8 selection confirmed in logs, if required/available for this runtime.
- [ ] Server policy checked before installing an optional mod.
- [ ] Exact game version, loader, dependencies, source, and behavior checked for each mod.
- [ ] Same-scene performance compared against the clean baseline.
- [ ] Clean instance and logs retained for rollback.

## Honest completion status

The documentation/template deliverable is present. A tested working setup on the user's CachyOS system is **not yet verified**; that requires the vanilla launch test and its logs. A custom visual mod/client is **not part of this deliverable**. See README and the linked guides for details.
