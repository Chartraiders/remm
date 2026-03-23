# REMM — Rade Engine Match Making

**Chart Raiders · Rade Engine Module · Deploying 2026**

REMM is the world's first adaptive AI matchmaking engine built for financial markets. It powers competitive day trading matches on Chart Raiders — the world's first DayTradeSport platform — by dynamically adjusting match parameters to real-time market conditions.

---

## What REMM Does

Traditional trading gives every user the same experience regardless of what the market is doing. A slow market session is boring. A volatile session is overwhelming. REMM solves this by reading market conditions every session and selecting the optimal match format automatically.

**The core principle:** slow markets create shorter, more frequent matches for more profit opportunities. Fast markets create longer matches to spread volatility and protect capital.

No other financial platform has built adaptive matchmaking of this kind. REMM is an industry first.

---

## How It Works

REMM analyzes the maximum price movement over the past 60 minutes and selects one of five match archetypes:

| Archetype | Market Movement | Match Duration | Why |
|---|---|---|---|
| Sprint | 0–40% (very slow) | 17 minutes | Quick cycles maximize profit opportunities in dead markets |
| Quick | 41–59% (slow) | 25 minutes | Balanced pace for mild conditions |
| Standard | 60–79% (normal) | 30 minutes | Default competitive experience |
| Extended | 80–99% (fast) | 35 minutes | Extra time to manage elevated volatility |
| Marathon | 100%+ (very fast) | 60 minutes | Maximum time to spread risk across wild market swings |

When the first player joins a match, all parameters lock. Everyone in that match competes under identical, frozen conditions — the same archetype, the same market snapshot, the same prize pool. This is the fairness guarantee.

---

## Contest Structure & Platform Classification

REMM powers a **peer-to-peer contest platform**. Understanding the structure is important:

- **Players compete against each other** — not against Chart Raiders
- **Chart Raiders is the platform operator** — it charges a fee for operating the service and does not participate as a player, set odds, take positions, or act as a counterparty
- **Chart Raiders is a Game of Skill** — REMM creates the structured competitive environment in which player skill determines match outcomes
- **Players never buy, sell, or hold securities** — REMM matches are conducted within a fictional bankroll environment using publicly available market data
- **Payouts are by rank** — prizes are distributed based on where players finish relative to each other, not based on the direction or value of any underlying asset

**Pre-match transparency:** All players are informed before the match begins of total entrants, the complete prize pool and distribution, and the ticker being analyzed. No information is withheld.

---

## Match Tiers

REMM supports four entry tiers:

| Tier | Entry | Target Player |
|---|---|---|
| Sponsored | Free | Learning the platform |
| Standard | $10 ticket | Casual competitors |
| Premium | $100 ticket | Serious traders |
| Elite | $1,000 ticket | High-stakes professionals |

---

## Sponsored Ticket System

Loyal users can earn free entry into paid matches. Slots are calculated to maintain platform sustainability:

- **Standard matches:** 1 sponsored slot per 15 paid players
- **Premium matches:** 1 sponsored slot per 30 paid players

Priority for sponsored slots is determined by usage count (ascending) — users who have used fewer sponsored tickets are prioritized first.

---

## Match Start Conditions

A match starts when one of two conditions is met:

1. **Recommended player count reached** — match starts immediately
2. **10-minute countdown expires** — match starts with however many players joined (minimum 2)

Maximum 3 match starts per hour per match type.

---

## Reconnection

- **60-second grace period** to reconnect after disconnection
- **Slot reserved** during the grace period
- **State preserved** — score and position intact on reconnection
- **Up to 3 reconnects** per user per match

---

## Production Specifications

REMM v4.0:

- **Rate limiting:** Token bucket algorithm, 10 tokens/sec per user
- **Circuit breakers:** Three-state protection for all external dependencies
- **Metrics:** Full observability with Prometheus-compatible export
- **A/B testing:** Built-in experimentation framework with statistical significance testing
- **Admin controls:** Full match management with append-only audit log (SOC2 certification in preparation)

**Test coverage:** 27/27 v4.0 feature tests · 50,000 stress iterations · 500,000 backward compatibility tests — all pass at 100%.

---

## Integration

REMM runs inside **Rade Engine**. It connects to REMMR at match completion, feeding verified results into the skill rating pipeline.

→ **Website:** https://chartraiders.com/gamified-trading  
→ **FAQ:** https://chartraiders.com/faq  
→ **Creator:** c0tt0nc4ndyta — Founder of Chart Raiders, Inventor of DayTradeSport

---

*Chart Raiders is the world's first DayTradeSport platform. Players never hold securities. Payouts are determined by player rank — a Game of Skill.*
