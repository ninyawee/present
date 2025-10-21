# The Present Manifesto

Present reimagines curated lists by using **data-driven karma scoring** to automatically surface what's actually being used in the wild.

## The Problem with Traditional Awesome Lists

Traditional awesome lists suffer from:
- **Stagnation** - Popular libraries stay at the top even when better alternatives emerge
- **Manual burden** - Maintainers can't keep up with the evolving ecosystem
- **Subjective bias** - Rankings reflect past popularity, not current relevance
- **Outdated recommendations** - Deprecated or unmaintained libraries linger

## How Present Works

### Karma-Based Ranking

Present calculates a **karma score** for each library using:

1. **Usage frequency** - How often the library appears in:
   - GitHub public repositories
   - GitHub private repositories (with privacy controls)

2. **Star count** - Community validation and popularity

3. **Recent activity** - Recent commits, releases, and adoption trends

The formula prioritizes libraries that are **actively used today**, not just historically popular.

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
- Current karma score
- Usage count (anonymized)
- Star count
- Last updated timestamp
- Trending indicator (↑ rising, ↓ falling, → stable)

This gives users context to make informed decisions.

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
