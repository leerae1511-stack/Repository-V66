# Tool Pocket Generator V66

V66 is built directly from the working V61 build. The V61 physical-grid process is preserved unchanged. Only the three agreed V61 issues are fixed.

## V66 fixes

1. **Remove Photo display**
   - Remove Photo now clears the photo canvas pixels as well as removing the photo reference.
   - Profile points and tool-outline geometry are not changed by this action.

2. **JSON export on iPad**
   - JSON export uses the same downloadable-file handling as V60 (`application/octet-stream`).
   - The JSON contents/structure are not otherwise changed.

3. **STL / claw / finger-relief geometry**
   - STL export is restored to the V60 working positive pocket-cutter architecture.
   - Main cutter volume is from `Tray Thickness - Pocket Depth` up to the tray top.
   - Enabled finger-access reliefs use the actual `fingerCutoutAt()` profile and their configured depth.
   - The V61 correction allowing finger-relief depth up to tray thickness is retained.

## Explicitly NOT changed

- Set dimensions from physical grid
- Physical grid measurement/dimension workflow
- Tool-outline detection workflow
- Manual point editing
- Rectangle sizing/repositioning behaviour
- Finger-relief placement workflow
- Geometry-check rules, except the already-existing V61 FR-depth rule
- Saved-tool workflow

V66 is a V61-based build, not a V62-based build.

See V66_FIX_DETAILS.txt for the exact scope and fixes.
