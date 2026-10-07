# Release verification — RippinPluginMaker 4.8.0

Checked on Windows, 2026-10-07, using Temurin JDK 25.0.4.1 and Gradle wrapper
9.1.0. The app targets Java 21. Generated Paper projects target Java 25 for 26.3.
Live server folders, installed app files and personal settings were not changed.

**605 assertions/checks passed:** 384 app checks, 169 simulated Paper event-adapter
checks and 52 simulated minimap runtime checks. The desktop app, generated full
Paper plugin, standalone HUD plugin and workflow-only plugin all built. Generated
Paper compilation used the cached 26.3.build.147-beta API.

| Check | Result |
| --- | --- |
| Map presets | Balanced/Detail/Low load set the intended cells, sampling distance and refresh; other draft settings retained |
| Saved designs | New controls roundtrip for integrated and saved HUD builders; older designs retain existing size/spacing and receive missing new options |
| Terrain artwork | Sixteen distinct terrain categories; dedicated ice, forest, crops, path, soil, End and Nether glyphs; tracked target differs from regular waypoint |
| Resource packs | Java/Bedrock atlas pixels match; manifests/UUIDs/versions, SHA-1, original MIT artwork/license and install kit preservation passed |
| Information rows | Coordinates/world/scale/target separate from map; largest map plus four rows fits fifteen sidebar entries; visibility changes rebuild row count |
| Scoreboard compatibility | Blank Java number format; original teams/health scores retained; previous board restored; another plugin's replacement board left alone |
| Update load | Unchanged prefixes not resent; cached loaded samples reused; unloaded chunks not sampled; action-bar mode performs no terrain sampling |
| Navigation | Ordinary-player tracking, suggestions, invalid selection preservation, arrival, off-screen/rotated edge marker, tracking off, independent players, restart persistence and cross-world world-name display passed |
| Invalid waypoint data | Non-finite coordinates excluded from targets and completion |
| Existing app/server behavior | Workspace close guards, themes/icons, menus, conditional workflows, source updates/backups, AFK/RTP/CrateNova rewards and actual Daisy/ZoneTimers JAR coexistence checks retained |
| UI review | Integrated Balanced/Detail screens, icon/text sample previews, saved HUD and original atlas rendered and inspected |

The final UI layout and usage text were refined after the full Paper run. The
384-check desktop suite passed again; the generated controller and runtime pack
artwork are unchanged from the successful 169/52-check Paper run.

The downloadable IntelliJ ZIP was extracted and rebuilt in a fresh folder with
all 384 app assertions passing. Its JAR's SHA-256 matches the Windows package
JAR exactly. Windows helpers parsed successfully and archive license checks
passed. Original map artwork remains MIT licensed; Maker additions retain
the Product Use License and existing component grants.

## Practical limits

No Minecraft Java or Bedrock game client was launched. Final in-game rendering,
resource-pack acceptance and native drag/drop still need the user's desktop/game
check. The minimap remains a vanilla sidebar terrain grid; it does not create a
movable client HUD or a full world map. Terrain is sampled from loaded surface
chunks, not caves. Java/Bedrock packs must be installed and updated separately.

The biome/world fallback path is exercised by the simulated server; actual biome
registry names are supplied by Paper in-game. Test-server process checks use a
controlled Java child fixture. Full Fabric Loom compilation remains unverified
in this restricted environment. Existing component and custom licenses remain.

## Reproduce

Run `gradlew.bat build` with JDK 25 for the app suite. For generated Paper builds
and simulated event/map tests, run `verification/Verify-Paper-Workflows.ps1` with
`-Offline` when dependencies are cached and optional CrateNova, DaisyEssentials
and ZoneTimers JAR paths for their integration checks. See UPGRADE_GUIDE.md and
MAP_SETUP.md for normal use and upgrading an existing plugin/packs.