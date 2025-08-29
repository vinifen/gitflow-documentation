## Issues

Issues are used to request a task and to report problems or bugs that may exist.

We have two types of issues, one to request tasks and another to report errors/bugs/any problem.

**Task Development Title Example:**

```task_development_title_example
[TASK: FEAT] Add new user functionality
``` 

**Task Development Template (1_development_task.md):**

```1_development_task.md
---
name: "🛠️ Development Task"
about: "Template for requesting a development task, feature, improvement, fix, etc."
title: "[TASK: TYPE] "
labels: ["task"]
assignees: ["dxf"]
---

# 🛠️ Issue_Title
<!-- Please keep the emoji and use Title Case for the issue title -->

### ✨ Description / Context:
<!-- Any details, context, or notes to help understand the work -->
- nothing_to_say

### 🛠 Type of task:
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

**Bug Title Example:**

``` bug_title_example
[BUG] Add new user functionality
``` 

**Bug Template (2_bug_report.md):**

```2_bug_report.md
---
name: "🐛 Bug Report"
about: "Template for reporting problems or bugs found"
title: "[bug] "
labels: ["bug"]
assignees: ["dxf"]
---

# 🐛 Issue_Title

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

**Suggestion Title:**

```suggestion_title:
[SUGGESTION] A suggestion example
```

**Suggestion Template:**

```3_suggestion.md
---
name: "💡 Suggestion"
about: "Template for sharing ideas or suggestions for improvement"
title: "[suggestion] "
labels: ["suggestion"]
assignees: []
---

# 💡 Issue_Title

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
**Config Template:**

```config.yml
blank_issues_enabled: false
contact_links:
  - name: 📚 Documentation
    url: https://github.com/vinifen/issue-test/wiki
    about: Check the documentation for help
```