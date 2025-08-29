## 🔀 Pull Requests

HOTFIX and RELEASE pull requests must include the version that will be updated in the commit message.  
Pull requests to the MAIN branch must always be done as a normal pull request, without squash or rebase.
Pull request to DEVELOP branch generally should be squash.

### ✏️ Title Example

```pr_title_example
✨ feat: example for a feature pull request
```

### 🧩 Template

```PULL_REQUEST_TEMPLATE.md
# 🔖_Pull_Request_Title

### Related Issue: #ISSUE_NUMBER
<!-- Use: "Related Issue: N/A" if no issue -->

## 🔄 Change Overview

### ✨ Summary of changes:
<!-- Briefly describe what was done and why, preferably in bullet points -->
- nothing_to_say

### 🛠 Type of change:
<!-- Select one or two that apply -->
- **TYPE**

### ⏳ Time spent:
- **X HOURS** (approximate)

### 📝 Additional notes:
<!-- Any extra context, screenshots, or information for the reviewer -->
- N/A

### ✅ PR Checklist
- [ ] No sensitive information (passwords, API keys, secrets) exposed
- [ ] All tests run and pass successfully (unit, e2e, lint, etc.)
- [ ] Code compiles and runs without errors
- [ ] Tests and documentation updated or added if applicable
- [ ] Removed unnecessary comments, debug statements and dev artifacts
- [ ] Related issues, labels, and PR links established; PR title OK
```
