# 🏷️ Repository Labels

## 📋 Issue Labels

These labels are automatically applied when using issue templates:

| Label | Description | Color | Template |
|-------|-------------|-------|----------|
| `task` | Work item or development task to be completed | `#0052CC` | 🛠️ Development Task |
| `suggestion` | Proposal or idea for improvement or change | `#FFD700` | 💡 Suggestion |
| `bug-report` | Report of a problem, error, or unexpected behavior | `#D73A49` | 🐛 Bug Report |

## 🔧 Additional Labels

These labels can be applied manually for better categorization:

| Label | Description | Color | Usage |
|-------|-------------|-------|-------|
| `documentation` | Improvements or additions to documentation | `#0075CA` | PR/Issue |
| `test` | Changes related to testing (adding, updating, fixing tests) | `#1D76DB` | PR/Issue |
| `fix` | Bug fixes and patches for existing code | `#D73A49` | PR/Issue |
| `hotfix` | Urgent fixes applied directly to production | `#FF0000` | PR/Issue |
| `infrastructure` | Infrastructure and environment configuration tasks | `#FF8C00` | PR/Issue |
| `refactoring` | Code restructuring without changing functionality | `#FBCA04` | PR/Issue |

## 🎨 Color Scheme

- **Red (`#D73A49`)** - Critical issues (bug, fix, hotfix)
- **Blue (`#0052CC`, `#0075CA`, `#1D76DB`)** - Development work (task, docs, test)
- **Yellow/Orange (`#FFD700`, `#FBCA04`, `#FF8C00`)** - Improvements (suggestion, refactoring, infrastructure)

## 🛠️ Setup Instructions

### Creating Labels via GitHub CLI:

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

### Creating Labels via GitHub Web:

1. Go to your repository
2. Click on **Issues** tab
3. Click on **Labels** 
4. Click **New label**
5. Add name, description, and color from the table above

## 📊 Label Usage Guidelines

### For Issues:
- Always use **one primary label** (task, suggestion, bug)
- Add **secondary labels** as needed (documentation, help-wanted)
- Apply **priority labels** if your project uses them

### For Pull Requests:
- Use labels that match the **type of change**
- Link to related issues with matching labels
- Add **review labels** if your workflow requires them

### Best Practices:
- **Be consistent** - Use the same labels across similar issues
- **Keep it simple** - Don't over-label issues
- **Update regularly** - Remove outdated labels as issues evolve
