# Sample API Outputs

**Real outputs** from the MTG Cube AI system. Every deck is auto-validated
against the Command Zone 2026 template and auto-fixed to pass.

## Commander Deck Builds (Auto-Fixed, Health Checked)

Each deck is validated against the Command Zone template (38 lands,
10 ramp, 10 draw, 10 removal, 6 board wipes). Gaps are auto-fixed
by swapping low-synergy cards for functional pieces.

| File | Commander | Budget | Cost | Fixes | Health |
|------|-----------|--------|------|-------|--------|
| `sample-deck-najeela-unlimited.json` | Najeela (5-color) | Unlimited | $3,189 | 11 | ✅ PASS |
| `sample-deck-najeela-budget-300.json` | Najeela | $300 | $86 | 8 | ✅ PASS |
| `sample-deck-najeela-budget-100-hipster.json` | Najeela | $100 hipster | $703 | 16 | ✅ PASS |
| `sample-deck-najeela-bracket2-200.json` | Najeela | $200 bracket 2 | $49 | 21 | ✅ PASS |
| `sample-deck-meren-budget-150.json` | Meren (BG) | $150 | $39 | 5 | ✅ PASS |
| `sample-deck-krenko-budget-100.json` | Krenko (mono-R) | $100 | $26 | 0 | ⚠️ |

Each JSON includes:
- Full categorized deck (creatures, instants, lands, etc.)
- Per-card Mana Pool pricing with purchase URLs
- `health_check` with category counts vs template targets
- `auto_fixes_applied` showing what was swapped and why
- `export_text` ready for Moxfield/Archidekt import

## Other Samples

| File | Description |
|------|-------------|
| `sample-cube-pricing.json` | Pro Tour Cube: $4,970 with 30A alternatives |
| `sample-similar-cards.json` | Tag-aware similarity for Cultivate (finds ramp cards) |
| `sample-rag-search.json` | RAG: "reanimator archetype" — transcript + article results |

## Data Behind These Outputs

- 33,573 cards with tag-aware 768-dim embeddings
- 14,174 cards classified (ramp, removal, wipe, draw)
- 95,774 Mana Pool prices
- EDHREC Commander data with bracket filtering
- 11,895 Lucky Paper transcript chunks (cleaned)
