# SITCON 2027 開發組零籌

## About this deck

This Slidev deck supports SITCON 2027 開發組的第一次籌備會議。它用來讓新成員認識彼此與開發組的協作方式，介紹日常使用的 GitLab、GitHub 等工具，並說明 CFP、CFS、年會主網站與大地遊戲等年度專案的時程和分工。

To start the presentation:

- `pnpm install`
- `pnpm dev`
- visit <http://localhost:3030>

Edit the [slides.md](./slides.md) to see the changes.

Learn more about Slidev at the [documentation](https://sli.dev/).

## Deployment

Pushing to `main` automatically builds and deploys the deck to GitHub Pages. Before the first deployment, set **Settings → Pages → Build and deployment → Source** to **GitHub Actions** in the GitHub repository.

## Reusable theme

The standalone [theme](./theme/README.md) contains all styles, layout overrides, shared components and fonts. Copy it into another Slidev project and set `theme: ./theme`, or install a tarball created with `npm pack` inside `theme/`.

- `pnpm dev:theme`: preview the [layout gallery](./theme-demo.md).
- `pnpm build`: build the meeting deck.
- `pnpm build:theme`: build the gallery to `dist/theme`.

The gallery demonstrates all 16 layouts, named column slots, image fit options, code and Traditional Chinese typography. The visual reference is the [SITCON 2027 website](https://sitcon.org/2027/). See [demo asset attribution](./public/theme-demo/SOURCES.md).
