# Tournament Result Submission Template

Use this to submit the standings from a Premodern event so it appears on premodernhq.com. You do not need to know any code: just copy the **Quick Copy Block** below, fill it in, and send it via any method listed at the bottom.

Every submission needs a **source link** (a tournament report or decklist page anyone can open to verify the results). Submissions without a citation cannot be accepted. Card legality follows [premodernmagic.com](https://premodernmagic.com).

---

## What we need

### Required (event info)

| Field | What to put | Example |
| --- | --- | --- |
| **Event name** | The full event name | `Lobstercon 2026 - North American Championship` |
| **Date** | The day it was held, as `YYYY-MM-DD` | `2026-05-01` |
| **Format** | `premodern` or `unchained` | `premodern` |
| **Player count** | Total number of players who entered | `326` |
| **Location** | `City, Country` for paper, or `Online` | `Cambridge, MA, USA` |
| **Source URL** | Link to a verifiable report / standings / decklist host | `https://mtgtop8.com/event?e=84398&f=PREM` |

### Required (standings — one row per player)

For each finisher, give: **place**, **player name**, **archetype**, and a **decklist link** (if one exists).

* **Place** — finishing position (`1`, `2`, `3` ...). Ties are fine — write the same place for tied players (e.g. two players at `3`).
* **Player** — the player's name as it appeared in the event.
* **Archetype** — the deck name in plain English (e.g. `Replenish`, `Sligh (RDW)`, `The Rock`). Don't worry about exact spelling or "official" names — we map it to a canonical archetype on our end.
* **Decklist link** — a URL to that player's list. Attach it **to that player's row** (see format below). Leave it blank if there's no list for that player; the result still counts.

### Optional / nice to have

* As many standings rows as you have (full Top 8, Top 16, Top 32, or the whole field — more is better).
* A separate note if part of the field has decklists and part doesn't.

You do **not** need to provide a star rating or "qualifying" flag — those are calculated automatically from player count and event type.

---

## How decklist links attach to standings

Each decklist URL belongs to **one player's row**. Put the link right after that player's archetype on the same line, so there is never any doubt whose list it is:

```
1. Brian Siu - Replenish - https://mtgtop8.com/event?e=84398&d=841314&f=PREM
```

If a player has no published list, just omit the link — keep the place, name, and archetype:

```
7. Nicholas Mostovych - Pit Rack
```

Lists can come from anywhere verifiable (MTGTop8, TCDecks, MTGGoldfish, Moxfield, a tournament report, etc.). They do not all have to be from the same site.

---

## Quick Copy Block (fill this in)

```
Event Name:   <full event name>
Date:         <YYYY-MM-DD>
Format:       <premodern | unchained>
Player Count: <number>
Location:     <City, Country | Online>
Source URL:   <link anyone can open to verify the results>

Standings (place - player - archetype - decklist link):
1. <player> - <archetype> - <decklist URL>
2. <player> - <archetype> - <decklist URL>
3. <player> - <archetype> - <decklist URL>
3. <player> - <archetype> - <decklist URL>
5. <player> - <archetype> - <decklist URL>
...
```

---

## Filled-in Example

```
Event Name:   Lobstercon 2026 - North American Championship @ Cambridge (MA)
Date:         2026-05-01
Format:       premodern
Player Count: 326
Location:     Cambridge, MA, USA
Source URL:   https://mtgtop8.com/event?e=84398&f=PREM

Standings (place - player - archetype - decklist link):
1.  Brian Siu        - Replenish    - https://mtgtop8.com/event?e=84398&d=841314&f=PREM
2.  Bryan Gulotta    - Replenish    - https://mtgtop8.com/event?e=84398&d=841315&f=PREM
3.  Claire Ackerman  - Oath Ponza   - https://mtgtop8.com/event?e=84398&d=841316&f=PREM
3.  Stuart Ziarnik   - Sligh (RDW)  - https://mtgtop8.com/event?e=84398&d=841318&f=PREM
5.  Ben Bauer        - Elves        - https://mtgtop8.com/event?e=84398&d=841319&f=PREM
5.  Galen Lemei      - Full English Breakfast - https://mtgtop8.com/event?e=84398&d=841317&f=PREM
7.  Nicholas Mostovych - Pit Rack   - https://www.tcdecks.net/deck.php?id=43463&iddeck=457055
9.  Andreas Voellmer - Landstill    - https://mtgtop8.com/event?e=84398&d=841325&f=PREM
```

(Note how places `3` and `5` repeat for tied finishers, and how each decklist link sits on its owner's row. The Pit Rack list comes from TCDecks while the others come from MTGTop8 — mixing hosts is fine.)

---

## The citation requirement

**Every submission must include a Source URL** that lets a maintainer independently verify the standings — for example:

* an MTGTop8 / TCDecks / MTGGoldfish event page,
* a written tournament report (blog, forum thread, Discord post with results),
* an organizer's published standings or bracket.

If the results are spread across more than one link (e.g. standings on one page, decklists on another), include all of them. A submission with no verifiable source can't be added.

---

## How to submit

Send your filled-in block through whichever is easiest:

* **Web form:** [premodernhq.com/contribute](https://premodernhq.com/contribute)
* **GitHub:** open an Issue or Pull Request on the [Data Mirror](https://github.com/premodern-wiki/data-mirror) (paste the block into an Issue, or add a file in a PR)
* **Discord DM:** `externality_0502`
* **Email:** `sv_gravity_400@proton.me`

Not sure about a field? Send what you have plus the source link — a maintainer will follow up. Thanks for helping build the Premodern record!
