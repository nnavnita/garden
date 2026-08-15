# garden

Personal digital garden — Obsidian vault (`content/`) published as a static site via Quartz v5. Fork of [jackyzha0/quartz](https://github.com/jackyzha0/quartz): `origin` = `nnavnita/garden`, `upstream` = `jackyzha0/quartz`.

The vault content itself is personal notes — treat `content/` as private unless told otherwise (e.g. don't summarize its contents into shared artifacts).

## Stack

- TypeScript, Node ≥22, npm ≥10.9.2
- Quartz v5 (static site generator, plugin-based: `@quartz-community/*`)
- Deployed as GitHub Pages

## Setup

```sh
git clone https://github.com/nnavnita/garden
cd garden
npm ci
```

## Common commands

```sh
npx quartz build --serve -d docs   # `npm run docs` — local dev server
npm run check                       # tsc --noEmit + prettier --check
npm run format                      # prettier --write
npm test                            # tsx --test
```

Notes are edited in Obsidian directly against `content/`; the vault's `.obsidian/` config is committed.

## Deploy

`.github/workflows/deploy.yml` — push to `main` → `npx quartz build` → GitHub Pages. This is the only workflow that actually runs on this fork: `ci.yaml`, `build-preview.yaml`, `deploy-preview.yaml`, `deploy-v5.yaml`, and `docker-build-push.yaml` are all upstream-only (gated on `github.repository == 'jackyzha0/quartz'`) and stay inert here — don't debug them as if they run on pushes to this repo.

## Roadmap

`bullseye.yaml` — managed by the bullseye MCP server. Use `bullseye_frontier` (cwd = this repo) for what's next. Infra is done; the open-ended work here is content, not code.
