Who or where — Mark, the meeting point — as one set of data in three layouts.

**Layouts.** `fact chip-l`: 44 tall (`size-tap`) white pill, 36 picture, caption-medium label, up to two lines; it lives in the docked bar on the ticket. `fact tile-l`: card in the left column of the ticket, picture, label, title, optional line, link line at the bottom (`size-fact-link`), at least `size-fact-tile` tall. `card`: a media row (photo or icon holder lg, label, title, line, chevron).

**Picture.** A person uses an avatar (md in the tile, sm in the chip); a place uses an icon holder (ink in the tile; in the chip the gradient holder with the chip icon, 36 like the avatar).

**Docking.** On scroll the tile morphs into the chip. The dock reads the chip's size, padding and label position from this component, so changing the chip changes the dock.

**Text.** Tile label `text-caption`, value `text-stat-value` (24 semibold, tightest tracking), detail `text-body`.
