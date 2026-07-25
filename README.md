# tomiadewusi.com

This is my personal knowledge repository — a long-lived public technical notebook. Markdown is the canonical representation of what I know; this repository is the source of truth, and [tomiadewusi.com](https://tomiadewusi.com) (built with [Quartz](https://quartz.jzhao.xyz/)) is a compiled view of it.

## Structure

Content lives under `content/`, organized into a small, consistent taxonomy:

| Folder | Purpose |
| --- | --- |
| `concepts/` | Single, coherent ideas — one note per identifiable question |
| `notes/` | Looser working notes that haven't crystallized into concepts yet |
| `projects/` | Project-specific notes and logs (e.g. MonteJax) |
| `decisions/` | Design decisions — context, alternatives considered, consequences |
| `experiments/` | Observations from experiments, kept separate from conclusions |
| `reading/` | Reading notes — an author's claims kept separate from my interpretation |
| `essays/` | Polished, stable-maturity arguments |
| `logs/` | Dated, chronological entries |
| `maps/` | Curated indexes tying related notes together |

Every note carries frontmatter (`title`, `description`, `type`, `topics`, `projects`, `created`, `updated`, `aliases`, `references`, `maturity`) so both humans and AI agents can interpret it consistently. See [`content/maps/maturity.md`](content/maps/maturity.md) for the maturity stages (`seed` → `developing` → `stable` → `deprecated`) — nothing is deleted just because my thinking evolved.

Notes are heavily interlinked with wiki-style links (authored edges), on top of which Graphify is used to surface inferred relationships.

## Local development

```bash
npm ci
npx quartz build --serve
```

Deploys to GitHub Pages automatically on push to `main` (see `.github/workflows/deploy-pages.yml`).
