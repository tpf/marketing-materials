The 2026 identity for The Perl & Raku Foundation: a dark, ruled, poster-weight system. Huge uppercase Archivo headlines, mono labels that read like paths, and two hot accents (coral for action, violet for structure) on a near-black ground. It looks like a well-typeset terminal that went to art school.

## Content fundamentals

- **Name the organisation in full** the first time: "The Perl & Raku Foundation", with the ampersand. After that, "TPRF". The legal entity is "Yet Another Society (DBA) The Perl And Raku Foundation" and appears only in the footer and payment details.
- **Write plainly and concretely.** Say what money does: "Grants pay for core maintenance, security fixes and new tooling", not "empowering the ecosystem". Address readers as "you"; the foundation is "we".
- **Headings are short and declarative** and are set uppercase by the style, so write them in sentence case in Markdown ("Our sponsors", "How your donation helps").
- **Labels are paths.** Kickers, breadcrumbs, menu labels and section labels are lowercase mono paths with a leading slash: `/about`, `/grants/perl-fund`, `/about/charters`. Never write "ABOUT US" as a label.
- **Numbers are mono and zero-padded** when they enumerate: `01`, `02`, `03`.
- **Arrows are glyphs, not icons**: `↗` for off-site links and row lists, `→` for in-site buttons, `+` and `—` as list markers, `+`/`−` for disclosures.
- **No emoji.** Page copy lives in Markdown under `/content`; templates style it and never hard-code it.

## Visual foundations

### Colour

- The page ground is `bg`. Panels that float (megamenu, search) use `bg-raised`; anything recessed (callouts, quotes, code, hovers) uses `bg-inset`.
- Separate with hairlines, never shadows or rounded cards: `rule` for every divider, `rule-strong` for chip and card borders. Build grids of cards as a 1px gap over a `rule` background so the hairlines are the gaps.
- Text runs from `text` (headings, primary) through `text-2` (body), `text-3` (secondary) to `text-4` (footer, meta). All four pass AA on all three dark grounds.
- **`coral` means action**: Donate, primary buttons, link hover, the active nav underline, inline links in prose, the focus ring. On a coral fill, set text in `bg`.
- **`violet` means structure**: kickers, breadcrumbs, list numbers, the 3px bar on callouts and quotes, row arrows. On a violet fill, set text in `bg`. Never put coral on violet or violet on coral (1.0:1).
- **Light bands** (`band-bg` with `band-text`) break up long pages: sponsors, the grant Application, "How your donation helps", the top sponsorship tier. Inside them, links and numbers switch to `violet-ink`, and hairlines to `band-rule`.
- Logos designed for white grounds sit on a `logo-tile`.
- `coral`, `violet` and `violet-ink` are defined in `oklch()`. If a target can't render `oklch()`, use the sRGB fallbacks noted on each token.

### Type

- **Archivo** (variable: width 62–125, weight 400–900) for everything that isn't a label. Display and headings are weight 800, `font-stretch` 112–118%, uppercase, with tight leading (.88–1.05) and negative tracking. The stretch is the signature; don't drop it.
- **IBM Plex Mono** (400/500/600) for labels, kickers, nav items, numbers, dates, meta rows, legal notices and code.
- Both load from Google Fonts: `Archivo:wdth,wght@62..125,400..900` and `IBM Plex Mono:wght@400;500;600`.
- Display sizes are fluid, scaling with the `.site` container (`cqi` units), so the `.site` wrapper (`container-type: inline-size`) is required. The fixed sizes in the type scale are each style's maximum; usage notes give the `clamp()`.
- Body copy is `body` (16.5px/1.65) in `text-2`, with a measure of 860–900px. Use `text-wrap: balance` on display headings and `pretty` on paragraphs.

### Space and layout

- Full-width sections are padded `section-pad` vertically and `gutter` horizontally, and are separated by `rule` borders, not margins.
- Grids are `auto-fit` with `minmax(min(100%, Npx), 1fr)`, so they collapse to one column without media queries. Typical minimums are 300–460px.
- Long pages get a 300px sticky left rail (SidebarNav) that hides below 1000px.
- Every interactive target is at least `space-touch` (44px) tall.

### Shape, depth and motion

- Everything is square (`radius-none`). The only curves are the `radius-disc` behind the header logo and the Pagefind search UI (`radius-search`).
- Accent bars do the work shadows would: a 3px `violet` left bar (`stroke-accent`) on callouts, quotes and code; a 3px inset `coral` underline for the active nav item; a 4px inset underline on Gold and Silver sponsor tiles.
- Only two shadows exist: `shadow-menu` on the megamenu and `shadow-dialog` on the search overlay.
- Hover is a colour change to `coral` (or `bg-inset` behind header items); links lose their underline on hover. There is no motion beyond the megamenu's visibility toggle.
- Focus is a 2px solid `coral` outline at 2px offset on every focusable element (on the coral skip link, it switches to `bg`).

### Imagery

- People photos are greyscale (`grayscale(1) contrast(1.05)`) and cropped with `object-fit: cover`. Event photos run full-bleed with a mono caption pinned bottom-left on `bg`.
- The Open Graph image in the repository still uses the previous navy-and-serif identity and is not part of this system.

## Iconography

- The mark is the **Perl onion** (`Logos/Perl_Onion_Color.svg`: a white onion on a navy `#212178` disc). In the header it sits at 34–38px on a `band-bg` disc. Use the PNG only where SVG isn't accepted (structured-data logo, social cards). Never recolour or redraw it.
- The only UI icon is a 24px stroked magnifier (2px stroke, round caps, `currentColor`) on the search trigger. Everything else is a typographic glyph (see Content fundamentals). Don't add an icon library.

## Accessibility notes

- `rule-strong` borders are 1.6:1 on `bg`. Chips and toggles that use them are always labelled, so the border is never the only cue; keep it that way.
- `text-year-past` is 3.5:1 and is only for numerals at 40px and up.
- Provide a skip link (coral pill, top-left on focus), keyboard-reachable menus that close on Escape and return focus, and `prefers-reduced-motion` handling if motion is ever added.

## Not synced

Built from `tpf/perlfoundation.org` at `redesign@9089894` (`static/css/custom.css`, `layouts/`, `content/`). The site is Hugo with plain CSS and has no component library, so the components here are static renditions of the site's own markup styled by its own stylesheet (`components/bundle.css`). The original Claude Design project wasn't read; where it and the repository differ, the repository wins. Six colours (`text-lede`, `text-year-past`, `rule-quiet`, `band-field`, `band-text-2`, `band-text-3`) and `logo-tile` are hard-coded in `custom.css` rather than in its `:root`, and are tokens here so the site can adopt them. Font files aren't stored: both faces are served by Google Fonts. Page-specific blocks not carried over as components: home photo-and-funding split, legal index, legal clause numbering, committees lists, Get Involved tiles, the grant Application field grid and the search overlay. Their styles are still in `bundle.css`.
