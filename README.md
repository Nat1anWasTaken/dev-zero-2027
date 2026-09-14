# SITCON 2027 開發組零籌

To start the presentation:

- `pnpm install`
- `pnpm dev`
- visit <http://localhost:3030>

Edit the [slides.md](./slides.md) to see the changes.

Learn more about Slidev at the [documentation](https://sli.dev/).

## Reusable theme

The standalone [theme](./theme/README.md) contains all styles, layout overrides, shared components and fonts. Copy it into another Slidev project and set `theme: ./theme`, or install a tarball created with `npm pack` inside `theme/`.

- `pnpm dev:theme`: preview the [layout gallery](./theme-demo.md).
- `pnpm build`: build the meeting deck.
- `pnpm build:theme`: build the gallery to `dist/theme`.

The gallery demonstrates all 16 layouts, named column slots, image fit options, code and Traditional Chinese typography. The visual reference is the [SITCON 2027 website](https://sitcon.org/2027/). See [demo asset attribution](./public/theme-demo/SOURCES.md).
