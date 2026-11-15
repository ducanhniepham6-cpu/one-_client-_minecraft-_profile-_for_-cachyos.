# Bedwars HUD layout guide (Minecraft 1.8.9)

A practical layout checklist for improving readability without hiding gameplay information or adding hidden-player information. This is a layout guide, not a mod or an importable OneClient configuration.

## Start with the vanilla HUD

Before adding overlays, play one match with the default HUD. Keep elements you can already read comfortably; add a third-party HUD element only to solve a specific problem. Avoid duplicating information already shown by Minecraft or the server scoreboard.

## Suggested layout zones

| Zone | Keep here | Guidance |
|---|---|---|
| Center | Vanilla crosshair and target view | Keep the center as clear as possible. Avoid large overlays or animated crosshairs. |
| Lower center | Hotbar, held item, health/armor/food | Preserve the vanilla hotbar and status bars; do not cover the held item or interaction area. |
| Upper corners | Small, optional status widgets | Use only a few compact widgets, with readable contrast and no overlap with the game view. |
| Side area | Server scoreboard | Leave the server-provided scoreboard visible and unmodified where practical; do not replace it with hidden or inferred data. |
| Keystrokes | Optional compact display | Place away from the crosshair and hotbar; it should be a visual display, not input automation. |

## Readability rules

- Prefer high contrast and compact labels over oversized panels.
- Avoid overlapping HUD mods that show the same health, armor, CPS, or key state.
- Use static or subtle effects; excessive animation and motion blur can obscure fights.
- Keep name tags to normal, server-provided visibility. Do not reveal entities through walls or beyond ordinary game rendering.
- Test at your actual resolution, GUI scale, and display scaling on CachyOS.
- If the server requires a vanilla HUD or restricts a feature, disable that feature or use the Clean/Tournament Safe profile.

## Change process

1. Save a screenshot of the current layout.
2. Change one widget or GUI scale setting.
3. Check that the hotbar, health, armor, crosshair, and scoreboard remain visible.
4. Test in a private world or permitted lobby before a match.
5. Revert changes that obscure the view, reduce performance, or conflict with server rules.
