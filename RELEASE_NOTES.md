# Release Notes

## v1.0.2
GH#651 Hub publish — republish to populate `nodes[].content` in object_manifest for prompt nodes. The /api/shared/<slug>/<v>/metadata endpoint now exposes `nodes[].content` for type='prompt' (GH#650 / GH#651), used by the engine validator's dep-aware loop-body `{{loop.item}}` interpolation check. Pre-fix publish-skrpt.mjs stripped content uniformly; aba4ccd7 preserves it for prompts. No content changes from v1.0.1; signed-bundle data identical, only D1 object_manifest gains the `content` field.

## v1.0.1
GH#638 Row 11 — republish with `manifest.id` aligned to Hub catalogue UUID. Pre-K-037 v1.0.0 bundles carried a local `manifest.id` that differed from the catalogue's UUID for this slug, causing engine STEP 4d strict-UUID match to halt consumer installs (`ComposedStagingError`). Row 5 (`0d9c9dbe`) reconciled the source file but did not republish the signed bundle; v1.0.1 ships the corrected `manifest.id` end-to-end. No content changes.

## v1.0.0
Initial catalogue release as independent shared object (GH#612 Wave 3).
