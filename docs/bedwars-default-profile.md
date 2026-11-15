# Default profile recommendation: Bedwars 1.8.9 on CachyOS

This is the project's current recommended **starting profile**. It is a documented setup, not an installer or a YAML format that OneClient imports. The project does not ship Minecraft, Java, OptiFine, or third-party mod binaries.

## Clean Bedwars — default

Start here so there is a known-good reference before customization.

- **Minecraft:** 1.8.9
- **Launcher:** OneClient, downloaded from the [official releases page](https://github.com/Polyfrost/OneLauncher/releases/latest)
- **Java:** explicitly select a Java 8 runtime for this instance; check the launch log to confirm
- **Instance:** separate/dedicated directory named `Bedwars 1.8.9 - Clean`
- **Mods:** none initially; launch vanilla first
- **Graphics:** shaders off; begin at 6 chunks render distance, reduced particles
- **JVM:** launcher defaults initially; optional small settings are in `../config/java-opts.txt`

Do not assume OneClient supports installing arbitrary legacy Forge or OptiFine combinations from a profile template. Follow the launcher's supported workflow and confirm the exact 1.8.9 loader path before adding a mod.

## Visual Bedwars — optional variation

Make a copy of the clean instance. Add only a specific HUD or visual mod if its official release explicitly supports Minecraft 1.8.9 and the instance loader, the target server permits its behavior, and the mod is downloaded from its official project page. Install one at a time and preserve the clean instance as a rollback.

Do not enable features that automate inputs, change reach/aim, reveal hidden entities, or alter network behavior. For unknown server policies, stay on Clean Bedwars.

## Tournament Safe — policy-first variation

Use vanilla 1.8.9, or only features explicitly approved by the tournament/server organizers. “Client-side” does not automatically mean permitted. When in doubt, disable optional mods and ask staff.

## Ready-to-use checklist

- [ ] OneClient downloaded from the official release page; package matches machine architecture.
- [ ] A separate 1.8.9 instance exists and has launched successfully without mods.
- [ ] Java 8 is selected for that instance and confirmed in its log.
- [ ] Server policy has been checked before adding any optional mod.
- [ ] Any optional mod has a verified 1.8.9 release, correct loader, official source, and documented behavior.
- [ ] Performance has been compared against the clean baseline on the same scene.
- [ ] Logs and the clean instance are retained for rollback.

## Project completion criteria

The documentation baseline is complete when the linked guides agree, explain that the YAML is not importer input, and provide this default and validation checklist. A genuinely integrated custom client/profile would additionally require actual launcher integration, verified mod metadata/artifacts, runtime tests on CachyOS, and compatibility checks on the target server; those are not implemented or claimed here.
