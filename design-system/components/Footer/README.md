Fixed bottom area that holds a screen’s actions and fades the content under it.

**Use** `<div class="ft">` as the last child of the screen with one or two Buttons and an optional note `<p class="ftn">` above them.

**Anatomy.** Padding `space-footer-fade` (28) on top, `space-footer-x` (24) at the sides, `space-footer-bottom` (32) below; gap `space-footer-gap` (16). The top 28 is a fade from transparent to white (`color-fade-footer` at half way, solid at the end). Behind the buttons sits the footer glow: `peach-250` at 60% and `lilac-400` radial blobs.

**Variants.** One action; one action + note (`ftn`, `text-caption`, `color-text-muted`, centred); main + second action (`btn ink` then `btn paper` or `btn plain`: the second is 40 tall, sits 8 below, and the footer ends 8 higher). `ft sheet-ft` sits on white inside sheets; `ft custom` is a bare fade (60%) for screens that draw their own footer.

**Content** scrolls under the footer: give the scroll body enough bottom padding (210 default, 140 for short screens) so the last item clears the buttons.

Don’t: put more than two buttons or anything but a note in it.
