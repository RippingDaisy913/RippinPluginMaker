# Testing 4.10.0

Use a separate Minecraft instance/server and keep backups.

1. Extract the Windows ZIP and launch it with Java 21+; build 26.x targets with JDK 25.
2. Open an existing design and confirm its command/settings remain. Change the
   map command to a name such as atlas and change appearance. Save, preview/apply
   Update Project and build. Test the chosen command and help in Paper/Bedrock.
3. Refresh Build & Install and check output versions. Check a disposable plugins
   or mods folder, review install and confirm. Verify unrelated files remain.
   Restore using its receipt and confirm previous copies return. Do not use a
   running Minecraft/server installation for this test.
4. Edit map PNGs in Pack Editor, undo/redo, export under a new name, save source
   backups and sync Java map art to Bedrock. Rebuild and accept both matching
   packs. Check icons, priority and HUD/sidebar without covering the scoreboard.
5. Try preview drag, click and wheel zoom, apply appearance, then test the actual
   Fabric map with M. Check pan, zoom, waypoint click, saved preferences and terrain
   in Overworld/Nether/End/caves. Check custom world linking.
6. Test workflow Undo/Redo with field edits, examples, ordering, deletion and an
   unfinished/disabled draft. Save/reopen to verify design persistence.
7. Test controller access/navigation separately; it has not been hardware verified.

Report failures in Issues using BUG-REPORT.txt. Include versions and exact steps;
remove credentials and private addresses from logs. See VERIFICATION.md and
KNOWN-LIMITATIONS.md for completed checks and remaining test scope.
