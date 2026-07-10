# Space Intelligence: Portal Space Systems and the Solar-Thermal Propulsion Thesis

An interactive explainer for [Space Intelligence: Portal Space Systems and the Solar-Thermal Propulsion Thesis](https://github.com/dpetkevich/explainer/blob/main/fixtures/portal-stp.md), built with
[explain-it](https://github.com/dpetkevich/explainer). Every concept is taught through an
interactive animation with real physics — and every caption, scene, and check in it
is open to improvement by you.

**Read it live → https://idea-explainer.github.io/portal-stp/**

## How this works

- **⭐ Star this repo** if the explanation taught you something — stars rank explanations
  on the [homepage](https://explain-it-hub.vercel.app).
- **Endorsements** (`endorsements.json`) are from qualified people in the field, added
  only through maintainer-approved pull requests. They appear at the top of the explainer.
- **Improve it**: fork, edit, open a PR — see [CONTRIBUTING.md](CONTRIBUTING.md).
  Maintainers review and merge; CI rebuilds and republishes automatically.

## What's in this repo

| File | What it is |
|---|---|
| `storyboard.md` | **The thing you edit**: audience, script, and every instruction that generates the graphics — one document |
| `paper.json` | Paper metadata (title, authors, source) |
| `endorsements.json` | Field-expert endorsements (maintainer-gated) |


The interactive scene graphics are **not in the tree** — they live in a release asset
bundle pinned by `.github/scenes.lock.json`; CI fetches, verifies, and assembles them.
Everything under `.github/` is infrastructure — the four files above are the whole
editable surface.
