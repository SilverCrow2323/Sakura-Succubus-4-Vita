# Project: Sakura Succubus IV — PlayStation Vita port

## Purpose
Maintain the Vita package shell and port-specific metadata for Sakura Succubus IV. The repository is a Vita port distribution/packaging surface, not the original game's source repository.

## Users and use cases
Vita owners install the VPK and provide their own legally obtained original game files. Maintainers verify SFO identity, LiveArea assets, source attribution and package integrity. Testers report runtime behavior from physical hardware.

## Scope and boundaries
In scope: Vita title metadata, LiveArea assets, port instructions, compatibility notes and build provenance. Out of scope: redistribution of the original game's proprietary game/ directory, DRM/license bypass, or changing the Ren'Py Vita runtime.

Original game source: https://store.steampowered.com/app/1466690/Sakura_Succubus_4
Ren'Py Vita tool reference: https://github.com/SonicMastr/renpy-vita

## Target and dependencies
- PlayStation Vita / PlayStation TV with a compatible homebrew environment.
- Ren'Py Vita runtime, VitaShell and separately supplied original game files.
- Rebuilds must record exact runtime/tool revisions, input build identifier and output VPK SHA-256.

## Package architecture
- sce_sys/param.sfo: expected TITLE_ID RNPYSS004; title Sakura Succubus IV; version 1.00.
- sce_sys/icon0.png, pic0.png and livearea/contents/: package presentation.
- README.md and wiki-source/: installation, credits, project status and troubleshooting.
- Original game assets are user-supplied at the path described in the README.

## Safety and quality
Do not commit proprietary game data or user saves. SFO parsers must validate offsets and lengths. Installation notes must separate confirmed behavior from assumptions. CI package checks do not certify gameplay or device compatibility.

## Verified baseline
The tracked SFO reports RNPYSS004, Sakura Succubus IV and 1.00. The repository tracks Vita package metadata and port/runtime files; original game content is expected to remain external. Physical-device runtime qualification remains open.
