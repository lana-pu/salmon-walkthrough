Salmon helps people in the Philippines buy a phone in monthly parts and meet a real person, Mark, in the mall to finish the deal. The interface is calm, warm and light: soft pastel haze, white cards, one black action, and type that does most of the work.

## Three layers, named as in Figma

Token names follow the Figma kit, with `/` written as `-`: `space/card/pad-lg` is `space-card-pad-lg`, `color/text/muted` is `color-text-muted`. Values come from production; where Figma had a different value, the token's note says so.

- **Foundations**: raw values named by what they are. The palette (`neutral-*`, `mauve-*`, `blue-*`, `lilac-*`, `pink-*`, `peach-*`…), `space-2` … `space-48`, `radius-8` … `radius-full`, `size-4` … `size-393`, `stroke-100` … `stroke-200`, and the type scale (`font-size-*`, `font-weight-*`, `leading-*`, `tracking-*`). Figma: `*/primitive/*`.
- **Semantic** (Figma "Salmon Design"): `color-base-bg`, `color-paper`, `color-ink`, `color-secondary`, `color-muted`, `color-hairline`, `color-status-live`, `color-haze-*`, `color-artwork-line`; `space-page-*`, `space-card-*`, `space-control-*`, `space-pill-*`, `space-text-*`; `radius-card`, `radius-inner`, `radius-pill`…; `size-icon-*`, `size-icon-holder-*`, `size-control-*`, `size-tap`…; `stroke-icon`, `stroke-control`; `gradient-*`; the text styles `h1` … `caption-medium`. Each points at a foundation.
- **Roles** (Figma "Salmon WF"), for colour: `color-text-text`, `color-text-muted`, `color-text-soft`, `color-text-on-inverse`, `color-background-white`, `color-background-sunken`, `color-background-muted`, `color-background-interactive`, `color-border-strong`, `color-border-border`, `color-border-dashed`, `color-camera-*`. Each points at a semantic colour.
- Screens and components use semantic and role tokens. One exception: a one-off layout value (a gap that appears on one screen only, an offset inside a hero) may read a scale step directly (`space-16`). As soon as the same spacing repeats as a pattern, it gets a semantic token.
- To rebrand, change foundations. To change what a role looks like, repoint it to another semantic token or foundation. A new need gets a new semantic or role token first.
- Colour tokens are live aliases on this page. Spacing, radius, size and text styles carry their value and name their foundation in the note ("Semantic → space-24"). In the prototype all of them are live `var()` chains. Screens read roles and semantic tokens by their Figma names; the old short names (`--bg`, `--sec`, `--r-card`, `--g-select`) are gone. Footer anatomy keeps its own local variables (`--ft-x`, `--ft-b`, `--ft-gap`, `--ft-fade`), which point at the footer spacing tokens.

## Principles

- **One clear next step.** Every screen and sheet has at most one black button. Everything else is quieter.
- **Calm while you wait.** The ticket is where people spend the most time. It stays light, readable and in motion only when something actually changes.
- **Type first, decoration second.** Hierarchy comes from size and weight in `color-ink`, `color-text-muted` and `color-text-soft`, not from boxes, borders or shadows.
- **Flat surfaces.** Cards are `color-paper` on `color-base-bg`. No drop shadows on cards, sheets or buttons. Depth comes from the haze behind content and from motion.
- **Every pair readable.** Text meets 4.5:1 on its ground; large headings and marks meet 3:1. Every control has a 44px hit area.

## Voice and copy

- Write in English, sentence case, short and concrete: "Mark arrives in 5 minutes", "Check what you'll need", "Missing something?".
- Name the person. Mark is "Mark", not "your agent". The customer is "you".
- Say what happens next, with real numbers: "₱1,467 a month × 12 · 0% interest", "Price held until 3:45".
- Buttons start with a verb and say the outcome: "Set up meeting", "Invite a friend", "Show directions". A second action that declines reads like speech: "I'll just wait", "Skip for now".
- No emoji. Currency is the peso sign with comma thousands: `₱21,999`. Times are 12-hour: "3:20 PM".

