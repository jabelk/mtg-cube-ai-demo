# Sample API Outputs

**Real outputs** from the MTG Cube AI system — not mockups.

## Commander Deck Builds (with Health Checks)

Each deck includes per-card Mana Pool pricing, Moxfield export text,
and a Command Zone template health check (ramp, draw, removal gaps).

| File | Commander | Budget | Cost | Health |
|------|-----------|--------|------|--------|
| `sample-deck-najeela-unlimited.json` | Najeela (5-color) | Unlimited | $3,224 | GAPS (low removal) |
| `sample-deck-najeela-budget-300.json` | Najeela | $300 | $98 | GAPS |
| `sample-deck-najeela-budget-100-hipster.json` | Najeela | $100 hipster | $35 | GAPS |
| `sample-deck-najeela-bracket2-200.json` | Najeela | $200 bracket 2 | $52 | GAPS |
| `sample-deck-meren-budget-150.json` | Meren (BG) | $150 | $38 | GAPS |
| `sample-deck-krenko-budget-100.json` | Krenko (mono-R) | $100 | $26 | GAPS |

Health checks flag where the deck needs more ramp, draw, removal,
or board wipes based on the Command Zone 2026 template. GAPS are
expected for auto-generated decks — the `check_deck_health` tool
suggests specific cards to fix them.

## Other Samples

| File | Description |
|------|-------------|
| `sample-cube-pricing.json` | Pro Tour Cube: $4,970 with 30A alternatives saving $288 |
| `sample-similar-cards.json` | AI similarity search for Dark Confidant |
| `sample-rag-search.json` | RAG: "how to build reanimator" — transcript + article results |

## Data Behind These Outputs

- 33,573 cards with 768-dim embeddings + Scryfall oracle tags
- 95,774 Mana Pool prices (daily refresh)
- 14,174 cards classified (ramp, removal, wipe, draw)
- EDHREC data with bracket filtering + synergy scores
- 11,907 Lucky Paper transcript chunks for RAG
