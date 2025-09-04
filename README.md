# 📋 Gitflow Documentation

**Complete GitHub workflow templates and documentation for standardized development processes.**

## 🎯 Overview

This repository provides a comprehensive set of GitHub templates, workflow guidelines, and best practices to implement consistent development processes across all your projects. From issue tracking to pull request management, branch strategies to commit conventions - everything you need for a professional development workflow.

## ✨ What's Included

### 📝 **Issue Templates**
- **🛠️ Development Task** - For features, improvements, and fixes
- **🐛 Bug Report** - For problem reporting and tracking  
- **💡 Suggestion** - For ideas and enhancement proposals

### 🔖 **Pull Request Template**
- Standardized PR structure with comprehensive checklist
- Related issue linking and change categorization
- Time tracking and reviewer guidance

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

## 🛠️ Template Features

### ✨ **Smart Design**
- **Consistent formatting** across all templates
- **Structured sections** for better organization  
- **Clear placeholders** with "nothing_to_say" defaults
- **No task checkboxes** to avoid incomplete counters

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

**Working branches:**
- Format: `@developer/task-type-issue/short-name`
- Created from DEVELOP
- Deleted after merging

## 📝 Commit Convention

All commits use emoji prefixes for quick visual identification:

```bash
# Examples
git commit -m "✨ feat: add user authentication"
git commit -m "🔧 fix: resolve login validation bug"
git commit -m "📖 docs: update API documentation"
git commit -m "♻️ refactor: optimize database queries"
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
| 🔥 | `hotfix` | Urgent production fixes |

## 📊 Usage Examples

### Creating a New Feature
```bash
# 1. Create issue using 🛠️ Development Task template
# Title: [TASK: FEAT] Add user dashboard

# 2. Create branch from develop
git checkout develop
git pull origin develop
git checkout -b @vinifen/feat/123/user-dashboard

# 3. Work and commit
git commit -m "✨ feat: add dashboard layout"
git commit -m "✨ feat: implement user stats widget"

# 4. Create PR using template
# Title: ✨ feat: add user dashboard
# Link to issue #123
```

### Reporting a Bug
```bash
# 1. Create issue using 🐛 Bug Report template
# Title: [BUG] Login form validation error

# 2. Developer creates branch
git checkout -b @vinifen/fix/124/login-validation

# 3. Fix and commit
git commit -m "🔧 fix: resolve login form validation"

# 4. Create PR
# Title: 🔧 fix: resolve login form validation
```

## 🤝 Contributing

We welcome contributions to improve these templates and workflows:

1. **🐛 Report Issues** - Use the Bug Report template
2. **💡 Suggest Improvements** - Use the Suggestion template  
3. **🛠️ Submit Changes** - Create a PR with our template
4. **📖 Enhance Docs** - Help improve documentation

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

*Last updated: September 2025*
