# Player DNA similarity · methodology

## What is Player DNA?

Player DNA is Rising Transfers' semantic representation of **how** a player plays — not just their raw counting stats. It is built from per-90 performance signals across attacking, passing, defending, and (for goalkeepers) shot-stopping metrics, aggregated over a full season.

Each player with sufficient minutes receives a 768-dimensional embedding. Cosine similarity between two embeddings yields a score from 0 to 1:

| Score | Interpretation |
|---|---|
| 0.85+ | Very similar stylistic profile |
| 0.75–0.85 | Strong overlap |
| 0.65–0.75 | Partial overlap |
| < 0.65 | Different profiles |

## What this repository publishes

- **players.csv** — index of 450 curated players (BIG 50 European squads + World Cup spotlight names)
- **similarity.csv** — top-10 similar players per indexed player only

We deliberately do **not** publish:
- Raw embedding vectors (768-dim)
- Full pairwise similarity matrices
- Third-party market values

## Player selection

1. Squads from 50 top European clubs (Premier League full + top clubs in La Liga, Serie A, Bundesliga, Ligue 1)
2. Star exceptions (global names outside top-5 leagues, e.g. MLS / Saudi)
3. World Cup 2026 curated spotlight players
4. Capped at ~400 players to balance coverage and model protection

## Attribution

> Data: Rising Transfers — risingtransfers.com

Interactive profiles: `https://risingtransfers.com/en/players/{slug}/alternatives`
