# RippinPluginMaker

Make Minecraft Paper plugins with a Windows desktop app. Created by **RippingDaisy913**.

## Download 4.10.0 public preview

**[Download the Windows ZIP](https://github.com/RippingDaisy913/RippinPluginMaker/releases/download/v4.10.0/RippinPluginMaker-4.10.0-Windows.zip)**

[Release notes](https://github.com/RippingDaisy913/RippinPluginMaker/releases/tag/v4.10.0) | [Checksums](SHA256SUMS.txt) | [Report a problem](https://github.com/RippingDaisy913/RippinPluginMaker/issues)

The app displays version **4.10.0**. This is a pre-release for testing generated
projects on a separate Minecraft instance/server. Existing releases remain
available from the [releases page](https://github.com/RippingDaisy913/RippinPluginMaker/releases).

## New in 4.10.0

- **Build & Install dashboard:** view generated plugin, mod and pack outputs.
- **Reviewed installation and restore:** preview replacements, back up previous
  copies, verify file hashes and restore without overwriting later edits.
- **Resource pack editor:** edit existing PNGs, undo/redo strokes, preserve pack
  metadata/licenses, save source backups, and sync map art to compact Bedrock tiles.
- **Troubleshooting:** reports for outdated builds, dependency/version issues,
  duplicate copies, matching pack differences and font/HUD overlap.
- **Interactive map preview:** sample terrain with drag, zoom, corner, size,
  shading, coordinates and heading-up controls.
- **Workflow Undo/Redo:** includes disabled and unfinished workflow drafts.
- **Map customization:** choose your command, such as `/atlas`, and edit map
  appearance. Old designs keep `/minimap`; configuration and permission identities
  remain stable. The Minecraft 26.3 Fabric drag/keyboard fix is retained.

Menus, commands, permissions, visual workflows, AFK/RTP zones, selected server
essentials, saved designs, project updates and existing appearance settings remain.
See [BUILD_INSTALL.md](BUILD_INSTALL.md) for the new tools.

## Quick start

1. Download and **extract the entire Windows ZIP**.
2. Install **Java 21+** to run the app. **JDK 25** builds Minecraft/Paper 26.x projects.
3. Run **RippinPluginMaker.bat** from the extracted folder.
4. Enter project details and choose features. Generate a project, then build it.
   First builds need internet and the target's dependencies.
5. Open **Build & Install**, Refresh, choose a built file and its exact destination
   folder, check it, then review Preview + Install. Stop Minecraft/server normally
   before installing files.
6. For an existing design, Save Design and preview/apply **Update Project** before
   building changed settings. Existing Fabric client preferences can override
   generated defaults; adjust them through M > Settings in Minecraft.

Java is not bundled. The optional installer creates user shortcuts. GitHub's
automatic **Source code** archives contain this repository's download documentation;
use the **Windows ZIP** asset for the app. Proprietary application source is kept
separate from this public distribution.

## Minimap setup

Enable **Include Map / HUD in this plugin**. Choose the server map command and
appearance. Generate the linked Fabric client if Java players need the client
minimap/world map; it requires matching Fabric Loader/API and Minecraft versions.
Bedrock uses the Paper/Geyser map and its separate native pack. Geyser does not
convert a Java resource pack. Enable graphical icons after the matching packs
are accepted. `/minimap layout sidebar` provides the sidebar fallback; replace
`minimap` with your chosen command. The Bedrock top-left HUD remains a preview
whose visibility needs an in-game retest.

The interactive editor preview is synthetic terrain; it does not show a live
Minecraft world or verify controller behavior. Nether, End and cave rendering,
pack priority, saved preferences and the actual world map need playtesting.

## Testing and feedback

**688 automated app checks pass**, including 71 checks for this release.
Generated renamed-command Paper/Fabric projects compile against Minecraft 26.3
APIs; 35 actual-API map input checks pass with a simulated surrounding screen.
See [VERIFICATION.md](VERIFICATION.md), [TESTING.md](TESTING.md), and
[KNOWN-LIMITATIONS.md](KNOWN-LIMITATIONS.md) for the scope and remaining checks.

[Open an issue](https://github.com/RippingDaisy913/RippinPluginMaker/issues) using
[BUG-REPORT.txt](BUG-REPORT.txt). Include steps, expected/actual results, versions
and the exact error. For visual issues, include a screenshot and say Java or
Bedrock. Remove passwords, tokens and private addresses from logs.

## License and ownership

The compiled app may be used for personal or commercial project creation under
its included **Product Use License**. Existing open-source component permissions
are preserved. Generated original Paper/HUD/Fabric starter code and map artwork
retain their **MIT** licenses and third-party notices.
Read [LICENSE](LICENSE), [LICENSING.md](LICENSING.md), and
[THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt). All required notices are included
in the app download. Copyright (c) 2026 RippingDaisy913.
Not affiliated with Mojang or Microsoft.
