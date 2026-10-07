# Java and Bedrock map setup

4.8 adds forest canopies, crops, roads, ice and more distinct terrain tiles.
Coordinates, biome/world, map scale and tracked destination can be shown below
the map. These options appear in both the integrated and saved HUD builders.
Java score numbers are hidden using [Paper's blank number format](https://jd.papermc.io/paper/1.21.7/io/papermc/paper/scoreboard/numbers/NumberFormat.html).

In **Map / HUD**, choose **Balanced**, **Detail** or **Low load**, then click
**Apply map quality**. Balanced uses 9 cells, 4 blocks per tile and a 10-tick
refresh; Detail uses 11 cells and 2 blocks; Low load uses 7 cells, 8 blocks and
a 20-tick refresh. The preset changes only these three settings. Zoom multiplies
the blocks represented by each tile. Other options and older saved values stay.

Create a waypoint as an operator with `/minimap waypoint add village`, then any
player with map access can use `/minimap track village`. A pink target shows the
destination, including on the edge when it is outside the visible area. Direction
and horizontal distance appear below the map; arrival means within three blocks.
Use `/minimap track worldspawn`, `/minimap track nearest`, or `/minimap track off`.
Selections are saved per player. `track waypoint <name>` also works for names
matching built-in options. A target in another world displays its world name.

When upgrading, use **Open Design → Update Project**, review/apply and build.
Install the rebuilt plugin JAR and both rebuilt packs. Replace the previous map
pack in Geyser's packs folder, update Java's ZIP URL/hash, and reconnect clients.
The Bedrock UUID stays stable; the artwork version increases for this revision.

In **Project Home**, enable **Map / HUD + resource packs**, then choose Configure.
Leave **Generate Java + Bedrock icon resource packs** checked. For Minecraft 26.3,
the Java pack format is **97.1**. Use SIDEBAR for an always-visible terrain map,
AUTO to preserve an existing sidebar, or ACTIONBAR for a compact text HUD.

Generate your project and build it. All selected server features share one Paper
JAR. The matching packs are in that project's **build/map-packs/** folder and
embedded inside its JAR. Editable artwork is under **resource-packs/java/** and
**resource-packs/bedrock/**. Build again after changing those files.

1. **Bedrock:** put the generated `*-Bedrock.mcpack` in
   `plugins/Geyser-Spigot/packs/`. Restart the server and reconnect. Players must
   accept the pack. Other Geyser platforms use their own packs folder.
2. **Java:** host the generated `*-Java.zip` at a direct download link. Set
   `resource-pack` in `server.properties` to that URL and `resource-pack-sha1` to
   the SHA-1 of that exact ZIP. Restart and reconnect; accept the pack. For a
   quick personal test, install the ZIP in Minecraft's resourcepacks folder.
3. **Test both editions:** use `/minimap on`, then `/minimap style icons`.
   Once both packs display correctly, set `minimap.icons-ready: true` in the
   plugin's config.yml, then `/minimap reload` as an operator. Players can use
   `/minimap style text` if they declined the pack or have conflicting fonts.

The plugin also exports both packs, the exact Java hash and a project-specific
MAP_SETUP.md into `plugins/<your-plugin>/resource-packs/` on startup. It does not
change server.properties or install packs into Geyser automatically.

Use `/minimap help` for controls. Operators can mark global waypoints at their
current location: `/minimap waypoint add spawn`, remove them with
`/minimap waypoint remove spawn`, and reload map settings with `/minimap reload`.
Players can use `/minimap waypoint list`, `/minimap zoom 1` through `4`, and
`/minimap off`. Global waypoints are visible to everyone with map access.

This is a terrain grid in Minecraft's sidebar. It does not add a freely movable
client HUD. The plain map works without a pack; the graphical tile icons need
the correct pack for each edition. Java and Bedrock packs use different formats:
Geyser sends Bedrock packs and does not convert Java packs automatically.

The map uses Unicode U+E400..E41F. If an existing pack uses these symbols or the
Bedrock `font/glyph_E4.png` file, merge the packs rather than replacing its font
atlas. Existing Java font providers may also need merging. The supplied artwork
is original and MIT licensed; each pack includes LICENSE. Minecraft client
rendering needs an in-game check on your Java and Bedrock versions.

References: [Geyser pack setup](https://geysermc.org/wiki/geyser/packs/),
[Bedrock manifests](https://learn.microsoft.com/en-us/minecraft/creator/reference/content/addonsreference/packmanifest),
[Minecraft 26.3 pack format](https://feedback.minecraft.net/hc/en-us/articles/48913133328013-Minecraft-Java-Edition-26-3).
