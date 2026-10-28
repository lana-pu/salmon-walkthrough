Row with a round icon holder, a title and a subtitle, and an optional trailing chevron, info button or value.

**Use** `<div class="rows">` (inside a Card) with `<div class="row">` items: `<span class="lead-ic">` + icon, `<span class="tx">` with `b text-row-title` (or `text-body`) and `c text-caption` (`text-row-subtitle`), then the trailing part. Make the row a `<button class="row">` when it opens something, and end it with `.chev`.

**Anatomy.** Icon holder `lead-ic` on `gradient-holder` with the icon in `color-icon-muted`. Sizes: default 24 (`size-icon-holder-sm`) with a 14 icon; `lead-ic md` 36 with a 16 icon (sheet options, tiles); `lead-ic lg` 44 with a 20 icon (delivery options); `lead-ic xl` 56 with a 20 icon (`size-icon-holder-xl`, locked reward). Size and fill are independent: any size (sm · md · lg · xl) takes any fill (gradient · `muted` · `paper` · `peach` · `ink` · `bare`), 24 combinations. `ink` puts a white icon on ink; `bare` drops the disc but keeps the size. In a box row a bare holder is 20, to line up with the radios. Gap `space-card-icon-gap` (12); title to subtitle `space-card-line` (8). Rows are `space-card-pad-lg` (16) tall-padded and 12 apart. `rows-c` removes the row padding for compact lists.

**Delivery option** `ful`: `size-option-row-lg` (128) tall, `lead-ic lg paper` holder, title `text-card-title` and line `text-body` 14 apart, radio at the end; off is muted, on is `gradient-hero`.

**Status banner** `sbanner`: the same row on a muted fill, not tappable; `sbanner paper` (white) and `sbanner tint` (`gradient-tile`, padding 16 × 12, icon in `color-icon`).

**Trailing.** Chevron 16 in `color-text-soft`; info `.info` (20, ink circle); a value in `text-body`.

**Title weight.** A row you can tap (chevron, checkbox, toggle, opens something) takes `text-row-title` (14 semibold); a row that only informs takes `text-body` (14 regular). Same rule in boxed option rows: they are always tappable, so always semibold.

**Option lists.** Every option row has an icon holder at the start (`lead-ic md`) and the radio at the end, as in Payment method. A list you cannot tap is never boxed: it is plain rows in a card (`card rows-c`, muted on a white sheet, white on the grey page).

**Density.** Two spacings on purpose: a list that is the main thing on the screen gets roomy rows (`space-card-pad-lg` padding); a list that supports something else is compact (`rows-c`, 20 between rows).

Don’t: put two lines of subtitle under a short title if a Key–value line says it better.

**One weight per list.** When a static list has a single row that opens something and that row already shows it with a trailing icon (m3, the ID row with ⓘ), the row keeps the regular title so the list reads as one. In code: `data-plain` on the row.

## Hit area and tinted rows

A tappable row (link, button or `data-go`/`data-act`) reaches `size-tap` through the shared invisible `::after`. On a selected row (`gradient-peach`) the subtitle uses `color-text-muted-on-tint`, set by the row itself.
