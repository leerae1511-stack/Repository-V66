# Tool Pocket Generator V68

V68 is built directly from V67. V65 was rejected and was not used.

## V68 scope

V68 retains the three V67 fixes and restores the confirmed clean New Tool work-area behaviour. No other functional area was intentionally changed.

### 1. JSON Export on iPad
- Retains the complete editable worksheet export, including the embedded current photo.
- Uses `application/json` with a `.json` filename to restore the known-working JSON handling.

### 2. Set Dimensions From Physical Grid after manual editing
- The measured physical Length × Width replaces the working dimensions when photo/ruler measurement succeeds, even if manual edits made the outline envelope larger.
- The edited outline is preserved in physical millimetres and translated/re-centred only.
- No scaling, distortion, clipping or point deletion.
- The orange rectangle remains a reference frame, not a clipping boundary.

### 3. FR/STL geometry
- STL export adds only the finger-relief cap/extension volume instead of exporting the complete expanded profile a second time.
- Main pocket Z architecture remains unchanged.

### 4. Confirmed New Tool work-area regression
- A genuinely new/empty tool now opens with the profile work area blank: no orange reference rectangle and no grid are drawn while there are zero outline points.
- Once an outline point exists (manual drawing/add-point or photo detection), the normal reference rectangle/grid and profile display return.
- This change is limited to the empty-state drawing path; it does not alter dimensions, detection, editing, grid measurement, imported projects, or completed profiles.

## Whole-generator impact review

The three V67 fixes were retained unchanged. The only additional functional change is the confirmed empty New Tool display regression described above. Existing saved/imported project state, detection, manual editing, geometry checking, FR placement/data, and STL main-pocket architecture were not otherwise changed.

A related existing constraint remains intentionally unchanged: subsequently dragged points are clamped to the orange reference frame. This was identified during the Physical Grid review but is outside the agreed scope.

Actual iPad/Safari JSON download handling and STL Viewer rendering must still be device-tested.
