# Combo Submission Template

Use this template to document a **mechanical interaction** (a combo) so it can be added to
the Premodern combo database at [premodernhq.com](https://premodernhq.com).

A combo is two or more cards whose interaction produces a meaningful payoff: an infinite loop,
a one-card-kill engine, a soft lock, a draw/tutor chain, etc. If you just want to document a
single strong card or a deck, this is the wrong template.

You do **not** need to write JSON. Fill in the sections below in plain text and submit them
(see **How to Submit** at the bottom). The maintainer converts your submission into the served
combo JSON, and the pipeline fills in everything technical automatically (see
**What the pipeline adds for you**).

---

## Core Info

*   **Name:** Full card-by-card name joined with `+`, e.g. `Goblin Bombardment + Saproling Burst`
    or `Aluren + Cavern Harpy + Wirewood Savage`. List the cards in the order they fire.
*   **Primary archetype:** The deck this combo defines or most often appears in
    (e.g. `Aluren`, `Reanimator`, `Parfait`). Use the slug you see in the URL on the site if you
    know it; otherwise the plain deck name is fine.
*   **Category:** Pick exactly **one** of:
    `library-mill` | `direct-damage` | `infinite-mana` | `infinite-tokens` | `infinite-life`
    | `reanimation` | `lock` | `draw` | `tutor-chain` | `general`
*   **Difficulty / Complexity:** One of `simple` | `intermediate` | `advanced`
    (how hard it is to assemble and execute correctly under pressure).
*   **Result / Payoff:** One short line describing what you win with, e.g.
    `Infinite damage`, `Mill the opponent's library`, `Arbitrarily large life total`.
*   **Is it a true infinite loop?** `yes` / `no`.
    Only answer `yes` if the loop can repeat without limit. If it is bounded by a finite
    resource (cards in library, life total, tokens, "exile the top card" effects, etc.) answer
    `no` and describe the bound in the rulings section. *(Validation rejects "infinite" combos
    whose steps depend on the library or exiling cards.)*
*   **Color identity:** The colors of the combo's cards, e.g. `R, G` or `U`. Use `C` for
    colorless. This is just the union of the cards' colors.

## The Cards

List **every** card the combo needs, one per line, each with its role.

*   Use the **exact** card name as printed (correct spelling, apostrophes, commas). The pipeline
    matches your card names against the Premodern legal-card database to attach images, sets, and
    legality, and to detect the combo in decklists — a misspelled name will fail validation.
*   The **role** is one short clause: what this specific card does in the loop.

Format:

*   **`<Card Name>`** — `<role in the combo>`
*   **`<Card Name>`** — `<role in the combo>`

> **Legality note:** Every card must be in the Premodern card pool, and legality follows
> [premodernmagic.com](https://premodernmagic.com). You **may** submit combos that use a
> **banned** card (e.g. historical "Combo Winter" kills) — just say so in the rulings section.
> The pipeline flags banned cards automatically; it does not reject them.

## Step-by-Step Instructions

Number the steps in execution order. Keep each step to one action or response. Where the timing
is load-bearing, add the technical detail inline — call out **priority holds**, **stack order**,
**triggered vs. activated abilities**, **mana floating**, and **what must already be on the
battlefield**.

1.  (Setup / what must be in play or in hand before you start.)
2.  (First action — activate / cast / tap...)
3.  (Response or trigger — note stack order if it matters.)
4.  (The repeating part of the loop, and what each iteration nets.)
5.  (How you convert the loop into the payoff / how you end it.)

## Prerequisites

(Optional but recommended.) Bullet the board/hand state required before step 1 — e.g.
`X creatures in play`, `a sacrifice outlet`, `untapped mana of a specific color`.

## Technical Rulings

Document the rules nuances a judge or careful player needs:

*   Why the loop works (or where it stops / what bounds it).
*   Key interactions with the current Comprehensive Rules — state-based actions, the stack,
    priority, "may" vs. mandatory triggers, intervening-if clauses, etc.
*   Any banned-card status and the historical context if relevant.
*   Common mistakes or non-bo's (cards that look like they fit but don't).

## Citation (required)

Every submission **must** include at least one source link so the entry can be verified.
This becomes the combo's `provenance.sourceUrl` and is mandatory — submissions without a
citation are rejected at validation.

*   **Source URL:** (a rules ruling, a primer, an article, a forum/Discord thread, a
    tournament-winning decklist that runs it, mtg.wiki, etc.)
*   **Source type:** `official-ruling` | `primer/article` | `community` | `decklist` | `other`
*   **Your name / handle:** (optional, for credit)
*   **Confidence:** `high` | `medium` | `low` — how sure you are it works exactly as written.

---

## Worked Example (real Premodern combo)

> A complete, well-formed submission. Copy this shape for your own combo.

### Core Info
*   **Name:** Goblin Bombardment + Saproling Burst
*   **Primary archetype:** Sligh / Saproling Aggro-combo
*   **Category:** direct-damage
*   **Difficulty / Complexity:** intermediate
*   **Result / Payoff:** Burst of direct damage to the opponent's face (one big finishing turn)
*   **Is it a true infinite loop?** no — bounded by the number of fade counters / Saproling tokens
*   **Color identity:** R, G

### The Cards
*   **`Goblin Bombardment`** — free sacrifice outlet: sacrifice a creature to deal 1 damage to any target, no mana or tap required.
*   **`Saproling Burst`** — enters with several fade counters; remove a counter to make a 1/1 Saproling token. When Saproling Burst leaves play, every Saproling it made is destroyed.

### Step-by-Step Instructions
1.  Have both `Goblin Bombardment` and `Saproling Burst` on the battlefield. `Saproling Burst` should still have fade counters.
2.  Activate `Saproling Burst`, removing a fade counter to create a 1/1 Saproling token. Repeat to bank as many tokens as you want (each removal is a separate activation).
3.  Sacrifice each Saproling to `Goblin Bombardment`, dealing 1 damage to the opponent per token. (Damage goes on the stack per activation; you can fire them one at a time.)
4.  **Finisher:** when `Saproling Burst` runs out of fade counters and the last counter is removed, sacrifice it — but first respond by making the final token; *then* let it leave. Critically, sacrifice the remaining Saprolings to `Goblin Bombardment` **in response to `Saproling Burst` leaving the battlefield**, before its "destroy all Saprolings" effect resolves, so none of the damage is lost.
5.  Total damage ≈ the number of fade counters you started with (typically 6), delivered to the opponent's face.

### Prerequisites
*   `Goblin Bombardment` and `Saproling Burst` both resolved and on the battlefield.
*   At least one fade counter remaining on `Saproling Burst`.

### Technical Rulings
*   `Goblin Bombardment`'s ability requires no mana and no tap, so all tokens can be sacrificed in a single turn at instant speed.
*   When `Saproling Burst` leaves the battlefield, its delayed trigger destroys all tokens it created. Hold priority and sacrifice those tokens to `Goblin Bombardment` while that trigger is on the stack — otherwise the tokens die for no value.
*   Not a true infinite: output is capped by fade counters, so this is `isInfinite: no`.
*   Both cards are legal in Premodern.

### Citation
*   **Source URL:** https://mtg.wiki/page/Goblin_Bombardment
*   **Source type:** community
*   **Your name / handle:** (optional)
*   **Confidence:** high

---

## What the pipeline adds for you (don't fill these in)

When the maintainer ingests your submission, the build pipeline auto-generates these — you can
ignore them:

*   **`id`** — derived from the name (e.g. `goblin-bombardment-saproling-burst`).
*   **Per-card data** — `scryfallId`, `setCode`, the preferred old-border printing image, and
    `legalInPremodern` / `isBanned` flags, all resolved from the Premodern legal-card database.
*   **`comboCost` / `costPartial`** — total price of the combo's cards, computed at serve time.
*   **`containsBannedCards`** — set automatically from the card legality data.
*   **`_schemaVersion`** and aggregation/sorting into the served `combos.json`.

**How your fields map to the served combo JSON:** Name → `name`; Primary archetype →
`archetypeAssociations`; Category → `category`; Difficulty → `complexity`; Result → `result`;
Is-it-infinite → `isInfinite`; Color identity → `colorIdentity`; The Cards → `cards[]`
(`name` + `role`); Steps → `steps[]`; Prerequisites → `prerequisites[]`; Technical Rulings →
`rulingNotes`; Citation → `provenance` (`sourceUrl`, `source`/method, `confidence`,
`lastVerified`).

---

## How to Submit

Pick whichever is easiest — all routes reach the maintainer, who PRs it to the public GitHub
data mirror:

*   **Web form:** [premodernhq.com/contribute](https://premodernhq.com/contribute)
*   **GitHub:** open an Issue or Pull Request on the [Data Mirror](https://github.com/premodern-wiki/data-mirror)
*   **Discord:** DM `externality_0502`
*   **Email:** `sv_gravity_400@proton.me`

Citations are required on every submission. Card legality follows
[premodernmagic.com](https://premodernmagic.com).
