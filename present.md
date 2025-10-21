# The Present Manifesto

Present reimagines curated lists as **federated, usage-driven rankings** that show what's actually being used in production, not just what's popular on GitHub.

## The Problem with Traditional Awesome Lists

Traditional awesome lists suffer from fatal flaws:
- **Star worship** - Confuse popularity with production readiness
- **Stagnation** - Libraries stay at the top forever once they reach it
- **Manual burden** - Maintainers can't keep up with ecosystem evolution
- **No context** - Global lists ignore org-level and regional differences
- **No time awareness** - Can't distinguish current from legacy usage

## The Present Solution: Federated Usage-Based Rankings

Present operates on three principles:

### 1. Project Count > Star Count

**Stars are meaningless for production decisions.**
- 50k stars with 100 projects using it = Hype
- 5k stars with 10k projects using it = Battle-tested

Present ranks by **project count** (how many repos use it), not stars.

### 2. Federated Architecture

Present runs at **org/user level** and aggregates up:
- **Org Level** (`ninyawee/present-python`) - What YOUR teams use
- **Community Level** (`present/thailand-present-python`) - Regional trends
- **Global Level** (`present/global-present-python`) - Worldwide usage

This gives you context: "Is this just us, or is everyone using it?"

### 3. Time-Aware Ranking

View usage across windows:
- **3 months** - What's being adopted RIGHT NOW
- **1 year** - Established and proven
- **3 years** - Mature ecosystem
- **5 years** - Legacy (might be outdated)

This reveals trends: rising, stable, or declining.

## How Present Works

### Ranking System: Two Tiers

Present uses a **two-tier ranking** that separates production usage from evaluation:

#### Tier 1: Battle-Tested (Production Usage)

Ranked purely by **project count** (how many repos use it):

1. **Project count** - Number of repositories with this dependency
   - Counts both public and private repos (with privacy controls)
   - Time-windowed: 3 months, 1 year, 3 years, 5 years

2. **Recency weight** - Recent usage counts more than old usage
   - A library with 1k projects (3 months) ranks higher than 1k projects (5 years)

3. **Scope** - Org-level, community-level, or global
   - Your org's projects vs regional vs worldwide

**Tier 1 formula:** `karma = project_count × recency_multiplier`

**Example:**
- `requests`: 847 projects (3 months) → karma = 847 × 1.5 = 1,270
- `urllib3`: 1,200 projects (5 years) → karma = 1,200 × 0.8 = 960

Recent adoption wins over legacy usage.

#### Tier 2: Under Evaluation (Bookmarked)

Ranked by **star list inclusions** (bookmarks for future use):

1. **Star list count** - How many users bookmarked it
   - Example: `github.com/stars/ninyawee/lists/present-python`
   - Each developer curates their "watching" list

2. **Diversity** - Breadth across different users/teams
   - 10 bookmarks from 10 different users > 10 from 1 user

3. **Emergence rate** - Growth in bookmarks over time
   - Time-windowed: 3 months, 1 year, 3 years

**Tier 2 formula:** `karma = star_list_count × diversity_score × emergence_rate`

**Example:**
- `httpx`: 89 users bookmarked (3 months) → emerging
- `aiohttp`: 234 users bookmarked (3 years) → established alternative

Tier 2 shows what developers are **watching**, not using yet.

### Why Two Tiers Matter

**The bookmark gap is meaningful:**
- A library in your star list is **interesting** but not yet **trusted** enough for production
- It might be awesome for future use, but you're waiting to see how it matures
- This signals: "I'm watching this, but not betting on it yet"

**Ranking philosophy:**
- **Tier 1 always ranks above Tier 2** - Usage > Interest
- Within each tier, karma scores determine order
- Libraries can graduate from Tier 2 to Tier 1 as adoption grows

**This solves the cold-start problem:**
- New libraries can gain visibility through star lists (Tier 2)
- As they prove themselves, they naturally rise to Tier 1
- No need to wait years for manual list maintainers to notice

### Privacy-Aware Configuration

Present includes a wildcard deny config system to exclude:

```yaml
deny_patterns:
  - "internal-*"           # Internal organization libraries
  - "company-private/*"    # Private company namespaces
  - "@myorg/*"             # Organization-specific packages
  - "*.local"              # Local-only dependencies
```

This ensures:
- **Privacy protection** - Internal libraries won't leak into public rankings
- **Relevance** - Only publicly useful libraries are ranked
- **Flexibility** - Custom patterns for different use cases

## Automated Updates

Present lists update automatically:
- **No manual curation** needed for rankings
- **Real-time reflection** of ecosystem changes
- **Transparent methodology** - Data-driven, not opinion-driven

## Transparency and Trust

Each library listing includes:
- **Tier badge** (🔥 Tier 1: Battle-Tested | 🌟 Tier 2: Under Evaluation)
- **Project count** (Tier 1) / Star list count (Tier 2)
- **Time window** - When this usage occurred
- **Trend indicator** - (↑ rising, ↓ falling, → stable)
- **Scope** - Org / Community / Global

**Stars are NOT shown** - they're irrelevant to production decisions.

**Example display for `present/thailand-present-python`:**

```
🔥 Tier 1: Battle-Tested (Thailand orgs, 3 months)
1. fastapi      - 245 projects | ↑ +89 (from 1 year) | Rising fast
2. django       - 189 projects | → stable | Established choice
3. flask        - 156 projects | ↓ -43 (from 1 year) | Legacy declining
4. requests     - 312 projects | → stable | Ubiquitous utility

🌟 Tier 2: Under Evaluation (Thailand devs, 3 months)
1. httpx        - 89 star lists | ↑ emerging | Watching requests replacement
2. pydantic     - 67 star lists | ↑ rising | FastAPI companion
3. strawberry   - 34 star lists | → new | GraphQL interest
```

**Comparison across time windows:**

```
fastapi:
- 3 months:  245 projects (current adoption)
- 1 year:    156 projects (+57% growth)
- 3 years:    45 projects (+444% growth)
→ Clearly rising, becoming dominant

flask:
- 3 months:  156 projects (current usage)
- 1 year:    199 projects (-22% decline)
- 3 years:   287 projects (-46% decline)
→ Legacy, being replaced
```

This transparency lets you make informed decisions based on **actual production usage**, not hype.

## Creating a Present List

1. **Define the scope** - What category of libraries (e.g., Python web frameworks)
2. **Configure filters** - Set up deny patterns for your privacy needs
3. **Set update frequency** - How often to recalculate karma scores
4. **Add descriptions** - Explain what each category covers

The system handles the rest automatically.

## Contributing

Since Present is automated, contributions focus on:
- **Improving the karma algorithm** - Better signals for relevance
- **Refining deny patterns** - Better privacy controls
- **Adding categories** - Expanding coverage to new domains
- **Reporting false positives** - Helping improve accuracy

See [contributing.md](contributing.md) for details.

## Philosophy

> **What's awesome changes over time. Present adapts automatically.**

Present respects that:
- **Usage is proof** - If developers are using it, it's relevant
- **Recency matters** - Recent activity signals current viability
- **Data beats opinion** - Objective metrics over subjective curation
- **Privacy is essential** - Internal tooling stays internal
