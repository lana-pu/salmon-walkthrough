Bottom sheet over a dimmed screen: grabber, close, header, content and its own footer.

**Use** `<div class="ovl"><div class="dim"></div><div class="sheet" role="dialog" aria-modal="true">…</div></div>`. Inside: `.grab` (46 × 4, `color-hairline`), close `.sh-x` positioning an Icon button `ib close` (28, 14 icon), then `.sh-in` with a header `.sh-hd` (`h4 text-sheet-title` + `c text-caption`, 8 apart, 24 below) and the content, then `.sh-ft` with the buttons.

**Surface.** White, top radius `radius-sheet` (28), up to 88% of the screen; the dim is `color-scrim`. Padding: 28 top (`space-sheet-pad-top`), 24 sides, 32 at the end; the footer gets the same glow as the screen Footer.

**Option rows** `<button class="boxrow">`: icon holder + title + subtitle + radio or chevron, 16 padded, radius `radius-card`, 2 inner ring in `color-base-bg`; chosen (`boxrow on`): `gradient-peach`, no ring. Rows stack 8 apart.

Close on the X or a tap on the dim. One sheet at a time.