## Color

- Screens sit on `color-base-bg`. Cards, tiles and sheets are `color-paper`. Inside a white sheet, nested cards use `color-base-bg`.
- Text is `color-text-text` for primary content and `color-text-muted` for everything secondary (sub-lines, captions, notes).
- `color-text-soft` is only for the quiet first line of large headings (the `em` in `h1`/`h2`) and for functional states such as disabled. Never use it for small text.
- The one strong surface is `color-ink`: the primary button, selected chips and pills, and the dark action tile. Text on `color-ink` is white; secondary text on `color-ink` is `color-text-on-inverse-muted`.
- Selection is shown with `gradient-peach` (rows in sheets) or `gradient-tile` (tiles), with text in `color-ink`.
- `color-status-live` marks live status (the pulsing dot), progress and the focus ring. It is never text.
- The haze tones belong to backgrounds and illustrations only: `haze-room-*` are the pale tones that fill the room (big, very blurred, low opacity), `haze-gather-*` the saturated tones that gather behind a hero.
- `color-status-danger` appears only as an outline or icon beside words, never as the only signal.

## Typography

- One family: DM Sans, weights 400–600 (`sans`).
- All text styles trim their box to cap height and baseline (`text-box: trim-both cap alphabetic`). Spacing is measured from cap height to baseline, so a "16px" gap looks like 16px.
- Type has the same layers as colour. Foundations: `font-size-*`, `font-weight-*`, `leading-*`, `tracking-*`. Styles (Figma text styles): `h1`, `h2`, `h3`, `h4`, `body-large`, `body`, `body-medium`, `caption`, `caption-medium`, and three display styles (`display-price`, `display-countdown`, `display-podium`). Roles name what a piece of text is for and point at a style; many roles share one style.
- Screens pick a role: `text-screen-title` (→ `h2`, often two tones: the main part in `color-text-text`, supporting words in `color-text-soft` via `<em>`; either part can come first; 32/33 on short phones), `text-screen-lead` (→ `body-large`), `text-section-title`, `text-sheet-title` and `text-card-title` (→ `h4`), `text-place-title` (→ `h3`), `text-body` and `text-toast` (→ `body`), `text-row-title`, `text-button` and `text-topbar-title` (→ `body-medium`), `text-row-subtitle` and `text-caption` (→ `caption`, in `color-text-muted`), `text-label` and `text-chip` (→ `caption-medium`), `text-hero-number` (→ `h1`).
- In code each style is also a set of tokens (`--type-h4-size`, `--type-h4-weight`, `--type-h4-leading`, `--type-h4-tracking`); base styles, text roles and component text (`--text-button-*`, `--text-chip-*`, `--text-topbar-title-*`, `--text-toast-*`) read them, so restyling `h4` restyles every place that draws h4.
- In code, text carries its role as a class next to the style (`class="h4 text-section-title"`); the role rules sit right after the styles, so a role can be restyled in one place. Buttons, chips, the top bar title and toasts take their role through the component (`.btn`, `.chip`, `.ht`, `.toast`).
- The iPhone system look (status bar, push, lock screen) has its own styles and stays off the scale.

## Spacing and layout

- The phone frame is 393 × 852. Side gutter is `space-page-margin` on screens, sheets and footers.
- Rhythm: `space-card-line` (8) between a title and its subtitle and between rows or cards in a list, `space-page-group` (16) under a section header, `space-card-pad-lg` (16) inside cards, `space-page-between` (24) between sections of the same group, `space-group-break` (32) between blocks that belong to different groups, `space-page-edge` (32) under the top bar, `space-sheet-end` (32) from content to the buttons in sheets.
- Cards in a grid sit `space-grid-gap` apart. Card padding is `space-card-pad-lg`, `space-card-pad-bottom-lg` when the card ends in text.
- The top bar is a 20px row: back arrow left, title beside it, actions right. The points pill is centred on the back arrow.
- Short phone screens (under 760px tall, as in a browser with its bars) tighten one-view screens so they fit without scrolling: smaller hero art, `space-page-pause` drops from 48 to 20 under heroes.

