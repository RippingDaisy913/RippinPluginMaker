# RippinPluginMaker licensing and credits

Copyright (c) 2026 RippingDaisy913.

The app combines proprietary additions with preserved MIT code and third-party
libraries. The root `LICENSE` permits using the compiled product for personal
or commercial projects and restricts reuse, publication, modification, and resale
of its proprietary application code. It expressly permits sharing the plugins
and mods created with the product under each generated project's license.

| Material | Applicable terms |
| --- | --- |
| Original CustomPluginMaker 3.0 code and template material | `LICENSE-3.0-MIT.txt`; existing MIT permissions remain |
| Original 3.1 launcher and HUD generator/builder additions | Preserved `LICENSE-3.1-ADDITIONS.txt`; product-use permission in `LICENSE` |
| Original 4.0/4.1 launcher, Fabric generator/builder, settings, branding, and project-type system | Preserved `LICENSE-4.0-ADDITIONS.txt`; product-use permission in `LICENSE` |
| New 4.2–4.6 design persistence, JAR checker, Windows scripts, unified workspace, map editor/pack generator, theme service, protected project updates, app integration and new modifications | Proprietary; root `LICENSE` |
| Generated Paper/HUD starter output and original map pack artwork | MIT; license inside that generated project, JAR and each pack |
| Generated Fabric starter output | Builder-selected license; license inside that generated project and JAR |
| Gson 2.13.2, SnakeYAML 2.5, Error Prone annotations 2.41.0 | Apache-2.0; see `THIRD-PARTY-NOTICES.txt` and `licenses/` |
| Gradle wrapper | Apache-2.0 and preserved Gradle notices; see `licenses/Gradle-NOTICES.txt` |

The 3.0 Java portion comprises BuildService, CoreEditor, CoreOptions,
FeaturesEditor, MakerApp, MenuEditor, MultiMenuEditor, PlayerFeatures,
PluginSpec, ProjectGenerator, ProjectOptions, and TprOptions. The preexisting
3.0 portions of those files remain MIT; new 4.2/4.3 modifications are identified in
their headers and are covered by the product-use license. Files in
`src/main/resources/*.template` and `project-template/` are starter output;
their existing MIT/template notices remain, and section 4 of the root license
expressly permits generated additions under the generated project's license.

The new 4.2 classes are DesignActions, DesignStore, JarCheckerDialog,
JarInspector, MenuActions, ProductInfoDialog, and StructuredData. Verification helpers and packaging
scripts added for this update are also covered by the product-use license.

The IntelliJ/source archive is the copyright holder's editable development
package. Share the Windows product archive with ordinary users. Possession of
source is not a grant to redistribute proprietary portions.

The new 4.8.0 ScrollSupport service and scrolling settings use the root Product
Use License. Existing component grants and generated-output licenses are retained.

Earlier MIT grants are preserved. These files do not claim exclusive ownership
of third-party code, Minecraft, Paper, Fabric, or independently created software.
No third-party endorsement is implied.

New 4.3 WorkflowSpec, WorkflowEditor, FlowEditor and WorkflowEngine classes,
their app integration and new verification helpers use the root Product Use
License. Generated copies of WorkflowEngine and WorkflowController are starter
output licensed under the generated project's MIT license, as permitted by
section 4 of the root license. WORKFLOWS.md is the generated project's guide.
