# LinkChips

Mono chips that a plain Markdown list of links becomes inside `.doc`, no classes needed.

**The consumer provides** a Markdown bullet list where each item is only a link. The `.doc ul:has(> li > a:only-child)` rule lays it out as a wrapping row of chips: min-height `space-touch`, 1px `rule-strong` border, mono 14px `text`, hover `coral`.

**Note** `rule-strong` is 1.6:1 on `bg`, so the chip's label, not its border, carries the affordance. Keep labels short (one to three words).
