# Known limitations - 4.10.0 pre-release

- Automated checks and Java compilation do not establish Minecraft playtest
  results. Actual Java/Bedrock rendering, shaders, performance and pack acceptance
  need testing. The Bedrock top-left HUD is still awaiting an in-game retest;
  sidebar is the available fallback.
- The interactive preview uses synthetic terrain and does not connect to a live
  world or test a controller. Actual controller navigation is unverified.
- Terrain uses loaded chunks; cave mapping follows height layers. Test Nether,
  End, caves and custom worlds before relying on their appearance.
- Mob/player head icons remain queued. This release does not add them.
- Minecraft/Paper 26.x builds need JDK 25. The app runs with Java 21+; Java and
  target dependencies are not bundled. First builds may require downloads.
- Build compiles saved project source. Apply Update Project after editor changes.
  Existing client preferences can override generated Fabric defaults.
- Install checks known processes and file identities/hashes. Custom launchers or
  inaccessible process details can limit process detection. Stop the game/server
  normally. Java pack replacement matches filenames, not arbitrary renamed copies.
- Restore refuses modified installed files, damaged backups and occupied previous
  filenames. It does not merge later edits. Keep backups and receipts.
- Pack editing preserves existing dimensions and metadata; imported archives are
  exported under new names. Online pack hosting remains managed separately.
- Dependency ranges and runtime behavior still need verification. Fabric and
  some other project types remain experimental; Paper is the primary path.

See VERIFICATION.md for exact checks and BUILD_INSTALL.md for tool behavior.
Existing licenses and third-party notices remain applicable.
