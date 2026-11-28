# Roadmap — Sakura Succubus IV Vita port

## P0 — Preserve package identity
- [x] Track SFO metadata and LiveArea assets.
- [x] Document upstream game source and the separation of user-supplied game data.
- [ ] Compare the released VPK against RNPYSS004 metadata and record its SHA-256.

## P1 — Package integrity
- [x] Add an offline SFO parser regression test with bounds checks.
- [x] Verify title ID, category, title and application version in CI.
- [x] Verify PNG signatures and LiveArea XML.
- [x] Reject an accidentally committed original game/ payload.
- [ ] Pin the exact Ren'Py Vita runtime/tool revision for reproducible builds.

## P2 — Runtime qualification
- [ ] Install on a physical PS Vita and record model, firmware, storage and free space.
- [ ] Verify first boot, game-file discovery, save/load, audio, suspend/resume and repeated launch.
- [ ] Record title-specific visual/performance findings with reproducible steps.

## P3 — Maintenance release
- [ ] Rebuild from a documented input game build and pinned runtime.
- [ ] Compare generated package metadata and assets against the reviewed baseline.
- [ ] Publish notes and checksums only after physical-device qualification.

## Acceptance
CI passes; SFO remains RNPYSS004; no original game payload is tracked; LiveArea assets are valid; any release candidate has a separate physical Vita report. CI is not hardware certification.

## Release target
Maintain existing port version 1.00; this change does not propose a release or version bump.


## Additional automated gate — 2026-11-28

The integrity suite now checks that the LiveArea `image` and `startup-image`
references are unique plain filenames confined to `sce_sys/livearea/contents`.
It also verifies the PNG signature, IHDR marker and non-zero dimensions for
`icon0.png`, `pic0.png`, the LiveArea background and startup image.

These checks validate package structure only. They do not prove visual quality,
controller behaviour, runtime boot or gameplay on a physical Vita.
