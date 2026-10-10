# Button

Square, uppercase, heavy-stretched call-to-action links in two styles, plus the larger Donate CTA.

**Variants**
- `.btn.btn--coral`: primary. `coral` fill, `bg` ink (6.6:1), 800 weight, stretch 112%, 15px, min-height `space-btn`.
- `.btn.btn--outline`: secondary. 1px `text` border and label, 700 weight; hover turns border and label `coral`.
- `.donate-cta`: the Donate page CTA. 17px, min-height `space-cta`, with a trailing glyph (`↗` for off-site) at weight 500.

**The consumer provides** an `<a>` with a short imperative label in sentence case; the style uppercases it. Use one coral button per view; pair it with an outline button for the second option.

**Don't** round the corners, add icons other than the arrow glyphs, or put a coral button on a coral or violet band (use outline in `bg` there).
