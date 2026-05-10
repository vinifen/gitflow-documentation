# 📝 Issue Management Guide

## 🎯 Overview

Issues are the primary way to track work, report problems, and suggest improvements in our projects. Templates live under **`full-github-templates/.github/`** or **`simple-github-templates/.github/`** — copy **one** bundle so your repo gets `.github/ISSUE_TEMPLATE/` plus `pull_request_template.md` (see [Workflow summary](WORKFLOW-SUMMARY.md)).

## 📋 Issue Types

Each bundle ships **three** issue templates with the **same filenames** (`1_development_task.md`, `2_bug_report.md`, `3_suggestion.md`). Choose the **full** or **simple** **root folder** when copying; you do not rename files. The simple bundle uses shorter bodies; full uses longer sections. With **simple**, blank issues are allowed (`blank_issues_enabled: true`); with **full**, they default to off unless you change `config.yml`.

| Type | File | Purpose | Label |
|------|------|---------|-------|
| 🛠️ **Development Task** | `1_development_task.md` | Features, improvements, fixes | `task` |
| 🐛 **Bug Report** | `2_bug_report.md` | Errors, unexpected behavior | `bug-report` |
| 💡 **Suggestion** | `3_suggestion.md` | Ideas, enhancements | `suggestion` |

## 🛠️ Development Task Template

Used for requesting any development work including features, improvements, and fixes.

### Title Format:
```
[TASK: TYPE] Brief description
```

**Examples:**
- `[TASK: FEAT] Add user authentication`
- `[TASK: FIX] Resolve login timeout`
- `[TASK: REFACTOR] Optimize database queries`

### Template Structure:

```1_development_task.md
---
name: "🛠️ Development Task"
about: "Template for requesting a development task, feature, improvement, fix, etc."
title: "[TASK: TYPE] "
labels: ["task"]
assignees: []
---

# 🛠️ Issue_Title
<!-- Please keep the emoji and use Title Case or Sentence case for the issue title -->

### ✨ Description / Context:
<!-- Any details, context, or notes to help understand the work -->
- nothing_to_say

### 🏷️ Type of task:
<!-- Select one or two that apply -->
- **TYPE**

### 🛠 Implementation / Steps:
<!-- Add steps, hints, or guidance if necessary -->
- nothing_to_say

### ⏳ Estimated Time:
- **X HOURS** (approximate)

### 📝 Additional Notes:
- N/A

### 🔗 Related:
<!-- List other issues or PRs that are dependencies of this task -->
- N/A
```

## 🐛 Bug Report Template

Used for reporting problems, errors, or unexpected behavior in the project.

### Title Format:
```
[BUG] Brief description of the problem
```

**Examples:**
- `[BUG] Login form validation error`
- `[BUG] Dashboard not loading on mobile`
- `[BUG] API timeout on large requests`

### Template Structure:

```2_bug_report.md
---
name: "🐛 Bug Report"
about: "Template for reporting problems or bugs found"
title: "[BUG] "
labels: ["bug-report"]
assignees: []
---

# 🐛 Issue_Title
<!-- Please keep the emoji and use Title Case or Sentence case for the issue title -->

### ✨ Description / Context:
<!-- A clear and concise description of what the bug is -->
- nothing_to_say

### 🛠 Steps to Reproduce:
<!-- Steps to reproduce the behavior -->
- nothing_to_say

### ✅ Expected Behavior:
<!-- A clear and concise description of what you expected to happen -->
- nothing_to_say

### ❌ Actual Behavior:
<!-- A clear and concise description of what actually happened -->
- nothing_to_say

### 🌍 Environment:
<!-- Please complete the following information -->
- **OS**: [e.g. Windows, macOS, Linux, or N/A if not applicable]
- **Browser**: [e.g. Chrome, Safari, Firefox, or N/A if not applicable]
- **Version**: [e.g. 22, or N/A if unknown]

### 📝 Additional Notes:
- N/A

### 🔗 Related:
<!-- List other issues or PRs that are dependencies of this task -->
- N/A
```

## 💡 Suggestion Template

Used for sharing ideas, proposals, and improvement suggestions.

### Title Format:
```
[SUGGESTION] Brief description of the idea
```

**Examples:**
- `[SUGGESTION] Add dark mode theme`
- `[SUGGESTION] Improve search functionality`
- `[SUGGESTION] Simplify user onboarding`

### Template Structure:

```3_suggestion.md
---
name: "💡 Suggestion"
about: "Template for sharing ideas or suggestions for improvement"
title: "[SUGGESTION] "
labels: ["suggestion"]
assignees: []
---

# 💡 Issue_Title
<!-- Please keep the emoji and use Title Case or Sentence case for the issue title -->

### ✨ Description / Context:
<!-- Any details, context, or notes to help understand the suggestion -->
- nothing_to_say

### 🎯 Why is this useful:
<!-- Explain why this would be helpful or beneficial -->
- nothing_to_say

### 📝 Additional Notes:
- N/A

### 🔗 Related:
<!-- List other issues or PRs that are dependencies of this task -->
- N/A
```

### Simple bundle (same filenames)

In **`simple-github-templates/.github/ISSUE_TEMPLATE/`**, `1_development_task.md`, `2_bug_report.md`, and `3_suggestion.md` mirror the full bundle names but keep **minimal** sections (for example “Description” / “What happened” / “Idea”). Labels stay `task`, `bug-report`, and `suggestion`.

## ⚙️ Configuration

Each bundle includes **`ISSUE_TEMPLATE/config.yml`**.

- **simple** — `blank_issues_enabled: true` (optional blank issues).
- **full** — `blank_issues_enabled: false` (templates encouraged).

### Config example (simple bundle default):

```config.yml
blank_issues_enabled: true
contact_links:
  - name: Documentation
    url: https://github.com/your-repo/wiki
    about: Check the documentation for help
```

## 📋 Best Practices

### ✅ Creating Good Issues

**Title Guidelines:**
- Use the correct format: `[TYPE] Description`
- Be specific and descriptive
- Use Title Case formatting
- Keep under 80 characters

**Content Guidelines:**
- Fill out all relevant template sections
- Replace "nothing_to_say" with actual information
- Be clear and concise in descriptions
- Include examples when helpful

### 🏷️ Labeling

**Automatic Labels:**
- Templates automatically apply appropriate labels
- `task` for `1_development_task.md`
- `bug-report` for `2_bug_report.md`
- `suggestion` for `3_suggestion.md`

**Additional Labels:**
- Add secondary labels as needed (documentation, test, etc.)
- Use priority labels if your project has them
- Keep labeling consistent across issues
