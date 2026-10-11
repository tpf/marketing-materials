# TierCard

A sponsorship tier: mono name and number, a huge price, a lead line and a `+` list of benefits.

**Variants** set by class, cycled down the page: `.sptier--light` (`band-bg`, markers `violet-ink`) for the top tier, `.sptier--violet` (ink `bg`, markers `bg`) for the second, `.sptier--dark` (`bg`, `rule-strong` border, markers `coral`) for the rest. Each variant re-points the local `--sp-rule` and `--sp-mark` variables.

**The consumer provides** the tier name, its index (`01`…), annual price, monthly equivalent, a lead heading and sentence, and the benefit list (inline links allowed; the `+` is absolutely placed so links flow).

Prices are in `tier-price`. Preview copy is from `content/how-do-sponsors-benefit.md`.
