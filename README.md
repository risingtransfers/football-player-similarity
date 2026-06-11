# Football Player Similarity Dataset

An open dataset of **stylistic similarity between football players** — "who plays like X" — computed with AI semantic embeddings of playing style.

Covers **hundreds of players** across Europe's top leagues. For each player, the top-10 most stylistically similar players are listed with similarity scores.

Maintained by [Rising Transfers](https://risingtransfers.com).

## Why this dataset is different

Traditional football stats sites tell you *what* a player did (goals, passes, tackles). This dataset answers a different question: **which other players play in a similar style?**

That makes it useful for:
- **Scouting** — find cheaper or younger players who play like a target
- **Transfer analysis** — identify realistic alternatives when a signing falls through
- **Fantasy / betting** — find like-for-like replacements when a player is injured or rotated

## What's inside

| File | Contents |
|---|---|
| `data/players.csv` | Player index: name, position, club, league, style tags |
| `data/similarity.csv` | Top-10 most similar players for each player, with similarity scores (0–1) |

## Quick start

Every player has a `slug`. Look up the full interactive similarity profile here:

https://risingtransfers.com/en/players/{slug}/alternatives

Example — players who play like Rodri:
https://risingtransfers.com/en/players/rodri/alternatives

## Methodology

Similarity is computed using **Player DNA**, a semantic embedding that represents each player's style as a high-dimensional vector built from per-90 performance signals. Cosine similarity between vectors gives the similarity score (0–1).

This repository publishes **model outputs only** — the top-10 similar players per player. Raw vectors are not included.

Coverage: hundreds of players from Europe's top five leagues plus selected internationals. For full coverage of 56,000+ players, see [risingtransfers.com](https://risingtransfers.com).

## License

Released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Attribution:

> Data: Rising Transfers — risingtransfers.com

## Related datasets from Rising Transfers

- [world-cup-2026-data](https://github.com/risingtransfers/world-cup-2026-data) — all 48 World Cup squads with per-90 stats
- [football-data-glossary](https://github.com/risingtransfers/football-data-glossary) — metrics & methodology reference
