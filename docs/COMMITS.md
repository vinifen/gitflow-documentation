## 📝 Commit Guidelines

### Assistive and AI tooling

- **Author identity:** Commits must use the **human contributor’s** Git author (`user.name`, `user.email`)—the person responsible for the change—not a model, product, or generic “AI” identity unless your organization explicitly requires otherwise.
- **Message content:** Do not stamp commit messages with assistant or model names, marketing sign-offs, or placeholders that replace the developer’s voice. Follow the project’s **full** or **simple** message format like any other team member.
- **Trailers:** Avoid `Co-authored-by:` or similar lines that credit a tool instead of a person; use them only when a real co-author exists and your team agrees.

Commits must stay consistent within a project: choose **full** or **simple** and stick to it.

### Full profile (emoji + type)

```
<emoji> <type>: <description>
```

### Simple profile (Conventional Commits, no emoji)

```
<type>: <description>
```

Supported `<type>` values match [Change types](TYPES-CHANGES.md) (for example `feat`, `fix`, `docs`, `chore`).

### 📏 Rules (both profiles)
- Always write in **English**
- Use **lowercase** for description
- Keep description **under 60 characters**
- Use **imperative mood** (add, fix, not added, fixed)

### ✨ Examples

**Full**

```bash
git commit -m "✨ feat: add user login"
git commit -m "🔧 fix: resolve api timeout"
git commit -m "📖 docs: update readme"
git commit -m "♻️ refactor: simplify auth logic"
```

**Simple**

```bash
git commit -m "feat: add user login"
git commit -m "fix: resolve api timeout"
git commit -m "docs: update readme"
git commit -m "refactor: simplify auth logic"
```
