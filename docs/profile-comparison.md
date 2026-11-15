# Bedwars profile comparison

These are three configuration targets for one isolated Minecraft 1.8.9 instance. They are documentation profiles, not importable OneClient profile files.

| Profile | Mods | Visual changes | Use case |
|---|---|---|---|
| **Clean Bedwars** (recommended start) | Vanilla 1.8.9; optionally one verified graphics mod | Minecraft defaults; reduced particles and modest render distance | Establish a stable baseline and test server compatibility |
| **Visual Bedwars** | Clean profile plus only individually verified, server-permitted visual/HUD mods | Improve readability with a single crosshair/HUD/armor feature at a time | Personal preference after baseline testing |
| **Tournament Safe** | Vanilla only, or only mods explicitly allowed by the event/server | No experimental effects or overlapping overlays | Minimize compatibility and policy risk |

## Settings starting point

- Minecraft: 1.8.9
- Java: Java 8, selected explicitly for this instance
- Render distance: start at 6 chunks and adjust to hardware/server needs
- Particles: Reduced
- Shaders: Off while testing
- Memory: start with a 2–3 GiB maximum only if the machine has enough RAM; do not treat more allocated memory as an FPS fix
- JVM flags: begin with defaults; use `config/java-opts.txt` only as a conservative test and revert if unstable

## Promotion checklist

Move from Clean to Visual only when vanilla is stable and you have verified each mod's exact game version, loader, source, behavior, and server permission. Keep the clean profile available for comparison. If a server or tournament policy is unclear, use Clean/Tournament Safe and ask the server staff.
