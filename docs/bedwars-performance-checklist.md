# CachyOS performance checklist for Minecraft 1.8.9

Use this checklist to diagnose frame pacing and launch stability without assuming a specific GPU or applying risky system-wide tweaks. Establish a vanilla baseline before changing settings.

## Before launch

- [ ] Use a dedicated Minecraft 1.8.9 instance.
- [ ] Confirm the instance selects Java 8; check the launcher's runtime setting or game log.
- [ ] Confirm the launcher asset matches your CPU architecture.
- [ ] Close unnecessary GPU-heavy applications and overlays for the test.
- [ ] Keep the system's normal CachyOS graphics drivers; do not switch graphics APIs or install random driver scripts for a game profile.

## Baseline in game

- [ ] Start with shaders off.
- [ ] Start around 6 chunks of render distance; reduce it if frame pacing is poor.
- [ ] Use reduced particles and default animations initially.
- [ ] Set a reasonable FPS cap supported by the display; an unlimited cap can increase heat/power use without improving perceived smoothness.
- [ ] Record resolution, GUI scale, average FPS, and noticeable stutter in the same scene.

## Isolate changes

- [ ] Change one graphics setting at a time.
- [ ] Add one verified mod at a time, then restart and test.
- [ ] If performance worsens after a mod, remove that last mod and compare.
- [ ] Test both a quiet scene and a busy Bedwars lobby/match; scene complexity changes results.
- [ ] Compare with default JVM options before adding custom flags.

## Symptoms and first checks

| Symptom | First checks |
|---|---|
| Low but steady FPS | Lower render distance and graphics effects; check resolution and FPS cap. |
| Stutter during play | Re-test with default JVM flags and no optional mods; inspect the game log for repeated errors. |
| Long pauses | Check memory pressure and other running applications; do not automatically allocate more heap. |
| Crash after a mod | Remove the last added mod; keep the crash report and launcher log. |
| Launcher opens but game fails | Verify the selected Java path/version, game files, and mod-loader compatibility. |

## Safe system diagnostics (read-only)

These commands report environment details; they do not change system configuration:

```bash
uname -m
java -version
```

If `java -version` does not report Java 8, select a Java 8 runtime for the instance through OneClient rather than changing the system-wide Java default blindly.
