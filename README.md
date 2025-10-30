# 🧭 Synchronized — Shared Workflows, Templates & Security

This repository centralizes the **shared workflows**, **templates**, and **security references** used across all repositories within **Synchronized-TV**.

---

## 🎯 Objectives

- Standardize Pull Requests, Issues, and CI/CD workflows  
- Integrate essential GitHub security controls into the development process  
- Simplify onboarding, maintenance, and release automation  

---

## 🧩 Contents

| Type | Description |
|------|--------------|
| **Workflows** | Reusable CI/CD pipelines for versioning and publishing |
| **Templates** | Pull Request, Issue, and Security Incident templates |
| **Security Policy** | Guidelines for reporting and managing vulnerabilities |

---

## ⚙️ Reusable Workflows

### 🔁 `bump-version-pr.yml`
Creates a Pull Request that bumps the version (`patch`, `minor`, or `major`) without publishing.

### 🚀 `publish-on-merge.yml`
On merge to `main`, tags the release and publishes the package to npm.

#### Example usage
To use a workflow from this repository in another project:

```yaml
name: release
on:
  workflow_dispatch:
    inputs:
      bump:
        description: "Version type"
        type: choice
        options: [patch, minor, major]
        default: patch

jobs:
  release:
    uses: Synchronized-TV/.github/.github/workflows/bump-version-pr.yml@main
    with:
      bump: ${{ inputs.bump }}
      node: "20"
    secrets: inherit
```
---


## 🛡️ Automated Security (Organization Level)

The following protections apply to all repositories within **Synchronized-TV**:

- **Branch protection rules** on `main` (and optionally `release/*`)  
- **CodeQL** static analysis on Pull Requests  
- **Dependabot** for dependency monitoring  
- **Secret Scanning & Push Protection** to prevent credential leaks  
- **Dependency Review** visible in PRs before merge  

> 🔒 For sensitive operational procedures (e.g., token rotation, internal audit logs), refer to the **private** repository [Synchronized-TV/.internal](https://github.com/Synchronized-TV/.internal).

---

## 🔗 Reference Files

| File | Purpose |
|------|----------|
| [Security Policy](./SECURITY.md) | How to report and handle vulnerabilities |
| [Pull Request Template](./PULL_REQUEST_TEMPLATE.md) | Standard PR format for all repositories |
| [Issue Templates](./ISSUE_TEMPLATE/) | Default issue templates (bug, feature, etc.) |
| [Reusable Workflows](./.github/workflows/) | Shared release and publish workflows |
| [CODEOWNERS (fallback)](./CODEOWNERS) | Default ownership and review rules |

---

## 🧭 About this Repository

This `.github` repository acts as the **shared governance and automation hub** for all projects under the Synchronized-TV organization.  
It ensures every repository benefits from the same CI/CD, security, and contribution standards.
