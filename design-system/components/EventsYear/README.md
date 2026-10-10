# EventsYear

A year row on the Events page: a giant year numeral at left, then ruled date/title/location rows.

**The consumer provides** one `## year` per year in `content/events.md`, each with a definition list (date as `dt`, title and location in `dd`; the template splits them).

**Rules** the current year gets `.events-year--now`: its numeral turns `coral` and its dates `violet`. Past years use `text-year-past` for the numeral (40px+ only: 3.5:1) and `text-4` dates. Titles are uppercase with a mono `violet` `↗`. Below 640px dates stack above titles. Preview entries are from `content/events.md`.
