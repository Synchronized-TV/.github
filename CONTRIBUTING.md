# 🤝 Contributing to Synchronized-TV

This guide defines how to contribute safely and consistently across all projects.

---

## 🧭 Scope

These guidelines apply to **all repositories** under the **Synchronized-TV** organization.  
They cover documentation, code, workflows, and shared configurations.

---

## 🧱 Contribution Types

| Type | Example | Commit prefix |
|------|----------|----------------|
| 🧾 **Docs** | Update `README.md`, `SECURITY.md`, `docs/*.md` | `docs(...)` |
| ⚙️ **Workflows** | Edit `.github/workflows/*.yml` | `chore(workflow):` |
| 🔧 **Code / Config** | Improve features or refactor | `feat(...)`, `fix(...)`, `refactor(...)` |
| 🧩 **Design System / Packages** | Update shared libraries or npm modules | `chore(release):`, `fix:`, `feat:` |

---

## 🌿 Branch Naming Convention

Use clear, lowercase, hyphen-separated names.  
Prefixes indicate the type of work being done:

| Prefix | Example | Purpose |
|---------|----------|----------|
| `feat/` | `feat/video-editor-annotations` | New feature |
| `fix/` | `fix/api-refresh-token` | Bug fix |
| `chore/` | `chore/update-dependencies` | Maintenance, CI, dependencies |
| `docs/` | `docs/contributing-update` | Documentation only |
| `refactor/` | `refactor/player-context` | Code refactor without behavior change |
| `release/` | `release/1.2.0` | Release preparation branch |
| `hotfix/` | `hotfix/1.2.1` | Urgent production fix |

### ✅ Rules
- Use **lowercase** and **hyphens**, never underscores or camelCase.  
- Keep names **short and descriptive**.  
- Avoid including your name or initials — the branch history identifies authors.  
- Delete feature branches after merge to keep the repository clean.

---

## 💬 Pull Requests

- Always work in a feature branch.  
- Keep PRs **atomic** — one clear purpose per PR.  
- Provide a meaningful **title and description** in English.  
- Request review from at least one teammate before merging.  
- **Do not commit directly to `main`** on protected repositories.

> 💡 For workflow or release changes, open PRs in the relevant repo and wait for approval before merging.

---

## 🧩 Commit Conventions

Follow the **[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)** standard.

Examples:
```bash
docs(readme): clarify publish process
feat(video-editor): add frame preview on hover
chore(workflow): add reusable bump-version action
fix(api): handle 401 refresh token edge case
```

---

## 🛡️ Security

- Never commit secrets, tokens, or credentials.  
- If you find a security issue, **do not open a public issue** — contact  
  **security@synchronized.tv** or report via **Slack `#alert-security`**.  
- All repositories have **Dependabot**, **CodeQL**, and **Secret Scanning** enabled.

---

## 🧾 License

All repositories are private to **Synchronized-TV** unless stated otherwise.  
Do not distribute code, documentation, or assets outside the organization.
