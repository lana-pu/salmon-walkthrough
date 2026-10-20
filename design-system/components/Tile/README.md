Square-ish choice tile: a title, a line of detail and a select mark; the chosen one turns into the soft gradient.

**Use** `<button class="tile" role="radio" aria-checked>` in a 2- or 3-column grid with `space-grid-gap` (16) — or a horizontal scroller (`terms-row`) for terms. Inside: a `stack` with `bm text-row-title` and `c sec text-row-subtitle`, then a Select mark `.sel` at the bottom right.

**States.** Off: `color-background-white`. On (`tile on`): `gradient-tile` fill and a filled select mark. Pressed scales to .97.

**Icon tile** `tile cat-tile`: 86 tall, icon top left, select mark top right, title below; used for picking interests. Its on-state gradient (`#e4e0f6 → #f6dfe6`) is not a token yet.

Radius `radius-card` (20), padding `space-card-pad-lg` (16).
