# 🔀 Pull Requests

Guidelines:

- **RELEASE** pull requests that publish or tag a version should mention that version where your team expects it (commit message, tag, or release notes).
- **HOTFIX** pull requests are **most often** aimed at **production** (`main`); they do **not** strictly require a version in every commit. Use a version when you ship to production or cut a release; hotfixes that only target **develop** can defer versioning until later.
- Pull requests to the MAIN branch should use a normal merge (no squash or rebase).
- Pull requests into the DEVELOP branch are typically squashed.

### Adoption profiles

Install **one** template bundle into your project (see [Workflow summary](WORKFLOW-SUMMARY.md)). Each bundle ships **`pull_request_template.md`** at `.github/pull_request_template.md`, which GitHub loads automatically when opening a PR.

### ✏️ Title examples

**Full**

```pr_title_example
✨ feat: example for a feature pull request
```

**Simple**

```pr_title_example
feat: example for a feature pull request
```

### 🧩 Template: full (`full-github-templates/.github/pull_request_template.md`)

```pull_request_template.md
# 📋 Pull request title
<!-- Emoji at the start of the title is optional; it is still helpful when your team uses change-type emojis (e.g. ✨ feat, 🔧 fix). Use Title Case or sentence case for the title text. -->

### Related Issue: #ISSUE_NUMBER
<!-- Use "Related Issue: N/A" if no issue -->

## 🔄 Change Overview

### ✨ Summary of changes:
<!-- Briefly describe what was done and why, preferably in bullet points -->
- nothing_to_say

### 🏷️ Type of change:
<!-- Select one or two that apply -->
- **TYPE**

### ⏳ Time spent:
- **X HOURS** (approximate)

### 📝 Additional notes:
<!-- Any extra context, screenshots, or information for the reviewer -->
- N/A

## ✅ PR Checklist
- [ ] No sensitive information (passwords, API keys, secrets) exposed
- [ ] All tests run and pass successfully (unit, e2e, lint, etc.)
- [ ] Code compiles and runs without errors
- [ ] Tests and documentation updated or added if applicable
- [ ] Removed unnecessary comments, debug statements and dev artifacts
- [ ] Related issues, labels, and PR links established; PR title OK
```

### 🧩 Template: simple (`simple-github-templates/.github/pull_request_template.md`)

```pull_request_template.md
## Summary

-

## Related Issue: #ISSUE_NUMBER

<!-- Use "Related Issue: N/A" if there is no linked issue. -->

<!--
Optional — uncomment if your team tracks time on PRs:

## Time spent
**X HOURS** (approximate)
-->
```