## Screen templates

Every screen and sheet uses one of ten layouts. The templates page shows each with a measured example.

- **Step** (21 screens): top bar, intro (two-tone title and lead), content, footer. The content is a list, a form, a guide or a summary in sections. Examples: m3, p2a, x2.
- **Collection** (m8, w2, a1): intro, a chips row from edge to edge, then a grid or a list.
- **Result** (13 screens): clear top bar, hero (art, title, lead, centred), then a reward, a card, the person card or the podium.
- **Message** (i4, i8, i10, x7): a short message in the middle of the free space.
- **Detail** (m1, pp, w3, m2): photo first — a photo under a top bar starts `space-page-edge-photo` (8) below it (pp, w3); a photo hero (`size-photo-hero` 302, `size-photo-cover` 196) or a hero number, the facts, then sections.
- **Ticket** (m6): ticket title and live label, the fact column next to the art, the actions; a sticky chip bar on scroll.
- **Camera** (i7, i9, w4c): dark ground, paper top bar, frame, shutter; no footer.
- **Map** (w4, w4m, w4a): full-bleed map with the map sheet docked at the bottom.
- **Play** (c2, c3): one big count or word card.
- **Sheet** (13 sheets): grabber, heading, body (options, list card, person, photo, invite card), Button pair or none.

Pause rule: `space-page-pause` (48) before a block of a different kind — a reward, the players, how it works, an optional extra; `space-group-break` (32) when the next block continues the same story (details, the next setting, the main choice). Message screens put the centre of their content at `layout-message-anchor` (42%) of the free height between the top bar and the first footer button.

Vertical rhythm for every scrolling template: `space-page-edge` (32) under the top bar; `space-group-break` (32) after the intro and above each section heading; `space-page-group` (16) under a heading; `space-page-between` (24) between blocks inside a section; `space-card-line` (8) between cards in a list. The scroll ends `size-footer-clear` (210) under the last block (`size-footer-clear-sm` 140 on short screens, `size-footer-clear-ticket` 150 on the ticket, `size-footer-clear-tall` 190 above the points footer). Sheets: `space-sheet-grabber` (6), `space-sheet-pad-top` (28), `space-sheet-head` (24), `space-sheet-end` (32).

## Footer and buttons

- Primary action: one `color-background-interactive` button, `size-button-height` tall, full width, `radius-pill`.
- Second action by meaning:
  - a useful alternative (View receipt, Show directions, Chat with Mark) is a `color-paper` button on screens, a `color-base-bg` capsule inside white sheets, `size-button-height` tall;
  - declining, skipping, cancelling, going back or reporting a problem is a text button, `size-button-text-height` tall.
- A lone action is always the `color-ink` button.
- The footer fades content out above the first button (`space-footer-fade`) and keeps `space-footer-bottom` below the last one: 32px for one button, 24px under a text button.

## Sheets

- Sheets are `color-paper` with `radius-sheet` top corners. The grabber is `color-hairline`, `size-grabber-width` wide, 6px from the top edge.
- Title (`h4`) sits 36px from the top edge, subtitle (`caption` in `color-text-muted`) 8px below it, content 24px below the subtitle.
- Blocks inside a sheet sit `space-card-line` apart; content ends `space-sheet-end` above the buttons.
- The close button is a 28px `color-base-bg` circle 14px from the top and 16px from the right. When a sheet opens with a photo, it moves inside the photo's corner.
- A sheet whose only action would be "Close" or "Cancel" has no footer. It ends with its content and is closed by the ✕ or a swipe down.

## Radii and surfaces

- `radius-card` for cards, tiles and rows; `radius-inner` for elements inside cards (QR plate, small images); `radius-pill` for buttons, chips, badges, avatars and icon holders.
- No strokes on icon holders or avatars. Dashed `color-slot-line` outlines are reserved for empty slots (add a player, waiting, free).

## Iconography

