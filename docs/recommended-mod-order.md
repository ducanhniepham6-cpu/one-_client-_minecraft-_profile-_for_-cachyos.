# Mod installation order and validation

This order is designed to make failures easy to diagnose. It deliberately does not prescribe downloading a bundle of unverified jars.

## Before installing anything

1. Create a dedicated OneClient instance for Minecraft 1.8.9.
2. Launch vanilla once; confirm Java selection and save the working logs.
3. Back up the instance's `mods/` and `config/` directories.
4. Check the target server's rules for each client mod and feature.

## Install in small steps

1. **Base game only:** launch and join the server.
2. **Graphics layer:** if desired, add only an OptiFine build explicitly made for Minecraft 1.8.9 and compatible with the instance's loader. Launch and test before proceeding. Do not assume every OptiFine installer/build is compatible with every Forge setup.
3. **One HUD/visual mod:** verify the exact 1.8.9 file and loader on its official project page. Install only one mod that provides the feature you need.
4. **Retest:** launch, inspect the HUD, join the server, and check logs.
5. **Repeat one at a time:** add another mod only if it does not duplicate functionality or introduce a conflict.

If a step breaks startup, remove the most recently added file and retest. Keep the known-good baseline rather than layering more mods over a broken installation.

## Verification record

For each candidate, record:

| Field | What to verify |
|---|---|
| Project and author | Official project page and recognizable maintainer |
| Game version | An explicit 1.8.9-compatible release, not just a generic label |
| Loader | Matches the exact instance loader and required dependencies |
| Feature | Cosmetic/readability only; no automation or hidden information |
| Distribution | Download from the official page/provider, not a rehost or video description |
| Server policy | Allowed by the specific server's current rules |
| Integrity | Keep the published checksum/signature if the publisher provides one |

Do not treat the repository's example names as a verified endorsement; availability and compatibility can change, and similarly named projects may be unrelated.

## Exclude

Do not install autoclickers, aim assistance, reach changes, ESP/wallhacks, automated bridging or combat, packet manipulation, or anti-cheat bypasses. Do not enable a feature merely because it is bundled with a visual mod.
