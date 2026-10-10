# Header

The site masthead: onion-and-wordmark brand cell, mono `/section` nav items, a search trigger and a solid coral Donate block, separated by vertical `rule` hairlines.

**Use** once per page, first in `.site`. Markup: `header.site-header > .site-header__bar > a.site-header__brand + nav.site-header__nav`.

**The consumer provides**
- The brand link with the onion logo (`assets/Logos/Perl_Onion_Color.svg`, 38px, sitting on a `band-bg` disc via `radius-disc`) and the two-line wordmark "The Perl & Raku / Foundation".
- One `a.site-header__navitem` per top-level section, labelled with a leading slash in mono (`/about`, `/sponsors`, `/grants`, `/legal`). Add `.is-active` to the current section: it turns `coral` with a 3px inset underline (`stroke-accent`).
- `button.site-header__search` with the magnifier icon, and `a.site-header__donate` last.

**Rules**
- Nav items are real links that work without JavaScript; `dropdown.js`/`tprf.js` enhance them into disclosure buttons that open the Megamenu.
- Below 1200px the bar is replaced by `.site-header__mbar` (34px logo, Search, a compact Donate and a mono "Menu" toggle with a `rule-strong` border, all at `space-touch`). Below 375px the wordmark hides; the logo's alt text still names the link.
- Donate is always the last, rightmost element and always coral.
