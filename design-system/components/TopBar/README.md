Screen header: the iPhone status bar, then a 20 tall row with back, title and right-side controls.

**Use** `<div class="top">` with the status bar `.sb` and the row `.hd` (`size-topbar-row`): back `.ib` (20 icon, 44 tap area), optional title `<span class="ht text-topbar-title">` (16 semibold), a spacer `.sp`, then right-side items.

**Right side,** one of: points pill `.pts` (ink pill, gem + number; `.pts.lg` on the home screens), live label `.livel` (blue `.dot` + time in `color-text-muted`), share and info `.info`, close `.ib`.

**Background.** A frosted layer (blur 14) in `color-base-bg` from 90% to 72% that runs 20 past the bar and fades out, so content scrolls under it without a line. `top clear` removes it (art screens); `top paper` sits on white; on white screens the layer is white 92% → 78%.

**Spacing.** Row starts `space-page-group` (16) below the status bar and ends 8 above the content (`top tight`: 0). `top nohd` hides the row (status bar only). Over a full-bleed map or photo the back button is `ib float`: a 44 (`size-tap`) white disc, `space-20` from the left edge.

Don’t: put more than two items on the right, or a title longer than one line.
