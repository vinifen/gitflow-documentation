# 📋 GitHub Workflow Summary

**Complete quick reference guide for standardized GitHub development workflows, templates, and conventions.**

> 📚 **Source Repository**: [vinifen/gitflow-documentation](https://github.com/vinifen/gitflow-documentation)  
> 🔗 **Get Templates**: Copy templates and configs from the source repository to implement in your project.

## 🎯 Overview

This guide provides a comprehensive workflow system for GitHub projects, including:

- **3 Issue Templates** (Development Task, Bug Report, Suggestion)
- **1 Pull Request Template** with comprehensive checklist
- **Complete Documentation** for branches, commits, issues, PRs, and labels
- **Emoji-based** commit conventions and change types
- **Ready-to-use** GitHub templates and configurations

### 🚀 Implementation
1. **Copy templates** from [vinifen/gitflow-documentation](https://github.com/vinifen/gitflow-documentation)
2. **Adapt** templates to your project needs
3. **Follow** the conventions outlined in this guide
4. **Train** your team on the standardized processes

---

## 🌿 Branch Strategy

### Permanent Branches
- **MAIN** - Production-ready code
- **DEVELOP** - Integration branch for new features

### Working Branch Format
```
@developer/task-type-issue/short-name
```

### Examples
```bash
# From your project root:
git checkout -b @john/feat/123/user-dashboard
git checkout -b @jane/fix/124/login-validation
git checkout -b hotfix/125/critical-bug-v1.1
git checkout -b release/126/v1.2
```

> 💡 **Note**: Adapt the `@username` format to match your team's preferences. Some teams prefer initials or full names.

---

## 📝 Commit Convention

### Format
```
<emoji> <type>: <description>
```

### Rules
- Write in **English**
- Use **lowercase** for description
- Keep under **60 characters**
- Use **imperative mood** (add, fix)

### Examples
```bash
git commit -m "✨ feat: add user authentication"
git commit -m "🔧 fix: resolve login timeout"
git commit -m "📖 docs: update API documentation"
git commit -m "♻️ refactor: optimize database queries"
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
| 🔥 | `hotfix` | Urgent production fixes |

---

## 📋 Issue Templates

### 🛠️ Development Task
- **Format**: `[TASK: TYPE] Brief description`
- **Label**: `task`
- **Use for**: Features, improvements, fixes

### 🐛 Bug Report
- **Format**: `[BUG] Brief description of the problem`
- **Label**: `bug`
- **Use for**: Errors, unexpected behavior

### 💡 Suggestion
- **Format**: `[SUGGESTION] Brief description of the idea`
- **Label**: `suggestion`
- **Use for**: Ideas, enhancement proposals

---

## 🔀 Pull Request Guidelines

### Branch-Specific Rules
- **MAIN**: Normal merge (no squash/rebase)
- **DEVELOP**: Typically squashed
- **HOTFIX/RELEASE**: Include version in commit message

### Title Format
```
✨ feat: example for a feature pull request
```

### Required Sections
- Related Issue linking
- Summary of changes
- Type of change
- Time spent
- PR Checklist completion

---

## 🏷️ Labels & Colors

### Core Labels (Auto-applied)
- `task` - Development work (`#0052CC` - Blue)
- `bug` - Problem reports (`#D73A49` - Red)
- `suggestion` - Ideas (`#FFD700` - Yellow)

### Additional Labels (Manual)
- `documentation` - Docs (`#0075CA` - Blue)
- `test` - Testing (`#1D76DB` - Blue)
- `fix` - Bug fixes (`#D73A49` - Red)
- `hotfix` - Urgent fixes (`#FF0000` - Red)
- `infrastructure` - Infra (`#FF8C00` - Orange)
- `refactoring` - Code cleanup (`#FBCA04` - Yellow)

### Color Scheme
- **Red** - Critical issues (bugs, fixes, hotfixes)
- **Blue** - Development work (tasks, docs, tests)
- **Yellow/Orange** - Improvements (suggestions, refactoring, infrastructure)

---

## 🚀 Quick Workflow Examples

### Feature Development
```bash
# 1. Create issue: [TASK: FEAT] Add user dashboard
# 2. Create branch
git checkout develop
git checkout -b @vinifen/feat/123/user-dashboard

# 3. Work and commit
git commit -m "✨ feat: add dashboard layout"
git commit -m "✨ feat: implement user stats"

# 4. Create PR: ✨ feat: add user dashboard
# 5. Link to issue #123
```

### Bug Fix
```bash
# 1. Create issue: [BUG] Login validation error
# 2. Create branch
git checkout -b @vinifen/fix/124/login-validation

# 3. Fix and commit
git commit -m "🔧 fix: resolve login form validation"

# 4. Create PR: 🔧 fix: resolve login validation
```

### Hotfix
```bash
# 1. Create branch from main
git checkout main
git checkout -b hotfix/125/critical-security-v1.1

# 2. Fix and commit (include version)
git commit -m "🔥 hotfix: patch security vulnerability v1.1"
# or
git commit -m "🔧 fix: patch security vulnerability v1.1"

# 3. PR to main, then merge back to develop, RP will always have a hotfix type 🔥 in the title.
```

---

## 📖 Template Files & Setup

### 🗂️ Required Files Structure
```
.github/
├── ISSUE_TEMPLATE/
│   ├── 1_development_task.md
│   ├── 2_bug_report.md
│   ├── 3_suggestion.md
│   └── config.yml
└── PULL_REQUEST_TEMPLATE.md
```

### 📥 Getting Started
1. **Download templates** from [vinifen/gitflow-documentation](https://github.com/vinifen/gitflow-documentation)
2. **Copy `.github` folder** to your repository root
3. **Customize** assignees and labels in templates
4. **Update** config.yml with your project links
5. **Set up labels** using the provided CLI commands

### 🔧 Template Customization
- **Assignees**: Update `assignees: ["your-username"]` in template headers
- **Labels**: Modify or add custom labels in template metadata
- **Contact Links**: Update `config.yml` with project-specific help resources
- **Descriptions**: Adapt template descriptions to match your project context

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
- Fill all template sections completely
- Replace placeholders with real information
- Apply appropriate labels
- Link related issues/PRs

### Commits
- Use emoji + type format
- Write in English, lowercase description
- Keep under 60 characters
- Use imperative mood

### Pull Requests
- Link to related issue
- Fill complete PR template
- Apply matching labels
- Complete all checklist items
- Include time spent

### Branches
- Use correct naming format
- Create from appropriate base branch
- Delete after successful merge
- Include version for releases/hotfixes

### 🏷️ Setting Up Labels

**Using GitHub CLI** (recommended):
```bash
# Core issue labels
gh label create "task" --description "Work item or development task" --color "0052CC"
gh label create "suggestion" --description "Proposal or idea for improvement" --color "FFD700" 
gh label create "bug" --description "Problem or unexpected behavior" --color "D73A49"

# Additional labels
gh label create "documentation" --description "Documentation improvements" --color "0075CA"
gh label create "test" --description "Testing related changes" --color "1D76DB"
gh label create "fix" --description "Bug fixes and patches" --color "D73A49"
gh label create "hotfix" --description "Urgent production fixes" --color "FF0000"
gh label create "infrastructure" --description "Infrastructure tasks" --color "FF8C00"
gh label create "refactoring" --description "Code restructuring" --color "FBCA04"
```

**Using GitHub Web Interface**:
1. Go to your repository → **Issues** → **Labels**
2. Click **New label**
3. Add name, description, and color from the table above

---

## 🤝 Contributing & Support

### 📝 Improvements
Found an issue or have a suggestion for these workflows? 
- **Report issues**: [Create an issue](https://github.com/vinifen/gitflow-documentation/issues)
- **Suggest improvements**: [Submit suggestions](https://github.com/vinifen/gitflow-documentation/issues)
- **Contribute**: [Submit a pull request](https://github.com/vinifen/gitflow-documentation/pulls)

### 📞 Getting Help
- **Documentation**: Check the [full documentation](https://github.com/vinifen/gitflow-documentation)
- **Examples**: See real-world usage in the source repository

---

## 📄 License & Attribution

This workflow system is provided by [vinifen/gitflow-documentation](https://github.com/vinifen/gitflow-documentation) under the MIT License.

**When using these workflows:**
- ✅ **Free to use** and adapt for any project
- ✅ **No attribution required** but appreciated
- ✅ **Modify** templates and processes as needed
- ✅ **Share improvements** back to the community

---

*This summary consolidates all workflow documentation from [vinifen/gitflow-documentation](https://github.com/vinifen/gitflow-documentation). For the most up-to-date information and detailed documentation, visit the source repository.*
