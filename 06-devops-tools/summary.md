# Domain: DevOps & Version Control Tools — Summary

## Current Level Assessment
- **Version Control (Git & GitHub CLI)**: 4/5 (Theory: 4/5, Practical: 4/5, Troubleshooting: 3/5, Design: 3/5) — *Verified via CLI branching, rebasing, merge conflicts & PRs.*
- **CI/CD Automation (GitHub Actions)**: 0/5 (Theory: 1/5, Practical: 0/5, Troubleshooting: 0/5, Design: 0/5) — *Unverified / Tracked Gap.*
- **Containerization (Docker)**: 0/5 (Theory: 1/5, Practical: 0/5, Troubleshooting: 0/5, Design: 0/5) — *Unverified / Tracked Gap.*

> ⚠️ **Critical Distinction**: Mastering Git and GitHub version control CLI (`git rebase`, `git merge`, PRs) does **NOT** equal mastering CI/CD automation (`GitHub Actions`, `.github/workflows/`), Docker containerization, or Infrastructure as Code.

---

## DevOps Knowledge Model & Tracking Status

| DevOps Knowledge Pillar | Specific Technologies | Current Level | Status / Evidence |
| :--- | :--- | :---: | :--- |
| **1. Version Control System** | Git CLI, GitHub, Branching, Rebasing, PRs | **4/5** | Verified via Git CLI & GitHub PR workflow |
| **2. CI/CD Automation** | GitHub Actions (`.github/workflows/`), GitLab CI | **0/5** | Tracked Gap (GitHub Actions is CI/CD, not Git) |
| **3. Containerization** | Docker, Dockerfile, Docker Compose, Docker Networks | **0/5** | Tracked Gap (High Priority Roadmap Item) |
| **4. Infrastructure as Code (IaC)** | Terraform, Ansible | **0/5** | Future Tracked Knowledge |
| **5. Cloud Infrastructure** | AWS (VPC, EC2, S3, IAM), GCP | **0/5** | Future Tracked Knowledge |
| **6. Container Orchestration** | Kubernetes (K8s), Helm | **0/5** | Future Tracked Knowledge |
| **7. Observability & Monitoring** | Prometheus, Grafana, ELK Stack, OpenTelemetry | **0/5** | Future Tracked Knowledge |

---

## What I Have Learned

### Version Control (Git & GitHub Verified)
- Version Control principles, Git installation & configuration (`user.name`, `user.email`).
- 3 Git States (Working Directory, Staging Area, Repository).
- Staging (`git add`), committing (`git commit`), status (`git status`), history (`git log`, `git diff`).
- `.gitignore` configuration.
- Branching (`git branch`, `git switch`), Merging (`git merge`), Rebasing (`git rebase`).
- Merge conflict identification and manual resolution.
- Undoing changes: `git reset` (soft, mixed, hard), `git revert`.
- GitHub collaboration: `git remote`, `git push`, `git pull`, `git clone`, Forking, Pull Requests (PR).
- VS Code Git integration & GitHub Desktop GUI.

---

## Strong Areas
- Daily Git CLI operations for version control and repository management.
- Branching strategies, rebasing, and resolving merge conflicts.
- GitHub collaboration flow (cloning, pushing, pull requests, forking).

## Weak Areas
- GitHub Actions CI/CD automation.
- Git disaster recovery (`git reflog`, `git bisect`).
- Containerization & Infrastructure as Code tools (Docker, Kubernetes, Terraform).

## Missing Knowledge (Tracked Gaps)
- **CI/CD Automation**: GitHub Actions workflow syntax (`.github/workflows/ci.yml`), build triggers, secret management, Docker build-push actions.
- **Containerization**: Docker Engine, Dockerfile multi-stage builds, Docker volumes, Docker Compose (`docker-compose.yml`), Docker bridge networks.

## Recommended Supplements
1. **GitHub Actions CI/CD**: Build a GitHub Actions workflow to run Maven compile & test on every Pull Request.
2. **Docker Containerization**: Containerize Java backend apps and SQL database.

## Readiness for Next Topics
- **Git Version Control & PR Workflow**: **READY (4/5)**
- **DevOps CI/CD & Deployment Pipelines**: **PARTIALLY READY (2/5)**
  - Git & GitHub CLI: 4/5
  - CI/CD (GitHub Actions): 0/5
  - Docker Containerization: 0/5
  - *Action*: Learn GitHub Actions CI/CD and Docker containerization to complete core DevOps pipeline skills.
