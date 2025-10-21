# The Present Manifesto

Present reimagines curated lists by using **data-driven karma scoring** to automatically surface what's actually being used in the wild.

## The Problem with Traditional Awesome Lists

Traditional awesome lists suffer from:
- **Stagnation** - Popular libraries stay at the top even when better alternatives emerge
- **Manual burden** - Maintainers can't keep up with the evolving ecosystem
- **Subjective bias** - Rankings reflect past popularity, not current relevance
- **Outdated recommendations** - Deprecated or unmaintained libraries linger

## How Present Works

### Karma-Based Ranking with Two Tiers

Present uses a **two-tier ranking system** that separates battle-tested libraries from emerging ones:

#### Tier 1: Battle-Tested (Production Usage)

Libraries ranked by **actual usage** in codebases:

1. **Repository usage frequency** - How often the library appears in:
   - GitHub public repositories
   - GitHub private repositories (with privacy controls)

2. **Star count** - Community validation and popularity

3. **Recent activity** - Recent commits, releases, and adoption trends

**Tier 1 libraries are proven** - developers are using them in real projects right now.

#### Tier 2: Under Evaluation (Bookmarked)

Libraries ranked by **developer interest** from GitHub star lists:

1. **Star list inclusions** - How many users added it to their curated lists
   - Example: `github.com/stars/ninyawee/lists/present-python`
   - Each user can curate their own "awesome" list

2. **Star list diversity** - Appearing in multiple users' lists shows broader interest

3. **Emergence velocity** - Rate of new bookmarks (trending potential)

**Tier 2 libraries are promising** - developers are evaluating them but haven't deployed yet.

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
- **Karma score** - Overall ranking within tier
- **Usage count** (Tier 1) / Star list inclusions (Tier 2) - Anonymized
- **Star count** - Total GitHub stars
- **Last updated** - Timestamp of last data refresh
- **Trending indicator** - (↑ rising, ↓ falling, → stable)

**Example display:**

```
🔥 Tier 1: Battle-Tested
1. requests (⭐ 48.2k | 📊 15.3k repos | ↑ +245 this week) - HTTP for Humans
2. django (⭐ 74.1k | 📊 12.8k repos | → stable) - High-level web framework
...

🌟 Tier 2: Under Evaluation
1. httpx (⭐ 11.2k | 📋 892 star lists | ↑ +89 this week) - Next-gen HTTP client
2. fastapi (⭐ 65.4k | 📋 1.2k star lists | ↑ +156 this week) - Modern async API framework
...
```

This gives users complete context to make informed decisions about which tier matches their risk tolerance.

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
