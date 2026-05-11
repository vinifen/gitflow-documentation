# 📋 GitHub Workflow Summary

**Complete quick reference guide for standardized GitHub development workflows, templates, and conventions.**

**Documentation version:** **2.0.0** — canonical value in [`VERSION`](../VERSION) at the repository root.

> 📚 **Source Repository**: [vinifen/gitflow-documentation](https://github.com/vinifen/gitflow-documentation)  
> 🔗 **Get Templates**: Copy templates and configs from the source repository to implement in your project.

> **Guidelines only:** All recommendations in this summary are **non-prescriptive**. They aim at common **good practices**, not strict compliance. **Adapt** branches, templates, commits, and ceremonies per project—keep what helps, drop or change what does not.

## 🎯 Overview

This guide provides a comprehensive workflow system for GitHub projects, including:

- **Two template bundles** at repo root — **`full-github-templates/.github`** and **`simple-github-templates/.github`** — each mirrors a real project layout
- **Full bundle:** 3 issue templates + **`pull_request_template.md`**
- **Simple bundle:** 3 issue templates + **`pull_request_template.md`**
- **Complete Documentation** for branches, commits, issues, PRs, and labels
- **Two adoption profiles**: **full** (emoji, `@dev/` branches) and **simple** (plain commits, lighter branches)
- **Ready-to-use** GitHub templates and configurations

### Adoption profiles (quick pick)

| | **Full** | **Simple** |
|---|----------|------------|
| Branches | `@dev/type/issue/slug` | `type/issue-slug` or `type/slug` |
| Commits | `<emoji> type: msg` | `type: msg` |
| Issues / PRs | Copy **`full-github-templates/.github`** into your repo | Copy **`simple-github-templates/.github`** into your repo |

GitFlow branch topology is unchanged. See [Branches](BRANCHES.md) and [Commits](COMMITS.md).

### 🚀 Implementation
1. **Clone or browse** [vinifen/gitflow-documentation](https://github.com/vinifen/gitflow-documentation)
2. **Copy one bundle** — `full-github-templates/.github` or `simple-github-templates/.github` — to your repository root (result: `./.github/…`)
3. **Adapt** assignees, labels, `config.yml` contact links, and any section that does not fit your team
4. **Use this guide as reference**, not as a fixed rulebook—adjust conventions until they match how your project works best

---

## 🌿 Branch Strategy

### Permanent Branches
- **MAIN** - Production-ready code
- **DEVELOP** - Integration branch for new features

### Working branch formats

**Full**
```
@developer/task-type-issue/short-name
```

**Simple**
```
task-type/issue-short-name
```

### Examples
```bash
# Full profile:
git checkout -b @john/feat/123/user-dashboard
git checkout -b @jane/fix/124/login-validation

# Simple profile:
git checkout -b feat/123/user-dashboard
git checkout -b fix/124/login-validation

# Release / hotfix (either profile)—version in the name is optional until you release:
git checkout main && git checkout -b hotfix/125/critical-bug-v1.1
git checkout develop && git checkout -b hotfix/126/quick-fix-no-version
git checkout develop && git checkout -b release/127/v1.2
```

> 💡 **Note**: In the full profile, adapt `@username` to match your team (GitHub handle, initials, etc.).

---

## 📝 Commit Convention

### Format

**Full:** `<emoji> <type>: <description>`  
**Simple:** `<type>: <description>` (no emoji)

### Rules
- Write in **English**
- Use **lowercase** for description
- Keep under **60 characters**
- Use **imperative mood** (add, fix)

### Examples
```bash
# Full
git commit -m "✨ feat: add user authentication"

# Simple
git commit -m "feat: add user authentication"
git commit -m "fix: resolve login timeout"
```

---

## 🏷️ Change Types

| Emoji | Type | Description |
|-------|------|-------------|
| ✨ | `feat` | New feature or functionality |
| 🔧 | `fix` | Bug fix or error correction |
| 🎨 | `style` | Code style changes (formatting) |
| 📖 | `docs` | Documentation updates |
| ♻️ | `refactor` | Code restructuring without behavior change |
| 🚀 | `perf` | Performance improvements |
| ⚙️ | `chore` | Maintenance tasks |
| 🏗️ | `infra` | Infrastructure changes |
| 🧪 | `test` | Adding or updating tests |
| 📈 | `enhancement` | Incremental improvements |
| 🚧 | `wip` | Work in progress |
| 🔖 | `release` | Release preparation |
| 🔥 | `hotfix` | Urgent fixes—**usually production** (`main`); sometimes `develop` only |

---

## 📋 Issue Templates

**Both bundles use the same filenames** under `.github/ISSUE_TEMPLATE/` (`1_development_task.md`, `2_bug_report.md`, `3_suggestion.md`, plus `config.yml`). Pick **`full-github-templates`** or **`simple-github-templates`** at clone/copy time; you never mix filenames—only the **body** (and default `blank_issues_enabled`) changes.

| File | Title hint | Label | Full bundle | Simple bundle |
|------|------------|-------|-------------|----------------|
| `1_development_task.md` | `[TASK: TYPE] …` | `task` | Detailed sections | Few sections |
| `2_bug_report.md` | `[BUG] …` | `bug-report` | Full repro / environment | Short repro |
| `3_suggestion.md` | `[SUGGESTION] …` | `suggestion` | Context + rationale | Short idea |

With the **simple** bundle, **blank issues** are allowed by default (`blank_issues_enabled: true`). **Full** defaults to `false`.

---

## 🔀 Pull Request Guidelines

### Branch-Specific Rules
- **MAIN**: Normal merge (no squash/rebase)
- **DEVELOP**: Typically squashed
- **RELEASE**: Include or reference the version when you are shipping or tagging a release (team convention).
- **HOTFIX**: **Typically** merged toward **main** / production; version in commits or branch name is **recommended** there. If the hotfix targets **develop** only, versioning is **optional** until you release.

### Title format

**Full:** `✨ feat: example for a feature pull request`  
**Simple:** `feat: example for a feature pull request`

### Templates
- **full** — Related issue, overview, type, time spent, extended checklist
- **simple** — Summary, related issue; optional time-spent section left commented in `pull_request_template.md`

---

## 🏷️ Labels & Colors

### Core Labels (Auto-applied)
- `task` - Development work (`#0052CC` - Blue)
- `bug-report` - Problem reports (`#D73A49` - Red)
- `suggestion` - Ideas (`#FFD700` - Yellow)

### Additional Labels (Manual)
- `documentation` - Docs (`#0075CA` - Blue)
- `test` - Testing (`#1D76DB` - Blue)
- `fix` - Bug fixes (`#D73A49` - Red)
- `hotfix` - Urgent fixes—usually production (`#FF0000` - Red)
- `infrastructure` - Infra (`#FF8C00` - Orange)
- `refactoring` - Code cleanup (`#FBCA04` - Yellow)

### Color Scheme
- **Red** - Critical issues (bugs, fixes, hotfixes)
- **Blue** - Development work (tasks, docs, tests)
- **Yellow/Orange** - Improvements (suggestions, refactoring, infrastructure)

---

## 🚀 Quick Workflow Examples

**Full** = `@dev/…` branches + emoji commits · **Simple** = `type/issue-slug` + plain `type:` (see [Branches](BRANCHES.md), [Commits](COMMITS.md)). Same steps; only naming and commit style change.

### Feature (issue → branch → commits → PR)

```bash
# Issue e.g. [TASK: FEAT] Add user dashboard → open PR to develop, link #123
git checkout develop && git pull
git checkout -b @vinifen/feat/123/user-dashboard    # simple: feat/123/user-dashboard
git commit -m "✨ feat: add dashboard layout"       # simple: feat: add dashboard layout
git commit -m "✨ feat: implement user stats"        # simple: feat: implement user stats
```

### Bug fix

```bash
# Issue e.g. [BUG] Login validation error
git checkout develop && git pull
git checkout -b @vinifen/fix/124/login-validation     # simple: fix/124/login-validation
git commit -m "🔧 fix: resolve login form validation" # simple: fix: resolve login form validation
```

### Hotfix

Usually from **main** (A); from **develop** (B) when integration comes first. Version in branch/message optional until release—see [BRANCHES](BRANCHES.md).

```bash
# A — main (typical production patch)
git checkout main && git pull && git checkout -b hotfix/125/critical-security
git commit -m "🔥 hotfix: patch security issue"       # simple: hotfix: … ; add vX.Y.Z when you tag

# B — develop
git checkout develop && git pull && git checkout -b hotfix/126/config-rollback
git commit -m "🔥 hotfix: restore config default"     # simple: hotfix: …
```

---

## 📦 Template bundle layout

Copy **one** of `full-github-templates/.github` or `simple-github-templates/.github` to your repo root. Result:

```text
.github/
├── ISSUE_TEMPLATE/
│   ├── 1_development_task.md
│   ├── 2_bug_report.md
│   ├── 3_suggestion.md
│   └── config.yml
└── pull_request_template.md
```

Core issue labels (`task`, `bug-report`, `suggestion`) should exist in the repo—see [NEW-LABELS](NEW-LABELS.md) for **GitHub CLI** commands and colors.

---

## 📖 Documentation Links

### 📚 Full Documentation (Source Repository)
- [🌿 Branches](https://github.com/vinifen/gitflow-documentation/blob/main/docs/BRANCHES.md) - Branch strategy and naming
- [📝 Commits](https://github.com/vinifen/gitflow-documentation/blob/main/docs/COMMITS.md) - Commit message standards
- [📋 Issues](https://github.com/vinifen/gitflow-documentation/blob/main/docs/ISSUES.md) - Issue templates and lifecycle
- [🔀 Pull Requests](https://github.com/vinifen/gitflow-documentation/blob/main/docs/PULL-REQUESTS.md) - PR process and guidelines
- [🏷️ Change Types](https://github.com/vinifen/gitflow-documentation/blob/main/docs/TYPES-CHANGES.md) - Semantic change classification
- [🏷️ Labels](https://github.com/vinifen/gitflow-documentation/blob/main/docs/NEW-LABELS.md) - Repository labels and colors
- [🔢 Semantic Versioning](https://github.com/vinifen/gitflow-documentation/blob/main/docs/SEMVER.md) - Version numbering standards

### 🛠️ Setup Resources
- [GitHub Templates Documentation](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests)
- [GitHub CLI Installation](https://cli.github.com/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitFlow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

---

## ✅ Best Practices

### Issues
- Use correct title format: `[TYPE] Description`
- Fill the template sections that add value for your team
- Replace placeholders with real information
- Apply appropriate labels
- Link related issues/PRs

### Commits
- Use **full** (`emoji type:`) or **simple** (`type:`) consistently
- Write in English, lowercase description
- Keep under 60 characters
- Use imperative mood

### Pull Requests
- Link to related issue
- Use the **`pull_request_template.md`** from the bundle you installed (**full** vs **simple**)
- Apply matching labels
- Complete all checklist items (full bundle includes time spent)

### Branches
- Use correct naming format
- Create from appropriate base branch (**hotfix usually from `main`** for production; **develop** when your process calls for it)
- Delete after successful merge
- Include version when you **release** or tag; hotfixes on **develop** alone may skip version until then

**Assistive / AI:** Attribute Git work to the **human** author and your **full/simple** conventions—never replace them with model or tool names in commits or branch names. Details: [Branches](BRANCHES.md), [Commits](COMMITS.md).

## 📄 License & Attribution

This workflow system is provided by [vinifen/gitflow-documentation](https://github.com/vinifen/gitflow-documentation) under the MIT License.

**When using these workflows:**
- ✅ **Free to use** and adapt for any project
- ✅ **No attribution required** but appreciated
- ✅ **Modify** templates and processes as needed
- ✅ **Share improvements** back to the community

---

*This summary consolidates all workflow documentation from [vinifen/gitflow-documentation](https://github.com/vinifen/gitflow-documentation). For the most up-to-date information and detailed documentation, visit the source repository.*
