# Assessment Instrument: P005 — Git Engineering Workflow + CI

## 📌 Project Overview
- **Project ID**: `P005`
- **Project Name**: Git Engineering Workflow + CI
- **Domain**: DevOps Tools & Build Automation
- **Status**: Planned
- **Evidence Status**: No Evidence
- **Repository**: TBD
- **Assessment Date**: Pending
- **Target Score**: Git Practical 4/5, GitHub Actions CI/CD Practical 3/5

---

## 🎯 1. Goal & Rationale
- **Goal**: Execute an end-to-end professional Git workflow demonstrating advanced version control operations (interactive rebase, merge conflict resolution, cherry-picking, PR review lifecycle) paired with an automated GitHub Actions CI/CD pipeline that compiles, tests, and verifies a Java Maven project on every commit.
- **Why this project exists**: While the repository reflects strong baseline Git familiarity ([`C007`](../00-sources/C007-git-github.md)), our gap analysis explicitly documents: *GitHub Actions CI/CD is currently at Level 0/5*. Furthermore, having a Git repository is not proof of software engineering rigor. This assessment evaluates disciplined Git engineering and automated CI/CD as two distinct, measurable capabilities.

---

## 📋 2. Prerequisites
- Git CLI Basics (Branch, Commit, Push, Pull) (Level 3/5)
- Maven Build Tool (`pom.xml`, `mvn test`) (Level 3/5)
- GitHub Account & SSH Key Setup (Level 3/5)

---

## 🔬 3. Skills Being Assessed

### A. Theory Assessed
- The Git Object Model: Commits, Trees, Blobs, Annotated Tags, and cryptographic SHA-1 hashes.
- Fast-forward vs 3-way recursive merge vs linear rebase history.
- The mechanics of Git HEAD, index (staging area), and working tree.
- CI/CD pipeline principles: Continuous Integration loop, automated feedback gates, build determinism, environment matrix testing.

### B. Practical Skills Assessed (Evaluated Separately)
1. **Git Version Control**:
   - Feature branching following trunk-based or GitHub flow.
   - Interactive rebase (`git rebase -i`) to squash messy commits and reword commit messages.
   - Intentionally creating and manually resolving a three-way merge conflict.
   - Selectively transferring commits across branches using `git cherry-pick`.
   - Undoing changes safely using `git revert` (preserving history) vs `git reset`.
   - Creating annotated Git tags (`git tag -a v1.0.0 -m "..."`) and GitHub Releases.
2. **GitHub Actions CI/CD Automation**:
   - Authoring `.github/workflows/ci.yml`.
   - Configuring event triggers (`on: [push, pull_request]`).
   - Using official actions (`actions/checkout`, `actions/setup-java`, `actions/cache`).
   - Running automated Maven builds and unit test suites on Ubuntu runners.
   - Enforcing PR protection rules: Pull requests cannot merge if CI tests fail.

### C. Troubleshooting Skills Assessed
- Diagnosing a broken Git history or detached HEAD state.
- Inspecting `git reflog` to recover an accidentally deleted branch or commit.
- Debugging a failing CI runner due to missing environment variables, Java version mismatches, or test assertions.

### D. Design Skills Assessed
- Designing an efficient, cached CI workflow that minimizes build latency.
- Designing a clear, readable Git commit history following Conventional Commits (`feat:`, `fix:`, `chore:`, `refactor:`).

---

## 🧪 4. Required Hands-on Experiments & Workflow Steps

All operations must be visible in the submitted GitHub repository commit graph and Actions tab:

### Workflow 1: The Merge Conflict Challenge
1. From `main`, create branch `feature/payment-v1` and modify line 15 of `PaymentService.java`. Commit.
2. Switch back to `main`, modify line 15 of `PaymentService.java` with conflicting logic. Commit to `main`.
3. Switch back to `feature/payment-v1` and execute `git rebase main` (or `git merge main`).
4. Inspect the Git conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
5. Manually edit the file to resolve the conflict correctly, stage the resolution with `git add`, and complete the rebase with `git rebase --continue`.
6. Provide screenshot or commit showing clean conflict resolution.

### Workflow 2: Interactive Rebase & Commit Hygiene
1. Create 3 small "wip" commits (e.g. "fix typo", "temp work", "add test").
2. Execute `git rebase -i HEAD~3`:
   - Squash the 3 commits into a single atomic commit.
   - Reword the final commit message following Conventional Commits format (e.g. `feat(payment): implement Stripe card tokenization`).
3. Prove that the history is clean and linear via `git log --oneline --graph`.

### Workflow 3: Safe Rollback with `git revert`
1. Push a commit introducing an intentional bug.
2. Revert the commit using `git revert <commit-sha>`.
3. Explain why `git revert` is the production standard for shared public branches instead of `git reset --hard`.

### Workflow 4: GitHub Actions CI Pipeline Implementation
Create `.github/workflows/ci.yml` with the following stages:
```yaml
name: Java CI Pipeline

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout Source Code
      uses: actions/checkout@v4

    - name: Set up JDK 17
      uses: actions/setup-java@v4
      with:
        java-version: '17'
        distribution: 'temurin'
        cache: 'maven'

    - name: Build with Maven
      run: mvn -B compile

    - name: Run Automated Tests
      run: mvn -B test
```
- **Validation**:
  - Push a passing commit: Show green checkmark in GitHub Actions.
  - Push a commit with a failing test assertion: Show red failure status blocking the PR.

---

## 🛑 5. Acceptance Criteria

| Capability | Minimum Acceptance Criteria | Advanced Criteria (Optional) |
| :--- | :--- | :--- |
| **Git Version Control** | Verified rebase conflict resolution, atomic commits, PR with branch merge. | `git cherry-pick` usage across branches; recovering dropped commit with `git reflog`. |
| **CI/CD Automation** | Functional GitHub Actions workflow compiling and running Maven tests on every push/PR. | Maven caching enabled (`~/.m2`); automated test report artifact publishing. |
| **Branch Protection** | PR requiring passing CI status before merging. | Multi-OS build matrix (Ubuntu + Windows runners). |

---

## 🚫 6. What This Project Does NOT Prove
- Does **NOT** prove Kubernetes Continuous Deployment (CD) / ArgoCD GitOps pipelines.
- Does **NOT** prove Docker image container registries (unless integrated with `P006`).
- Git mastery does **NOT** count towards CI/CD mastery (they receive separate matrix ratings).

---

## 📥 7. Project Submission Form

*Copy this block and fill it out when submitting your completed Git/CI project to AI for assessment:*

```markdown
Project ID: P005
Project Name: Git Engineering Workflow + CI
Repository URL: [Your GitHub Repo URL]
Commit SHA / Branch / PR: [Commit Hash]
Date: [YYYY-MM-DD]

### 1. Git Engineering Evidence
- Pull Request link:
- Merge conflict resolution commit:
- Interactive rebase commit log (`git log --oneline -n 5`):
- `git revert` commit hash:

### 2. GitHub Actions CI Evidence
- Workflow file path: `.github/workflows/ci.yml`
- Successful CI Run link:
- Deliberate failed test CI Run link (proving gatekeeping):
- Caching configured (Yes/No):

### 3. Self-Reflection
- What difference did you observe between `merge` and `rebase`?
- What was the most challenging part of resolving merge conflicts?
```
