Text input and text area on a muted fill.

**Use** `<input class="field">` or `<textarea class="field" rows="3">`. Fill `color-background-muted`, 1.5 border `color-border-border`, radius `radius-inner` (12), padding 14 × 16, `text-body` with `leading-relaxed` (1.45); placeholder in `color-text-soft`. Focus: border `color-muted`, fill white. `field paper`: white fill and a `stroke-control` border, for a field on a tinted sheet. Inputs are 48 tall (`size-field-input`), text areas 88 (`size-field-textarea`).

On phones the field text is 16 so iOS does not zoom.

**Inputs in forms** (address, card) use `<input class="field paper">` inside a `.pf` with its `text-label` label: white with the `stroke-control` border, 48 tall (`size-field-input`). The muted default is for a single field on its own (SMS number on m4, note in a sheet).
