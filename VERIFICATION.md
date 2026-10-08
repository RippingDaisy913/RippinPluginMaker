# RippinPluginMaker 4.10.0 verification

Date: 2026-10-08. Original app additions retain Product Use terms; generated
projects retain MIT and existing third-party notices.

## Passed checks

- Complete AppVerification: **688 assertions** (617 retained + 71 new).
- Custom map command generation: plugin.yml, executor/completer, generated help,
  pack setup guide and standalone HUD generator. Old designs keep /minimap;
  config keys and permission identities remain stable. Shading reaches Fabric.
- Workflow draft undo/redo: unfinished values, disabled drafts, rename, ordering,
  remove, grouped example, bounded history and abandoned redo branches.
- Install/restore in isolated test folders: duplicate same-ID replacement,
  byte-identical backups/restore, unrelated files and artifact kinds preserved,
  running-state guard, changed source/installation refusal, tampered backup
  refusal, later filename collision refusal, shared installation/restore lock.
- Dashboard: unbuilt and stale output reports, declared versions, wrong Java,
  exact Minecraft mismatch, missing Fabric API, pack glyph/HUD overlap and loaded
  asynchronous inventory. Screenshot review covers the dashboard, pack editor,
  interactive preview and app at its 960 x 680 minimum size.
- Pack editing: pixel export, preserved licenses/other bytes, compact Bedrock
  synchronization, source backup and manifest revision, external edit refusal,
  unchanged pixel byte preservation, wrong dimensions, oversized PNG header,
  traversal and case-insensitive duplicate paths, switching documents cleanly.
- Preview's actual Swing listeners: drag, short-click after panning, drag release
  without waypoint creation, cursor-anchored wheel zoom, heading-up drag and
  minimap corner selection.
- Newly generated /navigator Paper plugin and linked Fabric client compile with
  JDK 25 against cached Paper/Minecraft 26.3, Fabric Loader 0.19.5 and Fabric API
  0.161.0+26.3. The application compiles with --release 21. No dependencies changed.
- **35 actual Minecraft 26.3 input-event checks** pass using production generated
  map event bodies with a simulated surrounding screen/world. This retains the
  SDL left-button/keyboard correction from client 1.0.13.
- Release archives/JAR are checked for readable ZIPs, duplicate entries, version,
  exact source/template bytes, required notices and preserved dependency bytes.

## Limits

Tests use disposable workspace files and in-memory app preferences. They are not
live installation tests. No installed app/mod/plugin, server config or resource
pack was changed. Gradle tasks were not rerun against online repositories; javac
uses cached dependencies and the release JAR retains existing dependency bytes.
Actual Minecraft visuals, shaders, controller navigation, performance and
Bedrock HUD visibility need in-game testing. Head icons remain queued. The
separate RippinMap Fabric artifact remains 1.0.13; this app release is 4.10.0.
