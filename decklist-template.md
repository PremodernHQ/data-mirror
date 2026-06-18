# Decklist Submission Template

Thanks for helping build the Premodern community archive! This guide walks you
through submitting a decklist, whether you have a Moxfield/MTGGoldfish link or
just a typed-out list. **You do not need to be technical** — if you can paste a
link and fill in a few blanks, you can contribute.

Every decklist we publish is tied to a **player**, an **archetype**, an **event**
(or other context), and a **verifiable citation**. The two things we cannot
publish without are the **decklist itself** and a **source we can check**.

> **TL;DR — the EASY way:** paste a Moxfield / MTGGoldfish / Scryfall link, tell
> us the **pilot**, the **archetype**, the **event/date**, and a **citation**.
> That's it. The rest is optional.

---

## Two ways to submit a list

Pick whichever is easier for you. Both are equally welcome.

### Path A — The EASY path (deck link)

If the deck already lives online, just give us the link. We'll pull the cards
from it. Fill in:

*   **Deck Link:** (a public **Moxfield**, **MTGGoldfish**, or **Scryfall** URL)
*   **Pilot Name:** (who played/built it, e.g. `Martin Ryan`)
*   **Archetype:** (a category — `Aggro` / `Control` / `Combo` / `Midrange` /
    `Spicy Brew` — **or** a specific archetype slug like `rg-oath`,
    `the-rock`, `goblins`. If unsure, just name the deck and we'll slug it.)
*   **Event / Context:** (event name + date, e.g.
    `Premodern Monthly — 2025-01-11`. If it wasn't from an event, say so:
    `League`, `Casual`, `Brew`, etc.)
*   **Source / Citation:** (a link we can verify — see
    [Citations](#citations--legality) below)

That's the whole easy path. Everything else (placement, record, colors) is a
bonus.

### Path B — The RAW-LIST path (typed cards)

No link? Type the list. Use this **exact text format** so we can ingest it
cleanly:

*   One card per line.
*   Each line is: **quantity**, a space, then the **full card name**.
*   List the **mainboard** first, then a line that says **`Sideboard`** on its
    own, then the sideboard cards.
*   **60+ cards** in the mainboard, **15 or fewer** in the sideboard.
*   Use the **full canonical card name** (e.g. `Oath of Druids`, not "Oath").
*   For split cards, use the canonical `Name // Name` form, e.g. `Fire // Ice`.
*   Max **4 copies** of any card across main + side (except basic lands).

Raw-list skeleton:

```
4 Karplusan Forest
4 Wasteland
...
4 Oath of Druids
4 Terravore

Sideboard
3 Call of the Herd
2 Naturalize
2 Pyroblast
```

Then add the same metadata as Path A (Pilot, Archetype, Event/Context, Source).

---

## Required vs. optional fields

### Required (we can't publish without these)

*   **The decklist** — either a deck **link** (Path A) **or** a **raw list**
    (Path B).
*   **Pilot Name** — who played or built the deck.
*   **Archetype** — a category or a specific archetype slug.
*   **Source / Citation** — a link or reference we can verify.

### Optional (nice to have — improves the page)

*   **Event Name & Date** — strongly encouraged; ties the deck to a result.
*   **Placement / Rank** — e.g. `5th`, `Top 8`, `1st`.
*   **Record** — wins / losses, e.g. `5-2`.
*   **Colors** — we can usually infer these from the list.
*   **Notes** — tech choices, sideboard plan, anything fun about the deck.

You don't have to know the internal field names — the maintainer maps your
submission to the data format (which stores things like `playerName`,
`archetypeId`, `mainboard[]`, `sideboard[]`, and the source URL). Just give us
the human-readable info above.

---

## Examples (filled in)

### Example A — Deck-link submission

```
Deck Name:   RG Oath
Pilot Name:  Martin Ryan
Archetype:   rg-oath        (category: Midrange)
Event:       Premodern Monthly — 2025-01-11
Placement:   5th
Deck Link:   https://www.moxfield.com/decks/xxxxxxxxxxxxxxxxxxxxxx
Source:      https://mtgtop8.com/event?e=63533&d=680153&f=PREM
```

### Example B — Raw-list submission (shortened for illustration)

```
Deck Name:   RG Oath
Pilot Name:  Martin Ryan
Archetype:   rg-oath        (category: Midrange)
Event:       Premodern Monthly — 2025-01-11
Placement:   5th
Source:      https://mtgtop8.com/event?e=63533&d=680153&f=PREM

Decklist:
4 Karplusan Forest
4 Mishra's Factory
4 Rishadan Port
3 Snow-Covered Forest
1 Snow-Covered Mountain
4 Treetop Village
4 Wasteland
4 Wooded Foothills
4 Mox Diamond
4 Terravore
2 Naturalize
2 Pyroclasm
4 Thermokarst
4 Winter's Grasp
4 Oath of Druids
4 Sphere of Resistance
4 Sylvan Library

Sideboard
3 Call of the Herd
2 Naturalize
2 Phyrexian Furnace
2 Pyroblast
2 Pyroclasm
1 Red Elemental Blast
1 Tormod's Crypt
2 Zuran Orb
```

(The mainboard above is 60 cards, the sideboard is 15 — the standard
Premodern configuration.)

---

## Citations & legality

**Every submission needs a verifiable citation.** This is what lets us (and
future researchers) trust the data. Good sources include:

*   A tournament result page (MTGTop8, MTGDecks, TCDecks, etc.)
*   An official event report or stream VOD
*   A linked Moxfield / MTGGoldfish deck that shows provenance
*   A direct organizer/judge confirmation (note who and when)

If the deck is your own brew with no event, the citation can be your own
Moxfield link plus a short note — just be honest about the context.

**Legality:** Premodern legality follows the official banned/restricted list at
**[premodernmagic.com](https://premodernmagic.com)**. Our ingestion pipeline
checks each list against the legal-card set and the ban list (using each card's
effective ban date, so decks played *before* a card was banned are not flagged).
You don't need to verify legality yourself — but lists that are obviously not
Premodern-legal (wrong-era cards) may be held for review. A card that was legal
on the date it was played is fine even if it was banned later.

---

## How to submit

Use whichever channel is easiest:

*   **Web form:** [premodernhq.com/contribute](https://premodernhq.com/contribute)
    — the simplest option; the form asks for exactly the fields above.
*   **GitHub Issue or Pull Request:** open one against the
    [Data Mirror](https://github.com/premodern-wiki/data-mirror) repo. Copy this
    template into your issue/PR and fill it in.
*   **Discord DM:** message **externality_0502**.
*   **Email:** **sv_gravity_400@proton.me**.

Whatever the channel, please remember the four required pieces: **the list**,
**the pilot**, **the archetype**, and **a citation**.

---
*Submit via Pull Request or Issue in the [Data Mirror](https://github.com/premodern-wiki/data-mirror)*
