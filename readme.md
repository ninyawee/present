<div align="center">
	<img width="500" height="350" src="media/logo.svg" alt="Present">
	<br>
	<br>
	<h1>Present</h1>
	<p>
		<strong>Karma-based awesome lists that stay relevant</strong>
	</p>
	<br>
</div>

<p align="center">
	<a href="present.md">What is Present?</a>&nbsp;&nbsp;&nbsp;
	<a href="contributing.md">Contribution guide</a>&nbsp;&nbsp;&nbsp;
	<a href="create-list.md">Creating a list</a>
</p>

<br>

## What is Present?

**Present** is a federated, org-level approach to curated awesome lists. Instead of relying on global GitHub stars, Present tracks **actual usage** in your organization's repositories and aggregates across communities.

### Federated Architecture

Present operates at two levels:

#### 1. Org/User Level (e.g., `ninyawee/present-python`)
Your organization's or personal view based on:
- **Your repos** - What libraries YOUR projects actually use
- **Your star lists** - What YOU'RE evaluating (e.g., `github.com/stars/ninyawee/lists/present-python`)
- **Your context** - Relevant to your team's tech stack and needs

#### 2. Federated Level (e.g., `present/thailand-present-python`, `present/global-present-python`)
Aggregated views across organizations showing:
- **Community trends** - What multiple orgs are using
- **Geographic context** - Thailand-specific, Asia-specific, etc.
- **Time windows** - Recent (3 months), established (1 year), mature (3 years), legacy (5 years)

This federated model ensures you see both **your reality** and **broader trends**.

### How it works

Present ranks libraries by **project count**, not GitHub stars. The ranking uses a **two-tier system**:

#### Tier 1: Battle-Tested (Actively Used)
Ranked by **number of projects** (repos) using the library:
- **Project count** - How many repositories have this in their dependencies
- **Time windows** - Filter by recent usage (3 months, 1 year, 3 years, 5 years)
- **Recency weight** - Recent usage counts more than old usage

**Example:** `requests` used in 847 projects (3 months), 2,341 projects (1 year), 5,128 projects (3 years)

#### Tier 2: Under Evaluation (Bookmarked)
Ranked by **star list inclusions** across users:
- **Star list count** - How many users bookmarked it (e.g., in `github.com/stars/username/lists/present-python`)
- **Diversity** - Breadth across different users/orgs
- **Emergence rate** - Growth in bookmarks

**Example:** `httpx` in 89 star lists (3 months), 234 star lists (1 year)

### Why Project Count, Not Stars?

**Stars are ignored** because they don't reflect actual usage:
- ⭐ **Stars** = "I think this is interesting" (low commitment)
- 📊 **Project count** = "I'm using this in production" (high commitment)

A library with 50k stars but only 10 projects using it is **hype, not proven**.
A library with 5k stars but 1,000 projects using it is **battle-tested**.

### Time Windows Show Evolution

- **3 months** - What's hot RIGHT NOW, recent migrations, new adoption
- **1 year** - Established choices, proven stability
- **3 years** - Mature ecosystem, long-term viability
- **5 years** - Legacy but proven, or potentially outdated

You can see if a library is **rising** (more recent usage) or **declining** (only old usage).

### Privacy-aware filtering

Present includes a **wildcard deny config** that lets you exclude:
- Internal private organization libraries
- Proprietary patterns that shouldn't be ranked publicly
- Custom exclusion rules for your use case

This keeps the lists focused on publicly relevant libraries while respecting organizational privacy.

### Why Present?

Traditional awesome lists have fatal flaws:
- **Star-based** - Popularity ≠ Production usage
- **Static** - Once at the top, libraries stay there forever
- **Manual** - Maintainers can't keep up with ecosystem changes
- **Global only** - No org-level or regional context

Present solves this with:
- **Usage-based** - Project count > Star count
- **Time-aware** - See what's used NOW vs what WAS used
- **Automated** - Rankings update based on real data
- **Federated** - See your org's reality + global trends

### Real-World Example

**Your Org Level (`ninyawee/present-python`):**
```
🔥 Tier 1: Battle-Tested (in your repos)
1. django - 12 projects (your team loves it)
2. fastapi - 8 projects (new adoption)
3. flask - 3 projects (legacy apps)
```

**Federated Level (`present/thailand-present-python`):**
```
🔥 Tier 1: Battle-Tested (across Thailand orgs)
1. fastapi - 245 projects (3 months) - Thai startups prefer this
2. django - 189 projects (3 months) - Still strong
3. flask - 156 projects (1 year) - Declining, mostly legacy
```

**Global Level (`present/global-present-python`):**
```
🔥 Tier 1: Battle-Tested (worldwide)
1. django - 15.3k projects (1 year) - Enterprise standard
2. fastapi - 8.2k projects (3 months) - Rising fast
3. flask - 12.1k projects (3 years) - Mature but plateauing
```

You see **your reality**, **your community**, and **global trends** - all based on actual usage, not hype.

---

## Contents

- [Programming Languages](#programming-languages)

## Programming Languages

- [Python](https://github.com/CircleOnCircles/present-python#readme)

## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Nutchanon Ninyawee](https://nutchanon.org) has waived all copyright and related or neighboring rights to this work.
