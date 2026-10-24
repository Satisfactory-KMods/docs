# KDataForge documentation coverage

This matrix records the restructure boundary. All 66 pre-existing KDataForge pages keep their
routes and detailed content. New pages add player, concept, command, and developer paths instead of
replacing the established feature, example, tutorial, reference, and architecture material.

`KDataForgeJS` and `LoadBalancers` are outside this audit.

## Entry and onboarding

| Existing page | Preserved content | New route from entry |
| --- | --- | --- |
| `index.mdx` | Product scope, audience routes, commands, multiplayer and restart boundaries | Role choice now routes to Players, first pack, Concepts, and Developers |
| `getting-started.mdx` | Discovery, manifest, first patch, report, reload, debug, multiplayer, diagnosis | Pack-author tutorial remains canonical |
| `lint-your-pack.mdx` | Standalone linter, KPatchwork policy, installation, roots, output, limits | Tool-choice and example indexes link here |

## Tutorials

| Route | Preserved task |
| --- | --- |
| `tutorials/item-icon-recipe-schematic` | Item, icon, recipe, schematic, and unlock chain |
| `tutorials/research-trees` | Research tree, schematics, nodes, roads, and branch edits |
| `tutorials/existing-schematic-unlock` | Add a recipe to an existing schematic |
| `tutorials/localizing-your-pack` | New and overridden text, cultures, and iteration |
| `tutorials/tag-based-bulk-balancing` | Register tags and patch matching content in bulk |
| `tutorials/conditional-multi-mod-packs` | Mod, version, and class conditions for optional integrations |
| `tutorials/debugging-a-pack-that-wont-apply` | Ordered runtime diagnosis |
| `tutorials/renaming-content-safely` | File, ID, pack-ref, and redirect rules |
| `tutorials/editing-another-mods-data-assets` | Patch KAPI and Refined R&D assets |
| `tutorials/from-live-edits-to-a-shareable-pack` | Current Runtime and Packs workspaces, export, save, reload, and distribution |

## Complete examples

| Route | Preserved example |
| --- | --- |
| `examples/balancing` | Recipes, items, resources, equipment, progression, vehicles, creatures, filters, and bulk edits |
| `examples/power-and-machines` | Power, machines, extraction, pipes, storage, drones, and actor patches |
| `examples/building-chain` | Buildable, descriptor, recipes, schematic, and sink points |
| `examples/end-to-end-pack` | Item through localization, data assets, integrations, and redirects |
| `examples/kapi-data-assets` | KAPI air, cleaner, miner, slug, allow-list, and Delivery assets |
| `examples/delivery-task` | Complete Delivery task graph, parents, Endless, and unlocks |
| `examples/repeat-purchase-schematic` | Migration from removed repeat-purchase unlocks |
| `examples/unlocks-catalog` | Current unlock catalog routing |

The example index now also links the maintained
[KPatchwork DataForge packs](https://github.com/Satisfactory-KMods/KPatchwork/tree/main/DataForge).

## Authoring features

| Group | Preserved pages and contracts |
| --- | --- |
| Patch model | `patching-cdo`, `property-types`, `operations`, `targeting`, `actor-selectors` |
| Pack control | `conditions-and-packs`, `templates`, `pack-configuration`, `category-reorder`, `event-rules` |
| Runtime registration | `game-tags`, `localization`, `sounds`, `sublevels`, `sinkpoints` |
| Generated content | `items`, `resources`, `buildings`, `unlocks`, `recipes`, `schematics`, `research-trees`, `custom-classes` |
| Runtime assets | `data-assets`, `curves` |
| World and removal | `removing-content`, `resource-node-placement`, `resource-node-visuals` |

The feature pages remain the canonical behavior explanations. The new Concepts section provides the
shared vocabulary and tool choice that these pages previously assumed.

## Reference

| Existing page | Preserved contract |
| --- | --- |
| `reference/yaml-schema` | Manifest, every built-in root, selectors, operations, values, conditions, and order |
| `reference/config-expressions` | Operands, syntax, precedence, and diagnostics |
| `reference/base-game-unlock-classes` | Base-game unlock catalog |
| `reference/mod-unlock-classes` | Installed-mod unlock catalog |
| `reference/availability-dependency-classes` | Availability dependency catalog |
| `reference/api-design` | Public handler and main-module API |
| `reference/handler-template` | Full native handler pattern |
| `reference/editor-integration` | `KDF.ApplyToAssets` contract |
| `reference/desktop-editor-lsp` | Datapack binding, completion, hover, and diagnostics |
| `reference/reflection-export` | Export, archive, recovery, validation, and limits |

New reference pages cover commands, template providers, and the Blueprint configuration API. They
fill source-backed gaps without removing detail from the existing pages.

## Contributor background

| Existing page | Preserved and corrected content |
| --- | --- |
| `background/architecture` | Lifecycle, stages, reflection, snapshots, actor patches, registrations, saves, multiplayer, determinism |
| `background/module-structure` | Public API, YAML, runtime, reflection, in-game UI, localization, third-party audio, and dependency rules |

## High-risk facts retained

- Pack `ref` and generated IDs remain save contracts.
- ID redirects do not repair a changed pack `ref`.
- Stage, dependency, priority, include, and path ordering remain deterministic.
- Reloadable, new-actor, cold, frozen, and native-helper behavior remain distinct.
- Multiplayer processes still need matching files; KDataForge does not transfer or checksum packs.
- Actor writes, removals, inventory changes, and resource-node changes keep their save caveats.
- Pack settings retain hot/cold and host/local behavior.
- Runtime localization and Unreal localization gathering remain separate workflows.
- Client audio requirements and dedicated-server placeholders remain documented.
- Reflection publication and recovery steps remain in the reference.
