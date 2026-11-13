# Harbor Paint

Independent native painting editor maintained for @durtyrobbin, derived from PhotoCraft.

Preserves our live mixer brush, movable mixing palette, brush rack, palette knife and painting-tool preferences. The shared-canvas adapter also supports the separate Harbor Studio paint/vector host.

## Build

Clone harbor-paint and harbor-studio as sibling directories (the shared view contract lives in harbor-studio/crates/canvas). Use the existing documented Rust dependencies and optional CRAFT_FONTS_DIR, then `cargo build --release -p photocraft`.

The Windows portable application is Harbor-Paint.exe with portable.txt. It uses HarborPaintData; HARBOR_PAINT_CONFIG_DIR can explicitly choose a different settings directory. Native .pcraft documents and internal crate names remain compatible.

For the experimental editable-vector toggle, also clone harbor-vector beside these repositories and build harbor-studio. Shared projects save embedded native vector contents in .pcraft; this is not a flattened-image-only handoff. The shared host currently opens PNG, JPEG and .pcraft.

Only Windows portable builds are being qualified. Legacy upstream installers are not Harbor installers.

## Provenance

Fork base: 12abe500e33083de5100630558e1dee7028e2cbc, shared-document-studio. Original project: https://github.com/storytold/photocraft. Full history, credits, MIT/Apache licenses and third-party notices are retained. This is not an official ArtCraft product.

Development status: experimental source fork; Windows release compilation passed. See HARBOR-QUALIFICATION.md for validation and limitations. No signed installer or production release is claimed.

## PDF work

This shared-document branch prioritizes the mixer, palette and editable-vector integration. The separate [PDF Binder/import branch](https://github.com/durtyrobbin/harbor-paint/tree/archive/pdf-binder-2) and [earlier live mixer branch](https://github.com/durtyrobbin/harbor-paint/tree/archive/mixer-brush-live) are preserved online with their original history. PDF Binder/import is not integrated into this build. Do not assume this executable imports PDFs.
