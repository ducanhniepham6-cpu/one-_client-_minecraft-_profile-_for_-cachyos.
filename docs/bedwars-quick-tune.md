# Bedwars quick-tune workflow (1.8.9)

Use this short workflow on CachyOS after creating the dedicated OneClient instance. It avoids stacking generic JVM flags or mods without measurements.

## Pass 1 — clean baseline

1. Select Minecraft 1.8.9 and Java 8 for this instance.
2. Launch vanilla with default JVM arguments.
3. Keep shaders off, start at 6 chunks, and use reduced particles.
4. Test the same lobby or scene for a few minutes; note FPS, stutter, and whether the HUD is readable.

## Pass 2 — graphics tuning

If frame pacing is not smooth, lower render distance first, then reduce optional graphics effects. Use an FPS cap near a practical refresh target rather than assuming unlimited FPS is best. Change one setting at a time and repeat the same test.

## Pass 3 — optional visual mods

Only after the baseline is stable:

1. Verify the exact mod release supports Minecraft 1.8.9 and the instance loader.
2. Check the target server's current rules.
3. Install one mod from its official source.
4. Restart and inspect logs; test that the HUD does not overlap important information.
5. Keep it only if it solves a real readability need without hurting stability or violating policy.

## Pass 4 — memory and JVM

Begin with launcher defaults. If needed, use the small optional argument set in `config/java-opts.txt`; keep the maximum heap appropriate for total system RAM and leave room for CachyOS and the desktop. Remove custom arguments if they cause startup errors, longer pauses, or no measurable improvement.

## Pass 5 — keep a known-good profile

Keep `Clean Bedwars` unchanged as a control. Save visual changes in a separate instance/profile. For tournaments or unclear server rules, use vanilla or only explicitly approved features.
