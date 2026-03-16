# Sample API Outputs

These are **real outputs** from the MTG Cube AI system, generated against
live data (33,573 cards, 193 cubes, 95,774 Mana Pool prices).

## Files

| File | Description |
|------|-------------|
| `sample-najeela-deck.json` | AI-generated Commander deck: Bracket 2 Najeela, $300 budget, hipster mode. 65 nonland cards at $156 with per-card Mana Pool pricing and purchase URLs. |
| `sample-cube-pricing.json` | Pro Tour Cube (540) priced on Mana Pool: $4,969.80 total, top 10 most expensive cards, 30th Anniversary budget alternatives saving $288. |
| `sample-similar-cards.json` | Similarity search for Dark Confidant — top 10 AI-matched cards by semantic embedding distance. |
| `sample-commander-info.json` | EDHREC data for Najeela: top synergy cards with inclusion percentages. |
| `sample-rag-search.json` | RAG query "how to build a good reanimator archetype" — returns Lucky Paper podcast transcript passages with timestamps and article content. |

## Key Points for Mana Pool Integration

Every card in every output includes:
- **`price`** — current Mana Pool price
- **`url`** — direct link to buy on manapool.com

The `sample-cube-pricing.json` shows the **30th Anniversary alternatives** feature:
cards over $100 where the 30A printing saves money (e.g., Volcanic Island $486 → $344, save $142).

The `sample-najeela-deck.json` shows a **complete Commander deck** generated from
a natural language prompt, ready to import into Moxfield and purchase on Mana Pool.
