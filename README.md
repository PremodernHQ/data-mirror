# PremodernHQ — Community Data Mirror

This is the **public, community-facing data repository** for [premodernhq.com](https://www.premodernhq.com).
It's where the Premodern community submits the data that powers the site: tournament results,
decklists, archetype primers, combos, glossary terms, and community creators.

You do **not** need to be a programmer to contribute. Each data type below has a plain-language
**template** — copy it, fill it in, and submit it any way that's easy for you. A maintainer
reviews every submission and merges it; from there the pipeline normalizes it and it appears on
the site.

## What you can submit

| I want to submit… | Use this template | What it's for |
|---|---|---|
| **Tournament results / standings** | [`event-template.md`](./event-template.md) | Top-8/full standings from store championships, online leagues, etc. |
| **A decklist** | [`decklist-template.md`](./decklist-template.md) | A tournament 75 or a spicy brew — paste a link or a raw list. |
| **An archetype primer** | [`archetype-template.md`](./archetype-template.md) | Game plan, key cards, matchups, sideboard guide, deck history. |
| **A combo** | [`combo-template.md`](./combo-template.md) | A documented mechanical interaction, step-by-step, with rulings. |
| **A glossary term** | [`glossary-template.json`](./glossary-template.json) | A plain-language definition of a Premodern/MTG term. |
| **A community creator** | [`community-creators-template.md`](./community-creators-template.md) | A Premodern blog, podcast, YouTube channel, or Discord. |

## How to submit (pick whichever is easiest)

1. **Web form (no GitHub needed)** — [premodernhq.com/contribute](https://www.premodernhq.com/contribute)
2. **GitHub** — open an Issue or a Pull Request on this repository with the filled-in template.
3. **Discord** — DM **`externality_0502`** with your links + details.
4. **Email** — **sv_gravity_400@proton.me**

## Ground rules (please read)

- **Cite a verifiable source.** Every submission needs a link to where the data can be
  verified — a tournament report, a decklist host (Moxfield / MTGGoldfish / MTGTop8 / TCDecks /
  Scryfall), an official results page, etc. Submissions without a citation can't be published.
- **Legality follows [premodernmagic.com](https://premodernmagic.com).** We don't make
  independent format/ban decisions — we defer to the official Premodern format and ban list.
  (Decks are checked against the ban list *as of the date they were played*, so an older deck
  isn't flagged for a card banned later.)
- **You only fill the human-readable fields.** The templates note which fields the site
  generates automatically (card images, archetype stats, IDs, prices, …) — you never need to
  write those, and you never need to touch JSON unless you want to.

## For maintainers

- Submissions are reviewed, then merged. The site ingests the canonical data trees
  (`events`, `decklists`, `archetypes`, `combos`, plus `cards`/`prices`) via the
  PremodernHQ pipeline; see that repo's `docs/DATA_PIPELINE.md`.
- Each template documents how its fields map to the served data shape.
