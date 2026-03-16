# MTG Cube AI — Demo Showcase

An AI-powered deck building platform with live marketplace pricing.
Built for cube designers and Commander players.

## What It Does

19 MCP tools that let you talk to Claude about Magic deck building
with real data behind every answer.

---

## Card Intelligence

**33,573 cards** with AI embeddings for semantic similarity search.

```
> "Find cards similar to Dark Confidant"

  Keen Duelist               — same effect, budget alternative
  Novice Occultist           — pay life for cards theme
  Disciple of Bolas          — sacrifice for card advantage
  Pain Seer                  — inspired Dark Confidant variant
```

---

## Cube Analysis

**193 curated cubes** from CubeCon 2022-2025 with full card associations.

```
> "Analyze the Pro Tour Cube"

  Color Distribution:
    White: 113 (21.5%)  |  Blue: 109 (20.7%)  |  Black: 116 (22.1%)
    Red: 108 (20.5%)    |  Green: 110 (20.9%)

  Mana Curve: Heavy at 1-3 CMC, classic powered cube shape
  Type Split: 43% creatures, 15% instants, 12% sorcery, 12% artifacts

  → Verdict: Exceptionally well-balanced across all five colors
```

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
    Volcanic Island      $343.90   → manapool.com/card/30a/282/volcanic-island

  💡 30th Anniversary Budget Alternatives:
    Volcanic Island: $486 → $344 (30A) — save $142
    Tundra:          $373 → $276 (30A) — save $97
    Savannah:        $258 → $208 (30A) — save $49
    Total Savings: $288 by switching to 30A printings
```

---

## Commander Deck Builder (EDHREC Powered)

Build complete Commander decks from natural language with bracket
filtering, budget constraints, and style preferences.

```
> "Build me a bracket 2 Najeela deck for $300 using hipster cards"

  Commander: Najeela, the Blade-Blossom
  Bracket: Core (2)
  Style: Hipster — avoiding top EDHREC staples
  Budget: Under $300

  Generated 65+ nonland cards at $156.32
  All cards priced on Mana Pool with purchase links
  Exportable to Moxfield/Archidekt format
```

```
> "Show me top Izzet commanders"

  Vivi Ornitier                (27,998 decks)
  Ghyrson Starn, Kelermorph    (18,846 decks)
  Niv-Mizzet, Parun            (15,798 decks)
  Stella Lee, Wild Card         (15,047 decks)
```

---

## Archetype-Aware Card Suggestions

Keyword search + AI embeddings find cards that fit specific archetypes.

```
> "Suggest BG reanimator cards for my Pro Tour Cube"

  Reanimate         — the best reanimation spell, $X on Mana Pool
  Necromancy         — enchantment-based, harder to interact with
  Coffin Queen       — repeatable reanimation engine
  Phyrexian Tower    — sacrifice outlet that ramps
  Entomb             — instant-speed tutor to graveyard
```

---

## Cube Design Knowledge (RAG)

**57 Lucky Paper articles + 11,907 podcast transcript chunks** with
semantic search. Ask "why" questions about cube design and get answers
grounded in expert knowledge.

```
> "What does Lucky Paper say about how many lands to run?"

  [EPISODE] How Many Lands Should you Include in Your Cube?
    Andy and Anthony discuss precedents from other formats...
    → luckypaper.co/podcast/107

  [TRANSCRIPT] The Cube Player's Guide to Manabases (~37:20)
    "...if I'm playing a green white deck I might not actually
    need 17 lands to be able to consistently cast my spells..."
    → luckypaper.co/podcast/058

  [ARTICLE] How Many Lands Should You Include in Your Cube?
    Analysis drawing from retail limited format data...
    → luckypaper.co/articles/how-many-lands-should-you-include
```

---

## Deck Import & Export

Import from Moxfield, Archidekt, or any text format. Export to any
deck builder tool.

```
> "Import my Moxfield deck at moxfield.com/decks/abc123"
  → Fetches all cards, resolves against our database
  → Ready for analysis, pricing, suggestions

> "Export this deck for Moxfield"
  → Generates "1 Card Name" format with *CMDR* tags
  → Copy-paste into any deck building tool
```

---

## Data Foundation

| Data | Count |
|------|-------|
| Cards (Scryfall, all with AI embeddings) | 33,573 |
| Cubes (CubeCon 2022-2025 + user cubes) | 193 |
| Cube-Card Associations | 36,032 |
| Card Prices (Mana Pool, daily refresh) | 95,774 |
| Lucky Paper Articles (with embeddings) | 57 |
| Podcast Episodes (transcribed) | 303 |
| Transcript Chunks (RAG searchable) | 11,907 |
| EDHREC Commander Data | Cached on-demand |

---

## Architecture

- **MCP Server**: 19 tools, Claude connects directly
- **Database**: Supabase (PostgreSQL + pgvector)
- **Embeddings**: OpenAI text-embedding-3-small (768-dim)
- **Pricing**: Mana Pool public API (95K+ cards)
- **Commander Data**: EDHREC JSON endpoints
- **Storage**: Cloudflare R2 (podcast audio + transcripts)

---

## Mana Pool Integration Opportunity

### What exists today:
- Every card suggestion includes live Mana Pool pricing
- "Price my cube/deck" with per-card breakdown + purchase URLs
- 30th Anniversary budget alternatives for expensive cards
- AI finds substitute cards that ARE available on Mana Pool

### What Andrew's team could add:
- **Seller filter on optimizer API** → enables single-vendor sourcing
  ("buy all 100 cards from one seller, one shipping fee")
- **"Shop CubeCon Cubes"** → browse 193 curated cubes, one-click
  price and buy on Mana Pool
- **Commander deck → cart** → AI builds the deck, Mana Pool fills
  the order

### The pitch:
AI builds the deck. Mana Pool sells the cards. Every suggestion is
a potential sale. The AI becomes an acquisition funnel for the
marketplace.
