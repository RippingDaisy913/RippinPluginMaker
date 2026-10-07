# Public Preview 1 — known limitations

Copyright (c) 2026 RippingDaisy913. Product Use License; see LICENSE.

- This is a test preview based on 4.8.0. The app is not signed and Java is not bundled. It runs on Windows with Java 21+; generated Paper 26.x builds need JDK 25 and first builds need internet.
- Paper is the primary supported generation path. The Fabric builder is experimental: generated code was checked, but the full Fabric Loom build remains unverified in this environment. Some project-type pages are previews and do not generate projects yet.
- Minimap graphics are a vanilla sidebar terrain grid, not a movable client HUD or a full world map. They show loaded surface terrain, not caves. Other sidebar plugins can compete for that display. AUTO can fall back to text.
- The minimap sample in the app illustrates its appearance. It is not connected to a Minecraft world. Enable "Include Map / HUD in this plugin" to generate the feature.
- Graphical map tiles require matching Java and Bedrock packs installed separately. Exporting a pack does not automatically host it or install it in Geyser. Start in text style; enable icons after the appropriate pack is installed.
- Real Minecraft Java/Bedrock rendering, pack acceptance and native drag/drop still need in-game/manual testing. Automated and simulated checks cannot establish those results.
- Open Design reopens maker-generated designs. Arbitrary existing plugin JARs cannot be converted automatically into editable visual projects. Check JAR inspects them.
- Saving a design and building do not regenerate existing source. Use Update Project to apply feature changes, then install the new plugin JAR and restart the test server.
- Server Essentials covers selected features; it is not a complete replacement for every EssentialsX command or module. Optional integrations need their corresponding server plugins.

See VERIFICATION.md for what was actually tested.
