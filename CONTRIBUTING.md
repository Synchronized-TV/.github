# Contributing to Synchronized-TV

This guide defines how to contribute **safely, consistently, and efficiently** across all repositories within the **Synchronized-TV** organization.

It applies to all developers, contributors, and contractors working on code, documentation, workflows, and shared tooling.

---

# Scope

These contribution rules apply to every repository under the `Synchronized-TV` GitHub organization, including:

- Platform code
- Frontend & backend services
- Internal libraries and npm packages
- Documentation & configuration repositories
- GitHub Actions workflows

The goal is to ensure **quality**, **security**, and **traceability** across our SDLC.

---

# Contribution Types

| Type                   | Example                                        | Commit prefix                            |
| ---------------------- | ---------------------------------------------- | ---------------------------------------- |
| **Docs**              | Update `README.md`, `SECURITY.md`, `docs/*.md` | `docs(...)`                              |
| **Workflows**         | Update `.github/workflows/*.yml`               | `chore(workflow):`                       |
| **Code / Config**     | Features, fixes, refactors                     | `feat(...)`, `fix(...)`, `refactor(...)` |
| **Libraries / Packages** | Internal npm modules                        | `feat:`, `fix:`, `chore(release):`       |

We follow **Conventional Commits** for consistent history and automated releases.

---

# Branch Naming Convention

Branches must be **clear, lowercase, hyphen-separated**.

| Prefix      | Example                         | Purpose                          |
| ----------- | ------------------------------- | -------------------------------- |
| `feat/`     | `feat/video-editor-annotations` | New feature                      |
| `fix/`      | `fix/api-refresh-token`         | Bug fix                          |
| `chore/`    | `chore/update-dependencies`     | Maintenance & CI                 |
| `docs/`     | `docs/contributing-update`      | Documentation                    |
| `refactor/` | `refactor/player-context`       | Refactor without behavior change |
| `release/`  | `release/1.2.0`                 | Release preparation              |
| `hotfix/`   | `hotfix/1.2.1`                  | Critical production fix          |

**Rules:**

- Do not use camelCase or underscores.
- Keep names short and descriptive.
- Do not include personal names.
- Delete feature branches after merge.

---

# Pull Requests

All work must go through a **Pull Request**.

If your work relates to an Issue, reference it in the PR description using GitHub keywords (e.g., "Fixes #123") so the Issue auto-closes when the PR is merged.

### PR rules

- One purpose per PR (atomic).
- English title and description.
- CI must pass before review.
- At least **one approval** required before merging.
- No direct commits to `main` on protected repositories.
- Workflow/release changes must be reviewed by maintainers.

---

# Commit Conventions

We use **Conventional Commits**:  
https://www.conventionalcommits.org/en/v1.0.0/

When a commit references an Issue, append the Issue number at the end (e.g., `(#123)`) to keep history consistent with the PR's "Linked issue" section.

**Examples:**

```bash
docs(readme): clarify publish process (#45)
feat(editor): add frame preview on hover (#112)
chore(workflow): add bump-version composite action (#88)
fix(api): correct refresh token flow (#67)
refactor(auth): simplify token handling (#102)
```

---

# Security Requirements

Security is part of our SDLC.

### Mandatory rules

- Never commit credentials, tokens, certificates, or secrets.
- Never hardcode environment variables.
- Never log sensitive or client-related data.
- Do not upload client content or internal assets to public platforms.

### Protections

- GitHub **Secret Scanning**, **Dependabot**, **CodeQL**, and **Dependency Review** are enabled.
- Secrets must be stored in approved secret stores or GitHub encrypted secrets (CI only).
- New dependencies must be evaluated for security, size, and licensing.

### Reporting security issues

If you discover a vulnerability:

- Do NOT open a public issue  
- Email **security@synchronized.tv**  
- Follow the reporting instructions in [`SECURITY.md`](./SECURITY.md)

---

# SDLC & Code Quality Standards

All contributions must follow Synchronized's internal SDLC principles, including:

- Secure coding practices (OWASP Top 10 awareness)
- Clean, maintainable, and documented code
- Purposeful logging only
- No unused or unmaintained dependencies
- Proper error handling
- Tests updated when logic changes

---

# Dependencies

- Use existing libraries when possible.
- New dependencies must be justified and reviewed based on:
  - Security & maintenance
  - License compatibility
  - Bundle size / performance
  - Necessity

---

# Development Workflow (Simplified)

1. Create your feature branch
2. Implement changes
3. Run tests & linting
4. Open a PR
5. Request review
6. Apply feedback
7. Merge after approval

---

# License & Confidentiality

- Most Synchronized-TV repositories are **private by default** (some are public, like `Synchronized-TV/.github`).
- Do not share internal-only code, documentation, workflows, assets, or operational details outside approved channels.
