# Bacon Board

**An open-source endorsement game: six degrees of separation, pointed at the people we'd most like to talk to.**

Hollywood worked out that everyone on Earth is [six handshakes from Kevin Bacon](https://en.wikipedia.org/wiki/Six_Degrees_of_Kevin_Bacon). Bacon Board points those handshakes somewhere useful. [Something Better Australia](https://somethingbetteraustralia.com) (SBA) — an evidence-led grassroots movement working toward Australia's next major political party — names the conversations it would most like to have, by description rather than by name, and the community plays a forwarding game to bridge to those people through their own networks. No cold messages. No mass campaigns. Community-governed, built in public.

## Why this exists

The people most worth talking to are the hardest to reach honourably. Cold email gets deleted, unsolicited DMs get ignored, and both deserve it. Yet nearly everyone in Australia is a handful of warm introductions away from nearly everyone else — the network exists; what's missing is a respectful way to traverse it. Bacon Board is an attempt to build that traversal as open source, with consent engineered in from the first commit.

## Project status: zero

There is no code in this repository yet. No stack has been chosen. No architecture exists.

That's the pitch, not the apology. Bacon Board is at the design stage, and the people who show up now define what it becomes — the endorsement graph, the link-minting model, the serialised introduction queue, the consent flows. If you've ever looked at a social system and thought *I'd have designed the trust model differently*, this is the rare moment where you actually get to.

## How an endorsement works

1. **SBA lists a quest, by description.** Someone they'd like to talk to — described, not named, while the endorsement is in motion.
2. **You start an endorsement.** Request a private link from the quest page. The link is yours, and it has five charges.
3. **You forward to five people.** People you trust who you think are closer to the destination than you are. When someone clicks your link, the system mints them a new private link with its own five charges.
4. **The endorsement branches outward.** Each forwarder learns the destination's name only at the moment they decide to forward, so they can choose who's closer. Degrees of separation and elapsed time are tracked.
5. **It closes through a warm introduction.** The closing forwarder — someone who personally knows the destination — makes a discreet introduction on SBA's behalf. Accept, and it's recorded and can be closed publicly. Decline, and it ends quietly; no second endorsement is ever started toward that person.

Quests have four states — open, in motion, closed-accepted, closed-declined — and SBA publishes every outcome, including the declines. Your shortest path from forwarder to destination, counted in warm introductions, is your Bacon number; it feeds a leaderboard of top connectors.

## The rules

This is the part that matters. The mechanic is a game; the rules are invariants, and the system stands or falls on enforcing them:

1. **Destinations are described, not named, on the public board.** Identity propagates only down an endorsement, only to forwarders who need it to choose the next hop.
2. **Endorsements never reach the destination directly.** The closing forwarder makes a single warm introduction — that is the only contact.
3. **Converging endorsements are serialised.** If several paths reach the same person, there is one introduction, not five.
4. **A decline is permanent.** The endorsement ends quietly and no new endorsement is ever started toward that person.
5. **Each person can be a Quest exactly once.**
6. **Connector names are displayed only with consent.** Opt anonymous and only SBA knows it's you.
7. **SBA enforces all of the above.** Any endorsement that crosses these lines is closed, and any connector who tries is removed.

## What Bacon Board is not

Bacon Board is not cold outreach, not a mass-messaging or growth-hacking tool, and not a way to pressure or dox anyone. It is consent-first and introduction-based: names surface only when a destination accepts, connectors are anonymous by default, and every decline is respected permanently. A forwarding game that doesn't hold those lines is just spam with extra steps — so the lines hold.

## Contributing — who we need

The repo is at zero, which means every one of these areas is greenfield and whoever takes it on sets the standard. Fair warning: the consent and anti-abuse design is the hard, interesting part — that's where the real engineering lives.

- **Backend engineering** — you know that a private link with five charges is a graph problem with teeth, and you want to build the endorsement graph, the link-minting model, the serialised warm-introduction queue, and the anti-abuse layer that keeps the game honest.
- **Product design** — you know the make-or-break moment is one person deciding whether to forward a political introduction to a friend, and you want to design the invitation and consent flows — the hardest UX on the project.
- **Research** — you think effective network reach in a country the size of Australia is a genuinely open question, and you want the data to answer it: path lengths, branching behaviour, where endorsements stall and why.

Start in [issues](../../issues) or [discussions](../../discussions). There's no contribution ladder to climb yet — the first serious proposal in each area effectively becomes the draft standard.

## Governance & licence

Bacon Board is community-governed under the umbrella of [Something Better Australia](https://somethingbetteraustralia.com), owned by no party. Governance decisions and quest outcomes will live in this repository, in public — including the declines.

**Licence:** [MIT](LICENSE). Use it, fork it, audit it — that's the point.

---

Bacon Board is one piece of a larger bet: that Australian politics can be done better — hopeful, evidence-led, and accountable. That bet is [Something Better Australia](https://somethingbetteraustralia.com). Come shorten the path.
