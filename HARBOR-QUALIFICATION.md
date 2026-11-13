# Harbor Paint qualification

Experimental Windows portable fork, 2026-11-13.

- Optimized native Windows release build passed.
- Six portable/settings-path tests passed, including isolation and unwritable-folder fallback.
- The mixer, mixing palette, brush rack and palette persistence are preserved from the shared-document source branch.
- The shared host is built separately as Harbor Studio.

Limitations: the separate PDF Binder/import branch is archived, not integrated into this build. Legacy upstream installers are not Harbor installers. Optional Arabic and Thai font faces were unavailable in the selected font checkout; fallback rendering has not been independently qualified. No signed installer, broad platform qualification or production release is claimed.

Original authorship, source history and license notices are retained. Original installed applications and personal documents were not replaced. Existing E: build caches were reused.

Additional scoped checks passed: strict Clippy for the desktop app and UI (all targets), formatting after normalizing inherited whitespace, WASM UI compilation, and architecture layers (30 crates, no violations). The successful Studio host regression run also exercises the Paint UI and editable vector round trip.

Final regressions: six palette-filtered engine tests and six mixer-brush tests passed. Coverage includes deposit/mix/pickup/undo/presets without document loss, floating-selection preservation, hostile palette inputs, wet/dry/load behavior, and matching a frozen mixer kernel across color models, sample depths and spatial paint loads.
