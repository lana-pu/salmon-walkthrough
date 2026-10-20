# Gradients

Salmon’s gradients come from the Figma kit’s paint styles. Three of them are layered recipes: a linear base, soft radial glows and a veil on top. Each one is a single token in code (`--gradient-hero`, `--gradient-ambient`, `--gradient-feature`, `--gradient-warm`, `--gradient-plate`) and every element that uses it reads that token. The layers stretch with the element the way Figma stretches them, so one token fits any size.

Every layer colour is a token. A few come from the palette; the rest are the `glow-*` tones, kept in their own group (Gradient colours) outside the palette because nothing but the gradients uses them. Change a glow token and every gradient that uses it follows.

## gradient-hero

Hero · coral and lilac. Action tile “Your purchase”, product card, selected delivery, Pinoy Henyo tile, Points fact tile.

| # | Layer | Stops | Layer opacity |
|---|---|---|---|
| 1 | Linear | `glow-lilac-3` @0, `glow-peach-10` @35, `glow-rose-7` @70, `blue-350` @100 |  |
| 2 | Radial glow | `glow-rose-9` 65% @0, `glow-peach-11` 25% @50, `glow-periwinkle-4` 0% @100 |  |
| 3 | Radial glow | `glow-periwinkle-3` 45% @0, `glow-rose-6` 0% @100 |  |
| 4 | Radial glow | `glow-peach-9` 50% @0, `glow-lilac-2` 0% @100 |  |
| 5 | Veil | `neutral-0` at 49% | |

## gradient-ambient

Ambient · lilac with a sky wash. Action tiles “Take a seat” and “About”, Trivia tile, Time taken fact tile.

| # | Layer | Stops | Layer opacity |
|---|---|---|---|
| 1 | Linear | `glow-lilac-3` @0, `glow-peach-3` @35, `glow-peach-6` @70, `blue-350` @100 |  |
| 2 | Radial glow | `glow-orchid-1` 65% @0, `glow-peach-11` 25% @50, `glow-periwinkle-4` 0% @100 |  |
| 3 | Radial glow | `glow-rose-8` 45% @0, `glow-rose-6` 0% @100 |  |
| 4 | Radial glow | `glow-orchid-2` 50% @25, `glow-lilac-2` 0% @86 |  |
| 5 | Linear | `blue-150` @13, `glow-peach-4` 0% @89 |  |
| 6 | Veil | `neutral-0` at 20% | |

## gradient-feature

Feature · warm cream. The “Get ready” feature card.

| # | Layer | Stops | Layer opacity |
|---|---|---|---|
| 1 | Linear | `glow-lilac-4` @0, `glow-rose-2` @40, `glow-peach-2` @70, `glow-rose-5` @100 |  |
| 2 | Radial glow | `glow-periwinkle-1` @15, `glow-rose-1` 0% @81 | 50% |
| 3 | Radial glow | `glow-peach-8` @48, `glow-rose-4` 0% @100 | 50% |
| 4 | Radial glow | `glow-peach-1` @0, `glow-peach-7` 0% @100 | 50% |
| 5 | Veil | `glow-sky-1` at 20% | |

## gradient-warm

Warm · one layer. Escape room tile, third place on the podium.

| # | Layer | Stops | Layer opacity |
|---|---|---|---|
| 1 | Linear | `glow-peach-5` @0, `glow-lilac-1` @100 |  |

## gradient-plate

Plate · one layer. Colour together and Tangram tiles.

| # | Layer | Stops | Layer opacity |
|---|---|---|---|
| 1 | Linear | `glow-rose-3` @0, `glow-periwinkle-2` @100 |  |

Not used in the product (kept in Figma only): pearl, cool, mist, fraynbow, tile-blue, tile-warm, stol, stol2, podi. The podium uses its own spots.