- One round line set on a 24 grid with a 1.5 line (`stroke-icon`) and round ends. Most icons come from Misha Naer’s round line catalog, thinned to 1.5; camera, gift, gem, store, truck, bowl, baby, sofa, stairs and the single sparkle are Salmon’s own. Dense icons are drawn a little smaller so the whole set carries one visual weight. No filled icons. See the Icons group.
- Four sizes, each with one job: `size-icon-xs` 12 in small pills, `size-icon-sm` 14 in 24 holders and controls, `size-icon-md` 16 next to text, `size-icon-topbar` 20 when the icon stands alone.
- Colour comes from four tokens: `color-icon` for icons that act or stand alone, `color-icon-muted` for icons that describe (holders, sheet close, badges), `color-icon-soft` for chevrons, `color-icon-on-inverse` on ink.
- Icons sit in round holders: `size-icon-holder-sm` with `size-icon-sm` in card rows. Holders use `gradient-holder`.
- Icons are never the only label of an action, except back (←) and close (✕).
- A new icon comes from the catalog first; draw one only when the catalog has nothing, at a 1.5 line and a 20–22 box.

## Illustration and imagery

- Illustrations are soft line drawings in `color-artwork-line` with pastel blooms and sparkles in `haze-gather-*` tones. They appear in heroes (80px, 64px on short screens) and on action cards.
- Behind heroes a slow pastel haze of blurred blobs breathes; it never carries meaning.
- Photos (places, the phone) sit in `radius-card` frames with a small white status badge in the corner.

## Motion

- Default ease for things arriving: `cubic-bezier(.2,.8,.2,1)`, 420–700ms.
- Playful pops (ticks, sparkles, points) use a soft overshoot such as `cubic-bezier(.3,1.6,.5,1)`.
- Cards that move to a new place use a spring with no visible overshoot (damping about 0.9) and travel on a gentle arc; colour changes travel with them.
- Screens slide in 400ms; sheets rise in 380ms and fall in 260ms.
- Respect reduced motion: animations collapse to an instant change.

## Interaction and accessibility

- Every control has a `size-tap` hit area, even when the visual is smaller (icons, the info dot, chips).
- Focus is a 2px `color-status-live` ring with 2px offset, shown only for keyboard use.
- Disabled buttons use the `disabled` opacity and stay in place.
- When a screen changes, focus moves to its title; when a sheet opens, focus moves into it and returns to the opener when it closes.

## Shadows and rings

- There are no drop shadows. Depth is haze plus motion.
- Rings are the only box-shadows: `ring-row` on box rows in sheets, `ring-live`, `ring-join` and `ring-select` as pulses, `ring-tick` and `ring-badge` as cut-outs, `focus` for keyboard focus.

## Haze

The haze is a stack of blurred colour blobs behind content, placed in the 393 × 852 frame. Each blob is `x, y, width, height, colour, opacity, blur`. It never carries meaning and is the first thing to drop on short screens.

- **actions** (Final results, home): `color-base-bg` top-left, `color-haze-sky` top-left, four `color-haze-apricot`/`color-haze-cream` blobs at 16% low on the right. Blur 150.
- **warm** (gathering, 40% group opacity): `color-haze-gather-peach` 90%, `color-haze-gather-lilac` 85%, `color-haze-gather-rose` 85%, rotated, blur 24–100. Used behind the scan, ID and meeting heroes.
- **terms** (Preliminary terms): a small gathering of `color-haze-gather-peach`, `color-haze-gather-lilac` and `color-haze-gather-rose` behind the estimate.
- **check** (checklist): `color-haze-sky` and `color-haze-apricot`/`color-haze-cream` blooms plus a gathering behind the card.
- **soft** (Meeting confirmed, games): `color-haze-lilac`, `color-haze-blue` and `color-haze-cream` along the top at 42%, `color-haze-blush` and `color-haze-cream` down the right, `color-haze-cool` and `color-haze-pink` along the bottom. Blur 140–150.
- **hero** (Live meeting): the soft top row plus a tight gathering behind the scene.
- **top** (Quick break): `color-haze-warm` and `color-haze-lilac` at 50% at the top only.

