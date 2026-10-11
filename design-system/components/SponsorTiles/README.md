# SponsorTiles

White `logo-tile` boxes that let full-colour sponsor logos sit on the dark page, sized by tier.

**The consumer provides** entries in `data/sponsors.yaml` (name, url, image, level), rendered by the `sponsors-by-level` shortcode into `.sponsor-grid > .sponsor-logo.<level>`.

**Rules**
- Gold: 160px tile, 80px logo, 4px `coral` inset underline (`stroke-tier`). Silver: 60px logo, `violet` underline. Bronze: 110px tile, 44px logo, no underline.
- In the light home band the tiles drop their white box and logos render bare at 52/32/26px.
- In-kind sponsors use the `.in-kind-grid` hairline grid with a small logo, an uppercase name and a description in `text-3`.

The preview uses the onion as a stand-in logo.
