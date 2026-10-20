Round picture in a fixed size: a portrait or an illustration from the Avatars library.

**Use** `<span class="avatar avatar--md"><img src="…"></span>`. The size and the picture are independent: the size comes from a `size-avatar-*` token through the variant class, the picture is whatever the screen passes in (Mark’s portrait, or a player illustration from the Avatars library). Radius `radius-pill`, white behind, image covers.

**Sizes.** `avatar--sm` 36 (`size-avatar-sm`), `avatar--md` 44 (`size-avatar-md`), `avatar--lg` 72 (`size-avatar-lg`), `avatar--xl` 84 (`size-avatar-xl`), `avatar--xl-compact` 70 when four players share the strip. Inside the podium rings: `avatar--podium-lead` 70 and `avatar--podium` 56, ring `stroke-podium-ring` in the place colour.

**Ring.** Add `ring` for a white `size-avatar-ring` ring when the avatar sits on a picture or next to another avatar.

**Empty and add slots** are the Slot component; give the slot the same `avatar--*` class as the avatars beside it.
