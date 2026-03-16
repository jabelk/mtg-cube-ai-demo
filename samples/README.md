# Sample API Outputs

**Real outputs** from the MTG Cube AI system. Decks are auto-validated
and auto-fixed against the Command Zone 2026 template.

## Commander Deck Builds

| File | Commander | Budget | Cost | Fixes | Health |
|------|-----------|--------|------|-------|--------|
| `sample-deck-najeela-unlimited.json` | Najeela (5-color) | Unlimited | $3,184 | 11 | ✅ PASS |
| `sample-deck-najeela-budget-300.json` | Najeela | $300 | $95 | 8 | ✅ PASS |
| `sample-deck-najeela-budget-100-hipster.json` | Najeela | $100 hipster | $40 | 9 | ✅ PASS |
| `sample-deck-najeela-bracket2-200.json` | Najeela | $200 bracket 2 | $65 | 21 | ⚠️ |
| `sample-deck-meren-budget-150.json` | Meren (BG) | $150 | $39 | 5 | ✅ PASS |
| `sample-deck-krenko-budget-100.json` | Krenko (mono-R) | $100 | $106 | 19 | ✅ PASS |

Each JSON includes: categorized deck, per-card Mana Pool pricing,
`health_check`, `auto_fixes_applied`, and `export_text` for Moxfield.

## Other Samples

| File | Description |
|------|-------------|
| `sample-cube-pricing.json` | Pro Tour Cube: $4,970 with 30A alternatives |
| `sample-similar-cards.json` | Tag-aware similarity for Cultivate (ramp) |
| `sample-rag-search.json` | RAG: "reanimator archetype" results |
