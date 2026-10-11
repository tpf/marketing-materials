# Megamenu

A single dropdown panel under the header that shows only the section whose nav item opened it.

**The consumer provides** one `.megamenu__col` per section (id `megamenu-<section>`), each with a mono `.megamenu__label` (`/about`, in `violet`) and a `.megamenu__links` grid; add `--2` for two columns. A nested group gets `.megamenu__label--sub` with a path label (`/about/charters`).

**Rules**
- Panel: `bg-raised`, 1px `rule` border with no top edge, `shadow-menu`. It is the only menu with a shadow.
- JS adds `.is-open` to the header and `.is-shown` to one column; the column's left offset is set under its button. Escape and outside clicks close it and return focus to the nav item.
- Links are `text`, 14.5px, no underline; hover turns them `coral`.