Recipe rule: pale tones (`color-haze-sky`, `color-haze-cream`, `color-haze-apricot`, `color-haze-blush`) at low opacity and blur 140+ for the room; saturated `color-haze-gather-*` tones at 85–90% and blur 24–100 for the gathering behind a hero.

## Figma sync

The Figma kit "Salmon Design" (152 variables, 13 text styles, 13 gradient styles) is the older source. Production (the prototype) wins where they differ. Nothing in Figma is deleted; it is updated to match.

**Changed in production**

- `color-text-muted` #876e73 → #7e666b and `color-text-soft` #b29aa0 → #a4878e, for 4.5:1 and 3:1 contrast.
- Icon stroke 1 → 1.6.
- H1 tracking -0.8% → -5%; H3 tracking -6% → -2%.
- Podium 130/68 → one 110 style, line height 0.82.
- Avatar rings (`avatar/stroke/*`) removed; holders and avatars have no strokes.
- Text on ink uses `color-text-on-inverse-muted` (#b29aa0), the old muted value, kept as its own colour.
- `gradient-reward` stops moved (51.87 / 71.43). The layered recipes hero, ambient and feature now match Figma layer for layer (see Gradients).

**Only in Figma** (keep, mark as unused): avatar initial colours plum, indigo, clay; `artwork/line-on-ink`; gradients fraynbow, pearl, cool, tile-blue, tile-warm, mist; H1 Italic.

**Only in production** (add to Figma): map colours (`color-map-route`, `color-map-me`, `color-map-halo`), `color-place-bg`, `color-artwork-sky`, `color-status-busy`, `color-camera-focus`, `color-progress-track`, `color-control-line`, the `color-haze-gather-*` tones, gradients `gradient-holder`, `gradient-points`, `gradient-eta`, `gradient-category`, `gradient-footer-glow`, the rings, sheet spacing (`space-sheet-pad-top`, `space-sheet-head`, `space-sheet-end`) and the System (iPhone look) text styles.

**Unified in code** (18 Oct): #141417 → `color-ink`, #856e75 → `color-text-muted`, #f9f8f8 → `color-base-bg`, #d9cfd2 → `color-control-line`, #e3dae0 → `color-hairline`, #efe7ec → `color-progress-track`, #b29aa0 waiting dots → `color-text-soft`. The prototype now declares foundations and semantic tokens in its `:root`, and screens read the semantic ones. 

**Names changed to match Figma** (18 Oct): `bg` → `color-base-bg`, `sec` → `color-secondary` (role `color-text-muted`), `muted` → `color-muted` (role `color-text-soft`), `hair` → `color-hairline`, `live` → `color-status-live`, `tint` → `color-secondary-on-tint`, `haze-room-*` → `color-haze-*`, `r-card` → `radius-card`, `g-select` → `gradient-peach`, my earlier `page-edge` → `space-page-margin`, `card-pad` → `space-card-pad-lg`, text styles `b`/`bm`/`c`/`cm`/`bl` → `body`/`body-medium`/`caption`/`caption-medium`/`body-large`.

**Figma values that production does not follow**: `space/card/icon-gap` 10 (production 12), `space/page/edge` is 32 in both but means the top inset; the side gutter is `space/page/margin` 24. Figma roles with no production rule yet: `space/card/line-desc`, `space/card/before-action`, `space/text/line-h1`, avatar sizes 36–88. The WF spacing and radius t-shirt sizes (`space/xs` … `space/3xl`, `radius/sm` … `radius/full`) only re-label the semantic ones, so they are not repeated here.

**Snapped to the scale** (18 Oct): about 75 off-scale values in the prototype now sit on the scale. Spacing: 3→4, 5→6, 7→8, 9→10, 11→12, 13→14, 15→16, 17→18, 21→20, 22/23→24 (key–value rows, now `space-list-row-y`), 25→24, 27→28, 30/31→32, 38/39→40. Radii: 2/6/7/9→8, 10→12, 16/18/19→20, 24→28. Type: 11→12, 12.5→12, 13→14, 18→17, 22→24, 28→24, 46→48. Every on-scale value in the prototype now reads a token (`var(--space-16)`, `var(--radius-20)`, `var(--font-size-14)`). The iPhone system look (status bar clock, push banner, lock-screen activity) keeps 13 and 15 on purpose: see the "System (iPhone look)" text styles.

**Layered gradients** (18 Oct): hero, ambient and feature are rebuilt from the Figma styles layer for layer and are one token each in code; 12 elements read them instead of their own copies. Their layer colours are tokens: a few from the palette and 31 soft `glow-*` tones kept apart in their own group, Gradient colours, since nothing but the gradients uses them. `gradient-warm` had held plate’s values and `gradient-feature` was an old two-colour gradient: both fixed.

**Linked** (18 Oct): about 300 colour, radius and gradient references in the prototype moved from short names to roles (`color-text-muted`, `color-background-interactive`, `color-border-strong`…), and font weights, line heights and tracking now read type foundations. Sheet top inset snapped 26 → 28. Still written as numbers: a few line heights in px (icon boxes, h2 37/33), 1.15 / 1.25 / 1.45, tracking −0.03em and −0.384px.

**Roles in code** (18 Oct): white split by role (card fill `color-background-white`, text on dark `color-text-on-inverse`, cut-outs `color-paper`, camera `color-camera-on`); about 250 text elements carry their text role.

**Unified** (18 Oct): titles under hero art sit `space-hero-title` (16) below it on every screen except Pinoy Henyo set-up (art overhang, kept at 24); reward cards now sit `space-grid-gap` (16) apart like action tiles. Named exceptions kept on purpose: the “i” of the info button (an icon), the “you” label on the map, the price and the podium numbers.


## Components

- Components are CSS classes, not scripts. Load `components/bundle.css` after the tokens and build screens from its classes; it reads the tokens by name.
- Each component card shows the real markup from the prototype and its guideline: Button, Footer, TopBar, Card, ListRow, KeyValue, SectionHeader, Tile, SelectionControls, Toggle, Segmented, Chip, Badge, Field, Sheet, Toast, Progress, Avatar, Photo, Slot, Dots, Digit, Spinner, Notice. Functional components: Fact (chip · tile · card) and Action (tile · feature) on surfaces.
- A screen is a TopBar, a scrolling body with 32 above the content and 24 at the sides, and a Footer; sheets bring their own footer.
- State lives in a class on the element that owns it (`on`, `busy`, `disabled`) plus the matching ARIA attribute (`aria-checked`, `aria-selected`).
- Screen-specific pieces (camera frame, QR, scratch card, podium, points toast, ticket) are not components yet; copy them from the prototype.

## Translucent colours (18 Oct)

Six roles cover every translucent colour that repeats: **color-glass** (white 92), **color-glass-soft** (white 70), **color-glass-dark** (ink 85), **color-scrim** (ink 45), **color-text-on-dark-soft** (white 70), **color-fill-on-dark** (white 16). Each is a palette colour mixed with transparency, so a palette change flows through.

There is no opacity scale. A one-off inside a component (top-bar and footer fades, map veils, camera vignette, ripples, pulses, scan lines) mixes a palette or semantic token with its own percentage right where it is used, e.g. `color-mix(in srgb, var(--color-base-bg) 90%, transparent)`. Transparent gradient ends are plain `transparent`.

Left as they are: the prototype chrome around the phone, the podium and tile SVG gradients (Figma recipes), and canvas masks.


## Type leftovers (19 Oct)

Every line height and letter spacing in the app is now on the scale. Two line heights joined the foundations: **leading-normal 1.3** (two-line pairs and labels) and **leading-relaxed 1.45** (text fields, legal note). One tracking joined: **tracking-wider 1px** (pickup code). Screen titles (h2) now use leading-solid: 36 on 36, 32 on 32 on short phones, one pixel tighter than before.

The iPhone look (status bar, push, live activity) keeps its own iOS values on purpose; they are listed under System. The prototype panel around the phone is not part of the app.
