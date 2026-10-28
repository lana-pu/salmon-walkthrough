Full-width pill button, 46 tall, for the actions of a screen or sheet.

**Use** `<button class="btn ink">` for the one main action, `btn paper` for a second action on a tinted ground, `btn plain` for a quiet action (“Missing something?”, “Cancel”). One `ink` per screen.

**Anatomy.** Height `size-button-height` (46), radius `radius-pill`, label in `text-button` (16 semibold), icon gap `space-card-line` (8). Width is 100% of its column: buttons live in a Footer, a Sheet footer or a card, never side by side (the one exception: two `btn sm soft` in a card).

**Colours.** `ink`: `color-background-interactive` with `color-text-on-inverse`. `paper`: `color-background-white` with `color-text-text`. `plain`: transparent.

**States.** Pressed scales to .98. `disabled` drops to opacity `disabled` (.35). Busy: add `busy` and put `<i class="spinner on-dark"></i>` before the label (“Paying…”); the Spinner atom, on-dark variant.

**In a footer** a `paper` or `plain` right after an `ink` loses its fill, drops to 40 tall (`size-button-text-height`) and sits 8 below the main one: the text link. In `ft sec-w` the `paper` keeps its white fill and full height: the white pill. On a white sheet `btn soft` is the grey pill.

Don’t: put two `ink` buttons together, shorten a button to fit text, or add borders.

**Small** `btn sm`: 40 tall (`size-button-text-height`), `text-row-title` size, 14 icon. For buttons inside cards (“Earn more points”, “Got it”). `btn sm soft` has a `color-background-muted` fill, for actions inside a white card; two of them may sit side by side, each half the width (“Ask a question” and “Profile” on the person card, w6).

**More fills.** `btn muted`: `color-background-muted` (“Got it” on the rewards intro). `btn link`: no fill, `text-caption` in `color-text-muted`, auto width (“See my rewards”).

**Under the main button.** Three looks with a meaning each. Ink: the main action. White pill (`btn paper` in `ft sec-w`; on a white sheet the grey `btn soft`): a second, equal-weight action (“Show directions”, “View receipt”, “Retake”). Text link (`btn plain` or `btn paper` without `sec-w`): leaving or undoing: cancel, skip, leave, back, “Something’s wrong”.

## Hit area

Every button reaches `size-tap` (44 × 44) through the shared invisible `::after`; `sm`, `paper` and `plain` buttons stay 40 tall visually.
