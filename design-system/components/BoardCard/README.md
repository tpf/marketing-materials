# BoardCard

A person card for the board page: a 4:3 greyscale headshot with a mono role tag, an uppercase name, a short bio, a "More" disclosure and a mono meta footer.

**The consumer provides** (from the `members:` YAML list in front matter) a headshot in `static/images/headshots/`, role, name, bio paragraphs, optional extended bio, seat and email.

**Rules**
- Photos are `filter: grayscale(1) contrast(1.05)` and `object-fit: cover`; the placeholder ground is `bg-inset`.
- The role tag is `violet`; the president's is `coral` (`.is-president` on the photo).
- The "More" toggle is a `<details>` summary in mono `coral` with a `+`/`−` prefix and a restored focus ring.
- Cards sit in `.board-grid`, the 1px hairline grid.

The preview uses a placeholder name and no photo; real members come from `content/the-board.md`.
