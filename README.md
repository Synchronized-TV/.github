# Synchronized -- Shared Workflows, Templates & Security

This repository centralizes the **shared workflows**, **templates**, and **security references** used across all repositories within **Synchronized-TV**.

---

## Objectives

- Standardize Pull Requests, Issues, and CI/CD workflows
- Integrate essential GitHub security controls into the development process
- Simplify onboarding, maintenance, and release automation

---

## Contents

| Type                   | Description                                           |
| ---------------------- | ----------------------------------------------------- |
| **Workflows**          | Reusable CI/CD pipelines                              |
| **Templates**          | Pull Request and Issue templates                      |
| **Security Policy**    | Guidelines for reporting and managing vulnerabilities |
| **Contributing Guide** | Organization-wide contribution rules and conventions  |

---

## Reusable Workflows

For **security and reproducibility**, always reference reusable workflows using a **commit SHA**, not a branch (`@main`) or tag (`@v1`).

### `bump-version-pr.yml`

Creates a Pull Request that bumps the version (`patch`, `minor`, or `major`) without publishing.

### `npm-release.yml`

On merge to `main`, tags the release and publishes the package to npm.

#### Example usage

Workflow usage examples are maintained internally (private repository).

---

## Contributing

Organization-wide contribution guidelines are defined in [`CONTRIBUTING.md`](./CONTRIBUTING.md).

All repositories follow the same rules for:

- **Branch naming** (`feat/`, `fix/`, `chore/`, `release/`, etc.)
- **Commit conventions** (using [Conventional Commits](https://www.conventionalcommits.org/))
- **Pull request reviews** and **security policies**

> Note: See the contributing guide for naming rules, PR best practices, and security standards.

---

## Automated Security (Organization Level)

The following protections apply to all repositories within **Synchronized-TV**:

- **Branch protection rules** on `main` (and optionally `release/*`)
- **CodeQL** static analysis on Pull Requests
- **Dependabot** for dependency monitoring
- **Secret Scanning & Push Protection** to prevent credential leaks
- **Dependency Review** visible in PRs before merge

---

## Compliance & Operations

Synchronized's engineering practices are aligned with the Trusted Partner Network (TPN) / MPA Content Security Best Practices at a principles level.

Operational procedures and audit evidence are maintained in a private repository.

---

## Reference Files

| File                                                | Purpose                                      |
| --------------------------------------------------- | -------------------------------------------- |
| [Security Policy](./SECURITY.md)                    | How to report and handle vulnerabilities     |
| [Contributing Guide](./CONTRIBUTING.md)             | Organization-wide contribution standards     |
| [Pull Request Template](./PULL_REQUEST_TEMPLATE.md) | Standard PR format for all repositories      |
| [Issue Templates](./.github/ISSUE_TEMPLATE/)        | Default issue templates (bug, feature, etc.) |
| [Reusable Workflows](./.github/workflows/)          | Shared release and publish workflows         |
| [CODEOWNERS (fallback)](./CODEOWNERS)               | Default ownership and review rules           |

---

## About this Repository

This `.github` repository acts as the **shared governance and automation hub** for all projects under the Synchronized-TV organization.  
It ensures every repository benefits from the same CI/CD, security, and contribution standards.
