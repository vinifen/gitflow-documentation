## Types of Changes

Commit types with emojis to indicate the purpose of a change in commits, pull requests, or version control history, making it easier to understand the context of each update at a glance.

**Types:**

- ✨ feat: - A new feature or functionality added to the project.
- 🔧 fix: - A bug fix or error correction in the codebase.
- 🎨 style: - Code style changes (formatting, indentation, spacing) with no logic impact.
- 📖 docs: - Documentation updates (README, comments, guides, API docs).
- ♻️ refactor: - Code restructuring or cleanup without changing behavior.
- 🚀 perf: - Code change that improves performance.
- ⚙️ chore: - Maintenance tasks (dependencies, configs, CI/CD, build scripts).
- 🏗️ infra: - Infrastructure or environment changes (servers, Docker, pipelines).
- 🧪 test: - Adding or updating tests to improve coverage and reliability.
- 📈 enhancement: - Incremental improvements to existing functionality (not a new feature).
- 🚧 wip: - A temporary commit marking work in progress, not ready for merge.
- 🔖 release: - Preparation for a new release, including version bump and changelog update.
- 🔥 hotfix: - An urgent fix, usually applied directly to production; must update version.

## Commits

Commits must always be written in English and begin with the task emoji, followed by a space, a colon (:), another space, and a short lowercase message.

**Example:**
```commit_example
git commit -m "✨ feat: example for a feature commit"
```