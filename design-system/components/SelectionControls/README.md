Checkbox, radio and the round select mark, off and on.

**Checkbox** `<span class="chk">` with a check icon: 24, radius `radius-xs` (8), 1.5 border (`stroke-select`) in `color-border-control` on white; on: `color-background-interactive` fill, `color-border-strong` border, white 14 check. Used in checklists (with a `plus10` points pill at the end of the row: muted until earned, ink once earned).

**Radio** `<span class="radio">`: `size-control-radio` (20), `stroke-select` (1.5) in `color-border-control`; inside an element with `on` the border turns `color-border-strong` and a 10 ink dot appears (`size-control-radio-core`).

**Select mark** `<span class="sel">` with a check icon: `size-control-checkbox` (24) circle, `stroke-select` (1.5) in `color-border-control`, white 50% fill; inside `on` it fills with ink and shows a white check. It lives in Tiles.

Put `on` on the row or tile, not the control, and set `aria-checked` on the button that holds it.

**Select mark sm** `sel sm`: 20 (`size-control-radio`), for a finished step at the end of a row (“A valid government ID ✓”).

All three off states (checkbox, radio, select mark) share one border: 1.5 `stroke-select` in `color-border-control`.
