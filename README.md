# MTG Cube AI — Demo Showcase

An AI-powered deck building platform with live Mana Pool marketplace
pricing, EDHREC Commander data, and cube design knowledge from Lucky
Paper. 23+ MCP tools for conversational deck building via Claude.

## What It Does

Talk to Claude about Magic deck building with real data behind every
answer — 33,573 cards with AI embeddings, 95,774 Mana Pool prices,
193 curated cubes, 11,895 Lucky Paper transcript chunks, and EDHREC
Commander data with bracket filtering.

---

## Commander Deck Builder

Build complete 100-card Commander decks from natural language with
budget constraints, bracket filtering, hipster mode, and automatic
deck health validation.

```
> "Build me a bracket 2 Najeela deck for $300 using hipster cards"

  Commander: Najeela, the Blade-Blossom
  Bracket: Core (2)
  Style: Hipster — avoiding top EDHREC staples
  Total Cards: 99 + commander
  Total Cost: $94 on Mana Pool

  Deck Health Check:
    ✅ Lands: 38  |  ✅ Ramp: 10  |  ✅ Card Draw: 10
    ⚠️ Targeted Removal: 4 (need 6 more)
    ⚠️ Mass Removal: 1 (need 5 more)
    Suggestions: Swords to Plowshares, Wrath of God, ...

  Every card has a manapool.com purchase URL
  Export text ready for Moxfield/Archidekt import
```

### Budget Scaling

| Commander | Budget | Cost | Nonlands | Lands | Fixing |
|-----------|--------|------|----------|-------|--------|
| Najeela (5-color) | Unlimited | $3,224 | 65 | 34 | 25 nonbasic |
| Najeela | $300 | $94 | 61 | 38 | 33 fixing |
| Najeela | $100 hipster | $33 | 53 | 46 | 32 fixing |
| Meren (BG) | $150 | $36 | 57 | 42 | 35 fixing |
| Krenko (mono-R) | $100 | $25 | 59 | 40 | 13 fixing |

### Commander Exploration

```
> "Show me top Izzet commanders"

  Vivi Ornitier                (27,998 decks)
  Ghyrson Starn, Kelermorph    (18,846 decks)
  Niv-Mizzet, Parun            (15,798 decks)

> "Tell me about Najeela"

  Top synergy cards:
    Samut, Vizier of Naktamun   58% synergy
    Derevi, Empyrial Tactician  53% synergy
    Druids' Repository          45% synergy
```

---

## Deck Health Check

Validates any deck against the **Command Zone 2026 template**
using Scryfall oracle tags for card classification.

```
> "Check my deck's health"

  Template: 38 lands, 10 ramp, 10 draw, 10 removal, 6 mass removal

  ✅ Lands:              31 (target: 38) — compensated by 21 ramp
  ✅ Ramp:               21 (target: 10) — exceeds target
  ✅ Card Draw:          10 (target: 10) — on target
  ❌ Targeted Removal:    4 (target: 10) — need 6 more
  ❌ Mass Removal:        1 (target: 6)  — need 5 more

  Suggestions for targeted removal:
    Swords to Plowshares, Path to Exile, Beast Within...
```

Card classification powered by Scryfall oracle tags:
- 2,082 ramp cards
- 6,203 removal cards
- 902 board wipes
- 4,987 card draw cards

---

## Live Marketplace Pricing (Mana Pool Integration)

**95,774 card prices** from Mana Pool with direct purchase links.

```
> "Price the Pro Tour Cube"

  Total Cost: $4,969.80
  Average Card: $9.45
  Cards Priced: 526/526

  Most Expensive:
    Mox Diamond          $931.08   → manapool.com/card/sth/138/mox-diamond
    Tropical Island      $380.84   → manapool.com/card/cei/284/tropical-island

  💡 30th Anniversary Budget Alternatives:
    Volcanic Island: $486 → $344 (30A) — save $142
    Tundra:          $373 → $276 (30A) — save $97
    Savannah:        $258 → $208 (30A) — save $49
    Total Savings: $288 by switching to 30A printings
```

### Vendor Sourcing

```
> "Source these cards from Mana Pool"

  Available: 45/50 cards ($234.56)
  Missing: 5 cards

  AI Substitutions for missing cards:
    [Missing Card] → [Available Alternative] $2.50
      "Similar effect, in stock on Mana Pool"
```

---

## Card Intelligence

**33,573 cards** with tag-aware AI embeddings. Each card's embedding
includes its function tags (ramp, removal, board wipe, card draw) so
similarity search clusters cards by what they *do*, not just what
they look like.

```
> "Find cards similar to Cultivate"  (ramp)

  Rampant Growth             distance=0.2061
  Explore                    distance=0.1969
  Flare of Cultivation       distance=0.1371

> "Find cards similar to Shock"  (removal)

  Sudden Shock               distance=0.1673
  Electrify                  distance=0.2775
  Explosive Impact           distance=0.2674
```

### EDHREC-Enhanced Suggestions

```
> "Suggest Meren BG reanimator cards for my cube"

  Reanimate             score=5  (keyword + EDHREC synergy)
  Necromancy            score=4  (keyword + EDHREC synergy)
  Dread Return          score=4  (keyword + EDHREC synergy)
  Spore Frog            score=3  (EDHREC synergy for Meren)
  Plaguecrafter         score=3  (EDHREC synergy for Meren)
```

---

## Cube Analysis

**193 curated cubes** from CubeCon 2022-2025 with full card associations.

