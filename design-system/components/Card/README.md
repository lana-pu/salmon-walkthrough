White rounded surface that groups related content on the grey page.

**Use** `<div class="card">`: `color-background-white`, radius `radius-card` (20), no shadow, no border. Padding comes from what is inside: `.rows` (4 × 16), key–value lines (4 × 16), or `space-card-pad-lg` (16) for free content.

**Holds** List rows, Key–value lines, a checklist, a photo with text. Cards stack `space-page-group` (16) apart inside a section and `space-page-between` (24) between sections; a section after a card that belongs to another group starts `space-group-break` (32) below.

**Tinted cards** use a gradient token for the fill (`gradient-hero` on action tiles and product cards, `gradient-feature` for the Get ready card), never a flat tint.

Don’t: nest cards, add shadows or coloured borders.
