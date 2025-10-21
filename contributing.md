# Contribution Guidelines

Please note that this project is released with a [Contributor Code of Conduct](code-of-conduct.md). By participating in this project you agree to abide by its terms.

## How Present is Different

Present uses **automated karma-based ranking**, so contributions are different from traditional awesome lists:

- **No manual library additions** - Rankings are automated based on usage data
- **Focus on system improvements** - Contribute to the algorithm and infrastructure
- **Category expansion** - Help us cover new domains and ecosystems

## Ways to Contribute

### 1. Improve the Karma Algorithm

Help make our ranking system better:

- Suggest new signals for library relevance
- Propose weight adjustments in `present.config.yml`
- Report libraries that are ranked incorrectly
- Contribute research on better ranking methodologies

**How to contribute:**
1. Open an issue describing the improvement
2. Provide data/examples supporting your proposal
3. If accepted, submit a PR with changes to the algorithm

### 2. Refine Privacy Filters

Help improve the deny pattern system:

- Suggest common patterns for internal libraries
- Report false positives (public libraries being excluded)
- Report false negatives (private libraries leaking through)
- Contribute organization-specific pattern examples

**How to contribute:**
1. Edit `present.config.yml` with your suggested patterns
2. Explain the use case in your PR description
3. Provide examples of libraries it should/shouldn't match

### 3. Add New Categories

Expand Present to new programming languages or domains:

- Create a new Present list for a language/ecosystem
- Follow the [create-list.md](create-list.md) guide
- Configure appropriate deny patterns
- Set up initial category structure

**Required for new lists:**
- Clear scope definition
- Initial deny pattern configuration
- Category organization
- Description of what's included/excluded

### 4. Report Issues

Help us maintain accuracy:

**Library Issues:**
- Library ranked too high/low
- Deprecated library still showing
- False positive in deny patterns
- Privacy leak (internal library exposed)

**System Issues:**
- Karma score calculation bugs
- Configuration not working as expected
- Performance problems
- Data collection errors

**How to report:**
1. Open a GitHub issue with label `bug` or `ranking-issue`
2. Include specific library name and current karma score
3. Explain what's wrong and what you expect
4. Provide supporting data if possible

### 5. Improve Documentation

- Clarify how karma scoring works
- Add examples to configuration documentation
- Improve setup guides
- Translate documentation

## What NOT to Contribute

Since Present is automated, please don't:

- Submit PRs to manually add libraries (they're added automatically)
- Request specific libraries be moved up/down (that's algorithm-determined)
- Suggest subjective "awesome" lists (we use objective usage data)

## Development Setup

If you want to contribute code:

```bash
# Clone the repository
git clone https://github.com/CircleOnCircles/present.git

# Install dependencies
npm install  # or appropriate package manager

# Run tests
npm test

# Configure your environment
cp present.config.yml.example present.config.yml
# Edit present.config.yml with your settings
```

## Pull Request Guidelines

1. **One change per PR** - Keep PRs focused
2. **Test your changes** - Ensure tests pass
3. **Update documentation** - If you change behavior
4. **Follow existing style** - Match the codebase conventions
5. **Explain your reasoning** - Why is this change beneficial?

## Questions?

- Check existing [issues](https://github.com/CircleOnCircles/present/issues)
- Read the [manifesto](present.md) to understand Present's philosophy
- Open a new issue for questions

## Updating Your Pull Request

Sometimes maintainers will request changes before merging. [Here's a guide](https://github.com/RichardLitt/knowledge/blob/master/github/amending-a-commit-guide.md) on how to update your PR.
