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
	<a href="awesome.md">What is Present?</a>&nbsp;&nbsp;&nbsp;
	<a href="contributing.md">Contribution guide</a>&nbsp;&nbsp;&nbsp;
	<a href="create-list.md">Creating a list</a>
</p>

<br>

## What is Present?

**Present** is a new approach to curated awesome lists. Instead of manually maintaining lists where outdated libraries stay at the top forever, Present uses **karma-based ranking** to automatically surface what's actually being used right now.

### How it works

Present calculates a **karma score** for each library using a **two-tier ranking system**:

#### Tier 1: Battle-Tested (Actively Used)
Libraries that appear in actual codebases:
- **Repository usage** - Found in GitHub public and private repositories
- **Star count** - Community validation
- **Recent activity** - Active development and adoption

#### Tier 2: Under Evaluation (Bookmarked)
Libraries from GitHub user star lists (e.g., `github.com/stars/username/lists/present-python`):
- **Star list inclusions** - How many users bookmarked it for future use
- **Star list context** - What users think it's good for
- **Emergence signal** - New libraries gaining attention

**Why two tiers?**

Libraries in Tier 1 are **proven in production** - developers are using them right now. Libraries in Tier 2 are **interesting and promising** - developers are evaluating them but haven't committed yet. This distinction helps you understand:
- **Tier 1**: Safe bets, battle-tested
- **Tier 2**: Worth watching, potential future leaders

Both tiers are valuable, but Tier 1 always ranks higher because actual usage beats bookmarks.

### Privacy-aware filtering

Present includes a **wildcard deny config** that lets you exclude:
- Internal private organization libraries
- Proprietary patterns that shouldn't be ranked publicly
- Custom exclusion rules for your use case

This keeps the lists focused on publicly relevant libraries while respecting organizational privacy.

### Why Present?

Traditional awesome lists have a problem:
- Once a library reaches the top, it tends to stay there
- Maintainers can't keep up with the changing landscape
- New, better alternatives get buried below legacy options

Present solves this by **automating the curation process** based on real-world usage data.

---

## Contents

- [Programming Languages](#programming-languages)

## Programming Languages

- [Python](https://github.com/CircleOnCircles/present-python#readme)

## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Nutchanon Ninyawee](https://nutchanon.org) has waived all copyright and related or neighboring rights to this work.
