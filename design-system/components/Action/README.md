Something to do while you wait: Get ready, Take a seat, Game break, About Salmon, Your purchase.

**One data source, two layouts.** `ac-tile`: half width in the grid, `size-action-tile` (168) tall, title, short line, footer (go button, amenity icons, held time or Done). `ac-feat`: full width on top, `size-action-feature` (155) tall, with the illustration on the left and the text column `size-action-feature-body` (219) wide, “Recommended” (or ✓ Done), title, text and a link. Any action can be the feature or a tile; which one is on top is decided by the meeting state, not by the markup.

**Surface.** The card reads its colours from surface variables: `--surface`, `--surface-image`, `--on-surface`, `--on-surface-muted`, `--go-surface`, `--surface-icon`. Surfaces: `s-paper` (white), `s-tile` (`gradient-tile`), `s-ambient` (`gradient-ambient`), `s-feature` (`gradient-feature`), `s-hero` (`gradient-hero`), `s-ink` (`color-background-inverse`). Game tiles use the same mechanism with `s-plate` (`gradient-plate`), `s-warm` (`gradient-warm`) and `s-sunrise` (`gradient-sunrise`), one surface per game. Monochrome mode puts every tile on paper; colour mode picks one surface per action and arrangement in data (`AC_SURFACE`).

On ink, illustrations need a light version (Game break has one).
