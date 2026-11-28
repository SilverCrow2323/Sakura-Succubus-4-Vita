# Project definition — Sakura Succubus 4 Vita

## Product and boundary
A PS Vita Ren'Py package shell for **Sakura Succubus 4**. It supplies Vita application metadata, LiveArea assets and install guidance, not the original PC game.

## Upstream and runtime
- Original game: [Sakura Succubus 4 on Steam](https://store.steampowered.com/app/1466690/Sakura_Succubus_4/).
- Runtime/tool lineage: [Ren'Py PSVita Distribution Tool](https://github.com/SonicMastr/renpy-vita).
- Original game files remain user-supplied and must not be added without redistribution rights.

## Users and target
PS Vita users installing through VitaShell. The README reports possible Settings and Load/Save glitches on recent Winged Cloud titles; retain this caveat pending device retest.

## Install contract
The README specifies `ux0:/app/RNPYSS004/` as the original `game/` destination. SFO identity must match this path.

## Architecture and dependencies
Static package shell: SFO, icon/pic artwork, LiveArea template, background/startup images and documentation. External dependencies are the original game data and Ren'Py Vita runtime.

## Security and quality
Validate SFO, PNG and LiveArea paths. Preserve the known-bug note and avoid unsupported firmware/performance claims. Documentation is English.

## Verified baseline
The repository contains package metadata and wiki source, not the full original game. Automated checks prove structure only.

## Release acceptance
Consistent SFO/app path, valid LiveArea assets, correct attribution, and physical Vita verification of boot, Settings, Load/Save, Quick Save/Load, suspend/resume and performance.