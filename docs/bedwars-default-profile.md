# Default profile recommendation: Bedwars 1.8.9 on CachyOS

This is the recommended **starting setup**. It is documentation, not an installer or a YAML format that OneClient imports. This repository does not ship Minecraft, Java, OptiFine, Forge, or mod binaries.

## Clean Bedwars — default

- **Minecraft:** 1.8.9
- **Launcher:** OneClient, from the [official 2.10.2 release](https://github.com/Polyfrost/OneLauncher/releases/tag/oneclient-2.10.2) or [latest releases](https://github.com/Polyfrost/OneLauncher/releases/latest)
- **Instance:** separate/dedicated directory named `Bedwars 1.8.9 - Clean`
- **Java:** select Java 8 per instance where available and confirm it from the launch log
- **Mods:** none initially; launch vanilla first
- **Graphics:** shaders off; begin at 6 chunks and reduced particles
- **JVM:** launcher defaults initially; optional small test set is in `../config/java-opts.txt`

First establish whether the installed OneClient release can create and launch the exact 1.8.9 setup you need. Do not assume arbitrary legacy Forge/OptiFine combinations are supported. If launcher UI or metadata does not offer a supported route, capture the error and check OneClient's official documentation/releases rather than manually injecting unknown files.

## Visual Bedwars — optional variation

Make a copy of the clean instance. Add one HUD/visual mod only after verifying its official 1.8.9 release, exact loader/dependencies, documented behavior, integrity information, and permission under the target server's current rules. Keep the clean profile as rollback.

## Tournament Safe — policy-first variation

Use vanilla or only features explicitly approved by the tournament/server organizers. “Client-side” does not automatically mean permitted. When in doubt, disable optional mods and ask staff.

## Completion checklist

- [ ] OneClient official Linux asset matches machine architecture.
- [ ] Separate 1.8.9 vanilla instance launches successfully.
- [ ] Java 8 selection is confirmed in the launch log.
- [ ] Server policy has been checked before any optional mod.
- [ ] Each mod's release, loader, source, behavior and integrity are checked.
- [ ] Performance is compared against the clean baseline in the same scene.
- [ ] Logs and the clean instance are retained for rollback.

The documentation baseline is complete when these guides agree and the YAML is clearly marked as a template. A genuine integrated client/profile would additionally need launcher integration, verified mod metadata/artifacts, CachyOS runtime tests, and target-server policy checks; those are not implemented or claimed here.
