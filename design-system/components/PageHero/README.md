# PageHero

The opening block of every interior page: a mono breadcrumb, a huge uppercase H1 and an optional lede beside it.

**The consumer provides** the breadcrumb path (mono, `violet`, slash-separated; links hover `coral`), the page title as `h1.display-h1` (use `.display-h1--short` for one or two short words), and optionally a `p.lede` in the `.page-hero__grid` second column.

**Rules**
- The H1 is set in `display-h1`: Archivo 800, stretch 118%, uppercase, line-height .92, tracking -.03em, `text-wrap: balance`. It scales with the `.site` container (`cqi`), so the hero must sit inside `.site`.
- One word may be picked out with `.accent-coral` or `.accent-violet`; never both, never more than one phrase.
- The hero ends with a `rule` bottom border; the next section starts flush.
