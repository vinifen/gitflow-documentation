# 📋 Gitflow Documentation

#### v2.0.0

**Complete GitHub workflow templates and documentation for standardized development processes.**

## 🎯 Overview

This repository provides a comprehensive set of GitHub templates, workflow guidelines, and best practices to implement consistent development processes across all your projects. From issue tracking to pull request management, branch strategies to commit conventions - everything you need for a professional development workflow.

### Guidelines, not strict rules

Everything here—templates, branch naming, commits, labels, and checklists—is **guidance** oriented toward **good practices**. None of it is mandatory or one-size-fits-all. **Adapt** any part of this workflow to what works best for your team, product, and constraints: skip sections, simplify templates, mix profiles, or replace conventions entirely when that improves clarity and delivery.

### Two adoption profiles

| Profile | Branches | Commits / PR titles | Templates |
|---------|----------|---------------------|-----------|
| **Full** | `@dev/type/issue/slug`, emoji in titles when useful | `<emoji> type: message` | Bundle [`full-github-templates/.github`](full-github-templates/.github) → copy into your repo root |
| **Simple** | `type/issue-slug` or `type/slug`, no emoji required | `type: message` (Conventional Commits) | Bundle [`simple-github-templates/.github`](simple-github-templates/.github) → copy into your repo root |

GitFlow (main, develop, feature/release/hotfix flow) is the same for both; profiles differ in **strictness and ceremony**. Each bundle uses the **same `.github` layout and filenames** (`ISSUE_TEMPLATE/1_development_task.md`, `2_bug_report.md`, `3_suggestion.md`, `config.yml`, and `pull_request_template.md`) so you can copy either folder into a repo without renaming—only **template bodies** and **`blank_issues_enabled`** differ (`true` in simple, `false` in full by default).

### 📁 Template bundles (copy into your project)

```text
full-github-templates/.github/          # full profile
simple-github-templates/.github/        # simple profile
```

From your project root (pick one profile):

```bash
cp -r path/to/gitflow-documentation/full-github-templates/.github .
# or
cp -r path/to/gitflow-documentation/simple-github-templates/.github .
```

## ✨ What's Included

### 📝 **Issue Templates**
- **Same three files in both bundles:** `1_development_task.md`, `2_bug_report.md`, `3_suggestion.md` (🛠️ / 🐛 / 💡 in the picker)—**full** has richer sections, **simple** keeps them short

### 🔖 **Pull request template**
- Each bundle includes **`.github/pull_request_template.md`** (default filename [recognized by GitHub](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/creating-a-pull-request-template-for-your-repository))
- **full** — Structured overview, type, time spent, extended checklist
- **simple** — Summary, related issue; optional time-spent block (commented in the template)

### 📚 **Complete Documentation**
- **Branch management** strategies and naming conventions
- **Commit guidelines** with emoji conventions
- **Issue lifecycle** and management processes
- **Change type** definitions and classifications
- **Labeling & colors** definitions and setup (labels, colors, CLI/web instructions)

## 📖 Documentation Guides

### 📋 Quick Reference
| [**📋 Workflow Summary**](docs/WORKFLOW-SUMMARY.md) | **Complete quick reference guide** | **All processes, templates, and conventions in one place** |

### 📚 Detailed Guides
| Guide | Description | Key Features |
|-------|-------------|--------------|
| [🌿 Branches](docs/BRANCHES.md) | Branch naming and GitFlow strategy | MAIN/DEVELOP workflow, naming conventions |
| [📝 Commits](docs/COMMITS.md) | Commit message standards | Emoji conventions, English messaging |
| [📋 Issues](docs/ISSUES.md) | Issue lifecycle and templates | Complete template examples and usage |
| [🔀 Pull Requests](docs/PULL-REQUESTS.md) | PR process and guidelines | Review requirements, merge strategies |
| [🏷️ Change Types](docs/TYPES-CHANGES.md) | Semantic change classification | 13 change types with emoji indicators |
| [🏷️ Labels](docs/NEW-LABELS.md) | Repository labels and color scheme | Label definitions, colors, setup instructions |
| [🔢 Semantic Versioning](docs/SEMVER.md) | Version numbering standards | SemVer guidelines, release workflow |

## 🛠️ Template Features

### ✨ **Smart Design**
- **Consistent formatting** across all templates
- **Structured sections** for better organization  
- **Clear placeholders** with "nothing_to_say" defaults
- **Issue templates** avoid extra task checklists; the **PR template** carries the main review checklist

