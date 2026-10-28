Square-ish choice tile: a title, a line of detail and a select mark; the chosen one turns into the soft gradient.

**Use** `<button class="tile" role="radio" aria-checked>` in a 2- or 3-column grid with `space-grid-gap` (16) — or a horizontal scroller (`terms-row`) for terms. Inside: a `stack g12` (with `space-4` above it) holding `bm text-row-title` and `c sec text-row-subtitle`, then a Select mark `.sel` at the bottom right.

**States.** Off: `color-background-white`. On (`tile on`): `gradient-tile` fill and a filled select mark. Pressed scales to .97.

**Icon tile** `tile cat-tile`: 86 tall (`size-tile-sm`); a `cat-top` row (24 high) with the icon in `lead-ic lg bare` (`color-icon`) on the left and the select mark on the right, title below; used for picking categories. On: `gradient-tile`, like every tile.

**Game tile** `tile lg game surface s-<surface>`: 118 tall, picture slot (`size-game-slot`) on the left, title, line and meta on the right. The line stays `color-text-muted` on every surface.

Radius `radius-card` (20), padding `space-card-pad-lg` (16).

## Text on a selected tile

A selected tile (`gradient-tile`) switches `color-text-muted` to `color-text-muted-on-tint` for everything inside it, so captions keep 4.5:1.
