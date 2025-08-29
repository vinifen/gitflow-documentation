## Branches

**Branches Rules:**
- There are two permanent branches: MAIN (production) and DEVELOP.
- All branches (except HOTFIX) must be created from DEVELOP or another related branch.
- DEVELOP must always be up to date with MAIN (production) and may stay ahead, since new features are developed there.

**Working branches (created from DEVELOP or a related branch):**
- Must include: developer’s @, task type, issue number (if applicable), and a short descriptive name.
- Format: ``@developer/task-type-issue/short-name``
- Should be deleted after merging when the developer is comfortable.

**RELEASE and HOTFIX branches:**
- Do not require the developer’s @.
- Must include: task type, issue number, branch name, and the version being released.
- Should be deleted after merging when the developer is comfortable.

**Workflow:**

![gitflow](https://github.com/vinifen/gitflow-documentation/blob/main/images/gitflow-branches.png)

**Examples:**

```branch
git checkout main
```

```branch
git checkout -b hotfix/1/fix-example-v1.1
```

```branch
git checkout -b release/1/v1.2
```

```branch
git checkout develop
```

```branch
git checkout -b @vinifen/feat/2/create-example
```

```branch
git checkout -b @vinifen/fix/3/fix-example
```