### 🏷️ **Automatic Organization**
- **Auto-labeling** for easy categorization
- **Default assignees** for faster triage
- **Related issue linking** for better tracking

### 📝 **User-Friendly**
- **Helpful comments** to guide users
- **Title Case guidelines** for consistency
- **Emoji conventions** for visual clarity

**Two permanent branches:**
- **MAIN** - Production-ready code
- **DEVELOP** - Integration branch for features

**Working branches**

- **Full:** `@developer/task-type-issue/short-name`
- **Simple:** `task-type/issue-short-name` (see [Branches](docs/BRANCHES.md))

Created from DEVELOP and deleted after merging.

## 📝 Commit Convention

**Full** profile uses emoji prefixes; **simple** profile uses plain Conventional Commits (`feat:`, `fix:`, …). See [Commits](docs/COMMITS.md).

```bash
# Full
git commit -m "✨ feat: add user authentication"

# Simple
git commit -m "feat: add user authentication"
```

## 🏷️ Change Types Reference

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
| 🔥 | `hotfix` | Urgent fixes—**usually production** (`main`); `develop` is possible—see [Branches](docs/BRANCHES.md) |

## 📊 Usage Examples

### Full profile

Use after copying [`full-github-templates/.github`](full-github-templates/.github) into your repo.

#### Creating a new feature

```bash
# 1. Create issue — 🛠️ Development Task
# Title: [TASK: FEAT] Add user dashboard

# 2. Create branch from develop
git checkout develop
git pull origin develop
git checkout -b @vinifen/feat/123/user-dashboard

# 3. Work and commit
git commit -m "✨ feat: add dashboard layout"

# 4. Create PR (body from pull_request_template.md)
# Title: ✨ feat: add user dashboard
# Link to issue #123
```

#### Reporting a bug

```bash
# 1. Create issue — 🐛 Bug Report
# Title: [BUG] Login form validation error

# 2. Create branch
git checkout develop
git pull origin develop
git checkout -b @vinifen/fix/124/login-validation

# 3. Fix and commit
git commit -m "🔧 fix: resolve login form validation"

# 4. Create PR
```

### Simple profile

Use after copying [`simple-github-templates/.github`](simple-github-templates/.github) into your repo.

#### Creating a new feature

```bash
# 1. Create issue — 🛠️ Development Task (minimal template body)
# Title: [TASK: FEAT] Add user dashboard

# 2. Create branch from develop
git checkout develop
git pull origin develop
git checkout -b feat/123/user-dashboard

# 3. Work and commit
git commit -m "feat: add dashboard layout"

# 4. Create PR (body from pull_request_template.md)
# Title: feat: add user dashboard
# Link to issue #123
```

#### Reporting a bug

```bash
# 1. Create issue — 🐛 Bug Report (minimal template body)
# Title: [BUG] Login form validation error

# 2. Create branch
git checkout develop
git pull origin develop
git checkout -b fix/124/login-validation

# 3. Fix and commit
git commit -m "fix: resolve login form validation"

# 4. Create PR
```

## 🤝 Contributing

We welcome contributions to improve these templates and workflows:

1. **Report issues** — Describe the problem clearly (install **`full-github-templates/.github`** or **`simple-github-templates/.github`** into a fork if you want GitHub templates locally).
2. **Suggest improvements** — Same as above; optional templates live under those bundles.
3. **Submit changes** — Open a PR; align the description with [`full-github-templates/.github/pull_request_template.md`](full-github-templates/.github/pull_request_template.md) when possible.
4. **Enhance docs** — Help improve documentation.

## 📈 Benefits

- **Consistency** across all projects
- **Faster onboarding** with clear guidelines
- **Better tracking** of work and progress
- **Professional** project management
- **Organized** issue and PR management
- **Clear history** with semantic commits
- **Quality control** with comprehensive checklists
- **Maintainable** codebase structure

## 🔗 Resources

- [GitHub Docs - Issue Templates](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitFlow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [Semantic Versioning](https://semver.org/)

## 📄 License

This project is licensed under the [MIT License](LICENSE) - feel free to use and adapt for your projects.

**Made with ❤️ for better development workflows**

[⭐ Star this repo](https://github.com/vinifen/gitflow-documentation) • [🐛 Report Bug](https://github.com/vinifen/gitflow-documentation/issues) • [💡 Request Feature](https://github.com/vinifen/gitflow-documentation/issues)

*Last updated: May 2026*
