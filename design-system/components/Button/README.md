Full-width pill button, 46 tall, for the actions of a screen or sheet.

**Use** `<button class="btn ink">` for the one main action, `btn paper` for a second action on a tinted ground, `btn plain` for a quiet action (“Missing something?”, “Cancel”). One `ink` per screen.

**Anatomy.** Height `size-button-height` (46), radius `radius-pill`, label in `text-button` (16 semibold), icon gap `space-card-line` (8). Width is 100% of its column: buttons live in a Footer, a Sheet footer or a card, never side by side.

**Colours.** `ink`: `color-background-interactive` with `color-text-on-inverse`. `paper`: `color-background-white` with `color-text-text`. `plain`: transparent.

**States.** Pressed scales to .98. `disabled` drops to opacity `disabled` (.35). Busy: add `busy` and put `<i class="spinner on-dark"></i>` before the label (“Paying…”); the Spinner atom, on-dark variant.

**In a footer** a `paper` or `plain` right after an `ink` loses its fill, drops to 40 tall (`size-button-text-height`) and sits 8 below the main one, so the pair reads as one main action plus an alternative.

Don’t: put two `ink` buttons together, shorten a button to fit text, or add borders.

**Small** `btn sm`: 40 tall (`size-button-text-height`), `text-row-title` size, 14 icon. For buttons inside cards (“Earn more points”, “Got it”).

**More fills.** `btn muted`: `color-background-muted` (“Got it” on the rewards intro). `btn link`: no fill, `text-caption` in `color-text-muted`, auto width (“See my rewards”).
