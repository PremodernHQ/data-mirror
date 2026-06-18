# Archetype Primer Submission Template

Thanks for helping build out PremodernHQ! This guide is for submitting an
**Archetype Primer** — the editorial write-up that appears on an archetype page
(game plan, weaknesses, sideboard tips, matchup notes). You do **not** need to
submit decklists or stats: the site generates those automatically from
tournament data. You write the words; the pipeline fills in the numbers.

You don't need to know any code or JSON. Just copy the **Submission Form** below,
fill in what you can, and send it however is easiest for you (see
**How to Submit** at the bottom). The maintainer turns your answers into the
right file before it goes live.

---

## Before you start: two quick rules

1. **One archetype per submission.** Use the existing archetype name if there is
   already a page for it (e.g. you're improving the Replenish primer). Propose a
   new name only if the deck genuinely isn't covered yet.
2. **Cite your sources.** Every primer needs at least one verifiable link or
   reference (a tournament-winning list, a written primer, a video, a Discord
   thread). Submissions with no citation can't be published — we can't verify
   claims we can't trace. Legality questions follow the official banned/restricted
   list at **premodernmagic.com**.

---

## What you write vs. what the site generates

Only fill in the editorial fields. The pipeline **owns** everything else and will
overwrite it on every data refresh, so there's no point sending it:

| You write (editorial) | The site generates automatically (don't send) |
|---|---|
| Name, category, 2-3 sentence description | Card inclusion %, average counts, trends |
| Tier (your opinion / community read) | Win rates and match counts |
| Game plan | Decklists pulled from MTGO + events |
| Key cards (names + which is the icon) | Scryfall card IDs and images |
| Weaknesses / how to beat it | Meta share and sample sizes |
| How to win (piloting tips) | Color identity (derived from lists) |
| Sideboard philosophy / guide | Sub-category and signature cards |
| Notable matchups | |

> You list key cards **by name** and flag the icon. You do **not** look up any
> card IDs — the pipeline matches names to the card database for you.

---

## Submission Form

Copy everything between the lines and fill it in. Leave a field blank if you're
not sure — a partial primer is still useful and the maintainer can follow up.

```
=== ARCHETYPE PRIMER SUBMISSION ===

--- Core Info ---
Archetype name:        (e.g. Replenish)
New or existing page?:  (new | improving existing)
Category:               (aggro | control | combo | midrange | prison | tempo)
Tier (optional):        (top | strong | viable | rogue | pending) + one line on why
Colors:                 (e.g. W, U) — just so we can sanity-check; the site derives the real value

Description (2-3 sentences, the "elevator pitch" / vibe of the deck):


--- Key Cards (4-8) ---
List the cards that define the deck. Mark ONE as the icon (the card used for the
page artwork — usually the most iconic / recognizable payoff).
1. (card name)  [ICON]
2. (card name)
3. (card name)
4. (card name)
5.
6.
7.
8.

--- Strategy ---
Game plan (how the deck actually wins — a paragraph or two is great):


How to win / piloting tips (optional, bullet points — sequencing, mulligans,
key lines):
-
-

Weaknesses / how to beat it (at least 2 specific things that punish the deck):
-
-

Sideboard philosophy (1-3 sentences: what you bring in, common plans):


Notable matchups (optional — "favored / even / unfavored" + a sentence each):
- vs (archetype): (favored | even | unfavored) — why
- vs (archetype): (favored | even | unfavored) — why

--- Citations & Resources (REQUIRED: at least one) ---
Primary source URL:     (decklist, primer, or article that backs this up)
Author / pilot credit:  (who wrote the primer or piloted the list, if known)
Additional resources:   (videos, podcasts, extra primers — one per line)
Discord handle (optional, so we can credit/contact you):

=== END SUBMISSION ===
```

---

## Filled-in EXAMPLE — Replenish

This is a complete, well-formed submission you can model yours on.

```
=== ARCHETYPE PRIMER SUBMISSION ===

--- Core Info ---
Archetype name:        Replenish
New or existing page?:  improving existing
Category:               combo
Tier (optional):        strong — one of the format's defining combo decks; resilient and fast
Colors:                 W, U

Description:
Replenish is an enchantment-based combo deck that loads the graveyard with
powerful enchantments — Parallax Wave, Opalescence, and Parallax Tide — then casts
Replenish to return them all to the battlefield at once. With Opalescence in play
the returned Parallax effects animate and snowball into a lethal board or a
one-sided lock in a single explosive turn.

--- Key Cards (4-8) ---
1. Replenish            [ICON]
2. Opalescence
3. Parallax Wave
4. Parallax Tide
5. Attunement
6. Frantic Search
7. Enlightened Tutor
8. Counterspell

--- Strategy ---
Game plan:
The deck digs hard with cantrips and card filtering (Frantic Search, Attunement,
Enlightened Tutor) to pitch its key enchantments into the graveyard, then resolves
Replenish to put every binned enchantment onto the battlefield simultaneously.
Opalescence turns those enchantments into creatures; Parallax Wave removes the
opponent's blockers (or permanently exiles them) while the animated permanents
swing for lethal. Counterspell and discard protect the combo turn. A backup plan
is simply hard-casting Opalescence + Parallax Wave as a grindy removal-and-beatdown
package when the combo is disrupted.

How to win / piloting tips:
- Mulligan aggressively for a hand with both a way to fill the graveyard AND a
  Replenish or a tutor for it.
- Sequence Attunement/Frantic Search to bin enchantments, not just to draw.
- Hold up Counterspell on the turn you go off if the opponent is on permission.

Weaknesses / how to beat it:
- Graveyard hate (Tormod's Crypt, Phyrexian Furnace) blanks Replenish entirely if
  it lands before the combo turn.
- Fast aggro can race the deck before it assembles, since the early turns are spent
  digging rather than interacting.
- Disenchant/Seal of Cleansing on Opalescence post-combo can unravel the board.

Sideboard philosophy:
Bring in counterspells and extra disruption against control and mirror; bring in
sweepers or cheap blockers and life-gain against aggro. Expect graveyard hate from
every opponent post-board and keep enough redundancy (extra tutors / a hard-cast
plan) to win through one piece of hate.

Notable matchups:
- vs Sligh / mono-red aggro: even — they can race the dig-heavy early turns, but
  Parallax Wave + Opalescence stabilizes hard if you survive.
- vs The Rock / discard midrange: unfavored — Duress and Cabal Therapy strip the
  combo before it comes online.
- vs UW Control: favored — the combo goes over the top of permission once you bait
  or counter their Counterspell.

--- Citations & Resources (REQUIRED: at least one) ---
Primary source URL:     https://www.mtgo.com/decklist/premodern-league-...  (example list)
Author / pilot credit:  (pilot name, if from a known event)
Additional resources:   https://www.youtube.com/...  (gameplay/primer video)
Discord handle:         your_handle_here

=== END SUBMISSION ===
```

> The card names, tier, and prose above are illustrative — swap in real,
> citable details. The point of the example is the **shape** of a good
> submission, not these exact values.

---

## How your submission becomes a live page (for the curious)

You can skip this section — it's just so you know nothing is lost in translation.

The maintainer takes your form and turns it into a small editorial file. Only the
fields you wrote get merged onto the archetype page; the pipeline regenerates all
the stats around them on every data pull, so your write-up sticks but the numbers
stay current. Your fields map roughly like this:

- **Description** -> `description`
- **Game plan** -> `gamePlan`
- **How to win / piloting tips** -> `howToWin`
- **Weaknesses / how to beat it** -> `weaknesses` and/or `howToBeat`
- **Sideboard philosophy** -> `sideboardGuide`
- **Notable matchups** -> `matchupMatrix`
- **Tier** -> `tier`
- **Category** -> `category`
- **Key cards + icon flag** -> `keyCards` (the icon becomes the page artwork)

Anything in the "site generates automatically" column is ignored on purpose so we
never overwrite live tournament data with hand-entered numbers.

---

## How to Submit

Pick whichever is easiest — all of these reach the maintainer:

- **Web form:** https://premodernhq.com/contribute (choose "Archetype Primer")
- **GitHub:** open an Issue or Pull Request on the
  [Data Mirror](https://github.com/premodern-wiki/data-mirror) repo and paste your
  filled-in form
- **Discord:** DM **externality_0502**
- **Email:** sv_gravity_400@proton.me

Citations are required (at least one verifiable source). Card legality follows the
official list at **premodernmagic.com**. Thanks for contributing!
