# SidebarNav

The sticky left rail on long pages (grants, legal, content TOC): a mono label then links with a 2px left bar.

**The consumer provides** a mono label (`/section`) and a list of links; mark the current one `.is-current`. Rest state: `text-3` with a `rule` bar; current and hover: `coral` text and bar. Variants `.doc-toc`, `.fund-nav` and `.legal-toc` follow the same pattern (the TOC's top-level entries keep `text` with a `coral` bar).

The rail is 300px and hides below 1000px; nothing replaces it on mobile.
