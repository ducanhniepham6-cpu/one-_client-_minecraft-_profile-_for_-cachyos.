# Bedwars mod list and verification policy

This file is a **verification checklist**, not a claim that particular downloads are currently maintained, safe, compatible, or approved by a server. Mod names and compatibility data can change. Verify the exact release before installation.

## Safe profile scope

The goal is client-side presentation and comfort for Minecraft 1.8.9: performance settings, a readable crosshair, or a small HUD element. OneClient itself is the launcher; this repository does not contain a Minecraft client implementation or mod binaries.

## Candidate categories

Only consider a candidate after confirming its official project page explicitly offers a Minecraft 1.8.9 release and the correct loader:

- **Graphics/performance:** optional graphics layer such as a compatible OptiFine build. Test the exact build with the chosen loader.
- **HUD/readability:** choose at most one mod for each overlapping element (for example, keystrokes or armor status), and confirm the server allows it.
- **Cosmetic animations:** optional and only where permitted; disable if it reduces visibility or performance.

No specific third-party mod is marked as verified or approved by this repository. Do not use the former example list as a verified whitelist without checking each mod's official release metadata.

## Do not use

- autoclickers or automated clicking;
- aim assistance, reach changes, or automated combat/bridging;
- ESP, wallhacks, or overlays revealing hidden information;
- packet manipulation, anti-cheat bypasses, or fake movement;
- any feature prohibited by the target server, even if bundled with a visual mod.

## Verify every candidate

1. Open the developer's official page or the official Modrinth/CurseForge project page.
2. Confirm an actual 1.8.9 file and loader match; do not infer compatibility from a title or a newer release.
3. Review dependencies, changelog, permissions/license, and documented behavior.
4. Download only from that official source and retain its checksum/signature where published.
5. Add it to a disposable/dedicated instance, one at a time; check startup, logs, and server rules.

See [recommended installation order](recommended-mod-order.md) and [profile comparison](profile-comparison.md).
