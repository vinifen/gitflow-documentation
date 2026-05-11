## 🌿 Branches

### Assistive and AI tooling

- **Branch ownership:** Working branches must use the **real developer’s** identifier (for example `@your-github-handle` in the **full** profile), not a placeholder, shared “bot”, or model name unless the repository policy says otherwise.
- **Consistency:** Automation or AI may suggest names, but the final branch must match **your** team’s convention and traceability (who is doing the work).

### Adoption profiles

This workflow supports two convention levels. **GitFlow stays the same** (permanent branches, feature/release/hotfix flow); only naming strictness changes.

| | **Full** | **Simple** |
|---|----------|------------|
| **Working branches** | `@developer/task-type-issue/short-name` — includes `@`, task type, issue number when applicable | `task-type/issue-short-name` or `task-type/short-name` (no `@` required; issue number recommended when you use issues) |
| **Release / hotfix** | Same rules for both profiles | Same rules for both profiles |
| **Commits / PR titles** | Emoji + type (see [Commits](COMMITS.md)) | Plain `type: description`, no emoji required |

Pick **simple** for small teams or internal tools; **full** when you want uniform traceability and richer metadata.

### 📏 Branch Rules
- There are two permanent branches: MAIN (production) and DEVELOP.
- Everyday feature and fix branches are usually created from **DEVELOP** (or another integration branch).
- **Hotfix** is **most commonly** used to patch **production**: teams usually branch from **main** and merge back so users get the fix quickly. That is **not** the only option—you may also create a `hotfix/…` branch from **develop** when the urgent fix should land in integration first or when your process does not require branching off production. Use whichever base matches your release path.
- DEVELOP must always be up to date with MAIN (production) and may stay ahead, since new features are developed there.

### 🔀 Working branches (created from DEVELOP or a related branch)

**Full profile**

- Must include: developer’s @, task type, issue number (if applicable), and a short descriptive name.
- Format: ``@developer/task-type-issue/short-name``
- Should be deleted after merging when the developer is comfortable.

**Simple profile**

- Must include: task type and a short descriptive name; issue number in the branch name when the work is tied to an issue.
- Examples: ``feat/123-add-login``, ``fix/oauth-timeout``, ``feat/user-dashboard``
- Should be deleted after merging when the developer is comfortable.

### 🚨 Release and Hotfix branches

**Hotfix** is **normally a production-oriented** branch (patch what users run); **release** prepares a versioned delivery. Neither rule is absolute—adapt if your pipeline differs.

- Do not require the developer’s @.
- Include **task type**, **issue number** (when you use issues), and a **short descriptive name**. Putting the **version** in the branch name or in the merge/release commit is **recommended** when you ship to production or tag a release, but it is **not strictly required**—for example a hotfix that only merges into **develop** may omit a version until a later release branch.
- Should be deleted after merging when the developer is comfortable.

### 🔁 Workflow

![gitflow](https://github.com/vinifen/gitflow-documentation/blob/main/docs/images/gitflow-branches.png)

### ✨ Examples

```branch
git checkout main
```

```branch
git checkout main
git checkout -b hotfix/1/fix-example-v1.1
```

```branch
git checkout develop
git checkout -b hotfix/2/fix-example
```

```branch
git checkout develop
git checkout -b release/1/v1.2
```

```branch
git checkout develop
```

**Full profile**

```branch
git checkout -b @dev/feat/2/create-example
```

```branch
git checkout -b @dev/fix/3/fix-example
```

```branch
git checkout -b @dev/chore/4/update-ci-cache
```

**Simple profile**

```branch
git checkout -b feat/2/create-example
```

```branch
git checkout -b fix/3/fix-example
```

```branch
git checkout -b chore/4/update-ci-cache
```
