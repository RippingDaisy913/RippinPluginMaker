# Public Preview 1 — tester checklist

Copyright (c) 2026 RippingDaisy913. Product Use License; see LICENSE.

This package uses the same app binary as RippinPluginMaker 4.8.0.
Please start with a new project and a separate test server.

1. **Launch:** extract all files, run `RippinPluginMaker.bat`, and check that the app opens. Dark is the default on a fresh install; existing appearance choices are remembered.
2. **Simple Paper plugin:** enter a unique plugin name and package, select your Paper version, and add a command such as `hello` without a slash. Generate a project and build its JAR. Check that it loads and the command works.
3. **Save and reopen:** save your design, close its tab, then use Open Design. Verify settings and table rows are retained. Try closing a changed tab and cancelling the close prompt.
4. **Menu:** enable a menu, add a button and a message action, generate/build, then open it using its chosen command in Minecraft.
5. **Minimap:** open `Examples/Minimap Starter.json`, generate/build, and install the resulting MapStarter JAR on your test server. Try `/minimap on`, `off`, `status`, `zoom 2` and `help`. Start in text style. Follow MAP_SETUP.md before testing icon style. Report Java and Bedrock results separately.
6. **Update:** change a generated project's setting, use Update Project, inspect the proposed changes, apply and build. Confirm that a source backup is created. Keep any custom changes when resolving conflicts.
7. **AFK/RTP, optional:** enable the selected feature or workflow, set corners in game, and check countdown cancellation on exit. CrateNova rewards require the CrateNova plugin and an existing key/crate; they are off by default.
8. **Appearance:** try Light and Dark, switch feature pages, adjust scrolling, and close/reopen project tabs. Report unreadable controls or duplicate tabs.

## Report a problem

Copy BUG-REPORT.txt and fill it in. Give the steps and exact error message.
For build failures, include the relevant app build log. For plugin failures,
include the plugin's startup error from the test server log. A screenshot helps
with display problems. Remove private addresses, passwords and access tokens.

Send feedback to the person who shared this preview. No support address or
automatic reporting service is configured in this preview package.
