# Prose

The typography for rendered Markdown: `.doc` (content pages), `.prose` (default single pages) and `.legal-doc` (licences and bylaws).

**The consumer provides** Markdown only. Page copy lives in `/content`; templates never hard-code it.

**Rules in `.doc`**
- H2: Archivo 800 uppercase, stretch 112%. The paragraph right after the first H2 is a lede (`lede-doc`, `text-lede`).
- H3 is a mono `violet` label (`/how-grants-work` style), not a smaller headline.
- Body `body` in `text-2`; links `coral`, underlined, offset 3px, underline removed on hover.
- Blockquote and `pre`: `bg-inset` with a 3px `violet` bar. Inline `code`: mono on `bg-inset`.
- A trailing paragraph gets a `rule` top border as a "see also" footer.
- Bold-led lists become DefinitionRows; link-only lists become LinkChips.
