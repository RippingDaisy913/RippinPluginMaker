# Using the 4.10.0 upgrades

## Command and appearance

1. Open your existing design, then Map / HUD. Set **Map command** to a single
   word such as `atlas`. An optional leading slash is accepted; spaces and
   several built-in commands are rejected. A duplicate command row is rejected.
2. Change the title, map quality, labels, markers and linked Fabric settings.
   The interactive preview uses sample terrain. Drag its minimap to choose a
   corner; enable Big map to pan, wheel to zoom and click to place a sample point.
3. Apply Appearance copies the preview's settings into the design.
4. Save Design, preview/apply Update Project, then build. Update Project retains
   its existing conflict review and source backup. A changed command affects
   the generated Paper command, completer and help: `/atlas on`, `/atlas view
   cave`, `/atlas layout sidebar`, etc. Configuration and permission identities
   still use `minimap`, preserving existing settings and permission grants.
5. Existing Fabric client preferences override generated defaults. Change them
   in Minecraft through M > Settings when testing an existing installation.
   Client-only projects use Minecraft's keybindings; renaming this server command
   does not change the M binding.

## Build and installation dashboard

Select a saved/generated project, then Build & Install. Refresh reads declared
versions from JARs and pack manifests. The Java pack row uses the saved design
version because pack.mcmeta does not declare an application version.
Build compiles saved project files; it does not apply unfinished editor changes.
After it completes, Refresh loads the new files. Source timestamps identify
potentially outdated outputs. Reports explain missing linked builds, version
differences, Java requirements, missing dependencies, exact Minecraft mismatches,
duplicate IDs, matching pack pixel differences and overlapping font/HUD assets.
Dependency ranges and runtime behavior still need manual verification.

Choose a row and the exact destination folder: `plugins` for Paper, `mods` for
Fabric, `resourcepacks` for local Java packs, or Geyser's `packs` for Bedrock.
Java pack online hosting remains configured in ResourcePackManager; installing
into resourcepacks does not upload a pack or change server.properties.
Use Check Installation, then Preview + Install. Review the destination, previous
copies and any checks before confirming. Known Minecraft/server processes block
installation; stop them normally. Process inspection cannot prove that every
custom launcher or obscured process is stopped.

Install checks the source identity and hashes, backs up previous same-ID copies,
then installs one selected build. Unrelated files remain. Backups and receipt.json
are stored in **Rippin Install Backups** beside the destination folder. Java packs
are matched by filename; plugins/mods use their declared name/ID, and Bedrock
packs use the header UUID. It does not clean up arbitrarily renamed Java packs.

Restore Backup uses a receipt and that same destination folder. It checks backup
hashes and installed bytes and refuses to overwrite later changes or occupied
filenames. Restore and Install share a lock. Backups remain available afterward.
The dashboard does not start or stop Minecraft/the server or modify configs.

## Resource pack editor

Open editable pack folders, ZIPs or MCPACKs. Choose an existing PNG, paint with
Brush Color/Eraser, undo/redo strokes, or import matching-size art. Nearest-pixel
previews show original Java art and compact Bedrock map tiles. PNGs are limited
to 1024 x 1024; archives have entry, expansion and path checks.

Save Source + Backup changes editable PNG sources and keeps original bytes in
**Rippin Pack Backups** beside the source folder. Bedrock edits advance the header
and module patch versions while preserving UUIDs. External edits stop a save.
Export New Pack writes a new archive and retains unrelated assets, manifests,
licenses and credits. Imported archives are exported under a new name.
Sync Map to Bedrock converts the generated 256 x 256 Java minimap atlas to its
matching compact Bedrock glyph atlas, with a backup and version increase.
Save the Java source too, then rebuild and install both packs. Editing pack art
does not automatically update the live server, host, client or download cache.

## Workflow undo and redo

Undo/Redo cover workflow fields, disabled/unfinished drafts, action edits,
ordering, removal and examples. New edits after Undo discard abandoned Redo.
History holds the newest 100 states and resets when loading a saved design;
it is not written into design files. An example is grouped as one action.
AFK/RTP switches outside the workflow panel are outside this history.

## Testing before a stable release

Use a test project/instance. Check a renamed command on Paper and Bedrock;
accept the matching packs and test HUD/sidebar without overlapping the scoreboard.
Test Fabric map drag, click, wheel zoom, saved preferences and terrain in all
dimensions. Test the controller separately. The preview uses synthetic terrain
and does not connect to Minecraft or operate a controller.
