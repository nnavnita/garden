# garden

Personal digital garden. Obsidian vault (`content/`) published as static site via [Quartz v5](https://github.com/jackyzha0/quartz).

## Setup

```sh
git clone https://github.com/nnavnita/garden
cd garden
npm ci
```

## Commands

```sh
npx quartz build --serve           # local dev server
npm run check                       # tsc --noEmit + prettier --check
npm run format                      # prettier --write
npm test                            # tsx --test
```

## Deploy

Push to `main` → GitHub Actions (`deploy.yml`) builds and publishes to GitHub Pages.
