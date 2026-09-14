# SITCON 2027 Slidev theme

A self-contained theme following the [SITCON 2027 website](https://sitcon.org/2027/): LINE Seed TW typography, warm paper and mist surfaces, near-black covers, acid-lime section breaks, and thin rules. Reference checked September 2026.

## Reuse

Copy this entire directory into another Slidev project:

```yaml
---
theme: ./theme
layout: cover
title: My presentation
themeConfig:
  brand: SITCON
  year: '2027'
  footer: 學生計算機年會
  showPageNumber: true
---
```

No imports from the parent deck, sibling website, or remote font services are needed. Full Traditional Chinese fonts are bundled. Vite resolves their URLs for deployment under a base path.

For package distribution, run `npm pack` inside this directory and install the resulting tarball in the consuming project. Then set `theme: sitcon-2027`. Registry publication is optional.

## Layouts

| Layout | Purpose / slots |
| --- | --- |
| `cover`, `intro`, `end` | Large title and supporting text on ink |
| `default` | Headings, prose, lists, code and tables |
| `section` | Acid-lime section divider |
| `center` | Vertically centered content |
| `statement` | Large statement on ink |
| `quote` | Markdown blockquote on mist |
| `fact` | Large number or short fact on acid |
| `two-cols` | Default/left content, `::right::` |
| `two-cols-header` | Default or `::header::`, `::left::`, `::right::`, `::bottom::` |
| `image-left`, `image-right` | Text with an image alongside |
| `image` | Image fills the content region, optional text overlay |
| `full` | No chrome, 24px padding |
| `none` | No chrome or padding |

Other Slidev layouts retain their built-in implementation.

## Per-slide options

```yaml
layout: two-cols-header
tone: mist # paper | mist | dark | acid
eyebrow: 01 / 開發組
label: Architecture
footer: false # hide footer; a string overrides its text
layoutClass: gap-12 # column grid utilities
```

All framed layouts accept `background`, `backgroundSize`, and `backgroundPosition`. Use `tone: dark` with background photography. Background photographs are dimmed for legibility.

Image layouts accept `image`, `alt`, `caption`, `backgroundSize: cover | contain`, and `backgroundPosition`. Put deck images in the consuming project's `public/` directory and reference them with a leading slash. Image URLs respect Slidev's deployment base.

```md
---
layout: image-right
image: /photos/community.webp
alt: Participants at a community event
caption: Photo credit
backgroundPosition: 60% center
---

# A title

Supporting text.
```

Column layouts retain Slidev's `class` and `layoutClass` props. Normal slide classes and styles are forwarded through the shared frame. `center` centers vertically; add `class: text-center` for horizontal alignment.

## Structure and customization

- `styles/tokens.css`: public color, font and spacing variables plus surface variants.
- `styles/typography.css`: typography, Markdown elements and text helpers.
- `styles/layouts.css`: frame spacing and layout compositions.
- `components/SitconFrame.vue`: shared shell, branding, background and page footer.
- `components/SitconColumns.vue`, `SitconImage.vue`: shared compositions.
- `layouts/`: thin, named Slidev entry points.
- `assets/fonts/`: full Traditional Chinese fonts and their license.

Override tokens in the consuming deck's `style.css`:

```css
:root {
  --sitcon-acid: #d9ff65;
  --sitcon-space-x: 48px;
  --sitcon-column-gap: 32px;
}
```

The `--sitcon-*` variables are the public styling API. CSS is scoped to `.sitcon-frame` to avoid restyling presenter controls. Use `sitcon-muted` and `sitcon-caption` for secondary text.

The theme targets 16:9 slides at Slidev's 980px canvas width. It does not automatically shrink overflowing content.

## Assets

LINE Seed TW is © LY Corporation, distributed under SIL OFL 1.1; see `assets/fonts/OFL.txt` and [LINE Seed](https://seed.line.me/index_tw.html). The bundled Regular and ExtraBold files are the full WOFF2 fonts used by the SITCON 2027 site, not page-specific subsets.

The theme uses text branding. The repository's separate demonstration photograph is not included in the theme package.
