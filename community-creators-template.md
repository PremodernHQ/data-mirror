# Community Creator Template

Use this template to submit a Premodern **blog, podcast, YouTube channel, stream, newsletter, or Discord** to the Community Hub at premodernhq.com/media.

New to this? Don't worry — you only need a name, what kind of thing it is, and a link. Copy the block below, fill in the blanks, and submit it using any of the methods at the bottom.

## Required Fields
*   **Name:** The display name of the creator, show, or channel (e.g., Premodcast)
*   **Type:** One of: `podcast` | `blog` | `video` | `stream` | `newsletter` | `community`
    *   `video` = a YouTube channel or video series
    *   `community` = a forum/subreddit/group (use this for a Discord too)
*   **URL:** The main link — podcast feed, blog homepage, YouTube channel, etc. Must be a real, working link.
*   **Description:** 1–2 sentences on what they cover (decks, tournament coverage, brewing, interviews, etc.)
*   **Still active?:** Yes / No — are they currently producing new content?

## Optional Fields
*   **Author / Host:** Who runs it (creator name or handle)
*   **Language:** Content language if not English (e.g., German, Japanese)
*   **Recommended starting link:** A good first episode or post for newcomers
*   **Tags:** A few keywords, e.g., `brewing`, `tournament-coverage`, `deck-techs`, `interviews`, `meta-analysis`

## The Links Rule
*   Links must be **verifiable** (they actually open and work) and **on-topic** — the content must be dedicated to, or substantially about, **Premodern** Magic: The Gathering.
*   General MTG channels that only occasionally touch Premodern are usually not a fit.

## Example (filled out)

*   **Name:** Premodcast
*   **Type:** podcast
*   **URL:** https://premodcast.buzzsprout.com/
*   **Description:** Popular Premodern MTG podcast covering tournament results, deck techs, and format discussion.
*   **Still active?:** Yes
*   **Author / Host:** (optional)
*   **Language:** English
*   **Recommended starting link:** (optional — link to a favorite episode)
*   **Tags:** tournament-coverage, deck-techs, format-discussion

### How it's stored (for reference)

The maintainer turns your submission into an entry in `data/media/creators.json` that looks like this:

```json
{
  "id": "premodcast",
  "name": "Premodcast",
  "type": "podcast",
  "description": "Popular Premodern MTG podcast covering tournament results, deck techs, and format discussion.",
  "url": "https://premodcast.buzzsprout.com/",
  "active": true,
  "tags": ["tournament-coverage", "deck-techs", "format-discussion"]
}
```

You do **not** need to write JSON — the prose block above is enough. The `id` (a kebab-case slug) is generated for you.

> Submitting a **Discord server**? Use type `community`. Discord servers may be listed in the dedicated Discord Directory; just include the invite link and a one-line description of the server's focus (regional hub, archetype tech, etc.).

## How to Submit
Pick whichever is easiest for you:
*   **Web form:** premodernhq.com/contribute
*   **GitHub:** Open an Issue or Pull Request on the [Data Mirror](https://github.com/premodern-wiki/data-mirror) — paste your filled-in template into an Issue, or add to the JSON directly in a PR.
*   **Discord:** DM `externality_0502`
*   **Email:** sv_gravity_400@proton.me

---
*Citations / verifiable links are required for all submissions.*
