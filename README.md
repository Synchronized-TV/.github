# Synchronized — Best Practices & Security

This repository centralizes the **templates** and **security references** used across all repositories within **Synchronized-TV**.

## 🎯 Objectives
- Standardize Pull Requests and Issues  
- Integrate basic GitHub security controls into the development workflow  
- Simplify onboarding and repository maintenance  

## 🧩 Contents
| Type | Description |
|------|--------------|
| **Templates** | Pull Request, Issue, and Security Incident templates |
| **Security Policy** | How to report and handle vulnerabilities |

## 🛡️ Automated Security (Org-Level)

Organization-wide settings protect our repositories:
- **Branch Protection Rules** on `main` (and optionally `release/*`)
- **CodeQL** static analysis on Pull Requests (org configuration)
- **Dependabot** for dependency monitoring
- **Secret Scanning & Push Protection** for secret detection
- **Dependency Review** visible in PRs

> Note: If/when we add repo-specific automation, workflows will live under `.github/workflows/`.

## 🔗 Reference Files
- [Security Policy](./SECURITY.md)  
- [Pull Request Template](./PULL_REQUEST_TEMPLATE.md)  
- [Issue Templates](./ISSUE_TEMPLATE/)  
- [CODEOWNERS (fallback)](./CODEOWNERS)