```
> "Analyze the Pro Tour Cube"

  Color Distribution: White 21.5% | Blue 20.7% | Black 22.1% |
                      Red 20.5% | Green 20.9%
  Mana Curve: Heavy 1-3 CMC, classic powered cube
  Types: 43% creatures, 15% instants, 12% artifacts
  Verdict: Exceptionally well-balanced
```

---

## Cube Design Knowledge (RAG)

**57 Lucky Paper articles + 11,907 podcast transcript chunks** with
semantic search.

```
> "What does Lucky Paper say about reanimator?"

  [TRANSCRIPT] Going Against Your Intuition (~16:00)
    "fell specter is a modern creature that has the same
     meagre static text, and so I was looking at reanimator
     as an archetype that ties together..."

  [TRANSCRIPT] Modern Horizons 2 Set Review (~306:40)
    "priest of fell rites — return target creature card
     from your graveyard to the battlefield, activate
     only as a sorcery..."

  [ARTICLE] Frequently Asked Questions About Cube
    "Cube is a custom draft format. Designers choose and
     assemble their favorite cards into a re-draftable set..."
```

---

## Deck Import & Export

Import from Moxfield, Archidekt, or any text format. Export to any
deck builder tool.

```
> "Import my Moxfield deck at moxfield.com/decks/abc123"
  → Fetches all cards via API, resolves against our database
  → Ready for analysis, pricing, health check, suggestions

> "Export this deck for Moxfield"
  → "1 Najeela, the Blade-Blossom *CMDR*\n1 Sol Ring\n..."
  → Copy-paste into any deck building tool
```

---

## Content Creator Decklists

Browse decks from your favorite Commander content creators, priced
on Mana Pool.

```
> "Show me Commander's Quarters decks"

  Creator: Mitch (Commander's Quarters)
  Profile: moxfield.com/users/commandersquarters

  1. Budget Staples You Should Be Buying Right Now
  2. Jasmine Boreal of the Seven — $25.40
  3. Why These 7 Commander Cards Are Seriously Underrated
  ...
```

### Known Creators

| Creator | Show | Moxfield |
|---------|------|----------|
| Brian Kibler | Commander at Home | @Kibler |
| Olivia Gobert-Hicks | Commander at Home | @affinityartifacts |
| Seth (SaffronOlive) | MTGGoldfish Commander Clash | @SaffronOlive |
| Crim | MTGGoldfish Commander Clash | @TheAsianAvenger |
| Mitch | Commander's Quarters | @commandersquarters |
| Playing With Power | Playing With Power MTG | @playingwithpowermtg |
| MTGMuddstah | MTGMuddstah | @MTG_Muddstah |

---

## Precon Upgrades

Upgrade recommendations for Commander precons with Mana Pool pricing.

```
> "Upgrade my Bloomburrow precon for $30"

  Upgrades to add (12 cards, $28.50):
    Beast Whisperer        $2.50  — card draw for creature decks
    Heroic Intervention    $5.00  — protection
    ...

  Export text ready for Mana Pool purchase
```

Buy the precon + upgrade pieces from Mana Pool = one shipment.

---

## Top 100 Commander Decks

AI-generated $200 budget decks for EDHREC's top 100 commanders.
See the `top100-decks/` folder — each includes health check,
Mana Pool pricing, and Moxfield export.

**84% pass** the Command Zone template health check. Every card
has a `manapool.com` purchase URL.

---

## Smart Land Base Builder

Budget decks get proper mana fixing — not just basic lands.

| Budget | Before | After |
|--------|--------|-------|
| Najeela $300 | 1 fixing + 37 basics | 33 fixing + 5 basics |
| Najeela $100 | 0 fixing + 46 basics | 32 fixing + 5 basics |
| Meren $150 | 5 fixing + 37 basics | 35 fixing + 5 basics |

Picks guildgates, painlands, temples, utility lands —
all under $2 each.

---

## Data Foundation

| Data | Count |
|------|-------|
| Cards (Scryfall, all with AI embeddings) | 33,573 |
| Card Tags (ramp, removal, wipe, draw) | 14,174 classified |
| Cubes (CubeCon 2022-2025 + user cubes) | 193 |
| Cube-Card Associations | 36,032 |
| Card Prices (Mana Pool, daily refresh) | 95,774 |
| Lucky Paper Articles (with embeddings) | 57 |
| Podcast Episodes (transcribed) | 303 |
| Transcript Chunks (RAG, cleaned) | 11,895 |
| EDHREC Commander Data | Cached on-demand |

## Architecture

- **MCP Server**: 20+ tools, Claude connects directly
- **Database**: Supabase (PostgreSQL + pgvector)
- **Embeddings**: OpenAI text-embedding-3-small (768-dim, tag-aware)
- **Pricing**: Mana Pool public API (95K+ cards)
- **Commander Data**: EDHREC JSON endpoints with bracket filtering
- **Deck Validation**: Scryfall oracle tags + Command Zone template
- **Storage**: Cloudflare R2 (podcast audio + transcripts)

---

## Mana Pool Integration Opportunity

### What exists today:
- Every card suggestion includes live Mana Pool pricing
- "Price my cube/deck" with per-card breakdown + purchase URLs
- 30th Anniversary budget alternatives for expensive cards
- AI finds substitute cards that ARE available on Mana Pool
- Commander deck builder → price → export → buy
- Deck health validation ensures playable decks before purchase

### What Andrew's team could add:
- **Seller filter on optimizer API** → single-vendor sourcing
- **"Shop CubeCon Cubes"** → browse 193 cubes, one-click buy
- **Commander deck → cart** → AI builds, validates, prices, buys

### The pitch:
AI builds the deck. Validates it against the Command Zone template.
Prices it on Mana Pool. User buys with one click.
Every suggestion is a potential sale.
