# Git & GitHub Complete Guide

## Status
- **Overall Level**: 4/5
- **Theory**: 4/5
- **Practical**: 4/5
- **Troubleshooting**: 3/5
- **Design**: 3/5
- **Confidence**: High

## What I Have Learned
- **Version Control Concepts & Environment**:
  - Purpose of Version Control Systems (VCS), Distributed VCS architecture.
  - Installing Git on Windows, Linux, macOS.
  - Basic Terminal CLI navigation commands (`pwd`, `cd`, `ls`, `mkdir`).
  - Initializing local Git repository (`git init`).
  - Configuring user identity (`git config --global user.name`, `git config --global user.email`).
- **Core Git Workflow**:
  - The 3 Git States: Working Directory -> Staging Area (Index) -> Repository (HEAD).
  - Staging & Committing: `git add`, `git commit -m "msg"`.
  - Status & History: `git status`, `git diff`, `git log` (`git log --oneline --graph`).
  - Ignoring files: `.gitignore` setup for binaries, build outputs, environment configs.
- **Branching, Merging & History Manipulation**:
  - Branching: `git branch`, `git checkout -b <branch>`, `git switch <branch>`.
  - Merging: `git merge <branch>` (Fast-forward merge vs 3-way merge commit).
  - Rebasing: `git rebase <branch>` (re-basing feature commits on top of target branch).
  - Resolving Merge Conflicts: Identifying conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`), manual resolution, `git add`, `git commit`.
  - Branch Deletion: `git branch -d <branch>`, `git branch -D <branch>`.
  - Detached HEAD & Inspection: `git checkout <commit_hash>`.
  - Undoing Changes: `git reset` (`--soft`, `--mixed`, `--hard`), `git revert <commit_hash>` (creating undo commits).
- **Remote Repositories & Collaboration via GitHub**:
  - GitHub Account creation, setting up SSH keys / Personal Access Tokens.
  - Creating remote repositories on GitHub.
  - Remote commands: `git remote add origin <url>`, `git remote -v`.
  - Pushing & Pulling: `git push -u origin <branch>`, `git pull origin <branch>`, `git fetch`.
  - Cloning existing repositories: `git clone <url>`.
  - Forking repos & Syncing upstream updates.
  - GitHub Pull Requests (PR): Creating PRs, reviewing code changes, merging PRs.
  - GUI Tools: GitHub Desktop GUI app, VS Code Git & GitHub extension integration.

## What I Understand
- Internal Git Object Model (Blobs, Trees, Commits, Annotated Tags identified by SHA-1/SHA-256 hashes).
- How branches in Git are lightweight pointers to specific commit hashes.
- Difference between `git merge` (preserves linear history context with merge commits) and `git rebase` (re-writes commit history for a clean linear log).
- Difference between `git reset` (rewinds HEAD pointer, can lose uncommitted history if `--hard`) and `git revert` (creates a safe new commit that reverses past changes without rewriting history).
- How merge conflicts occur when two branches alter the exact same lines of code independently and how Git presents conflict blocks.
- Open-source collaboration workflow via Forking, Feature Branching, and Pull Requests on GitHub.

## What I Can Do
- Initialize, configure, and manage Git repositories via command-line interface (CLI).
- Create feature branches, perform merges, perform rebases, and resolve complex merge conflicts.
- Configure `.gitignore` to protect sensitive or generated files from version tracking.
- Manage remote repositories on GitHub: push, pull, fetch, clone, fork, create PRs.
- Safely navigate commit history using `git checkout`, `git reset`, and `git revert`.
- Utilize VS Code and GitHub Desktop GUI alongside CLI.

## What I Cannot Yet Do
- Use advanced Git tools: `git bisect` (binary search to locate bug-introducing commits), `git reflog` (recovering deleted commits/branches from reflog), `git submodule` / `git subtree` (managing multi-repository dependencies).
- Configure CI/CD pipelines on GitHub (GitHub Actions `.github/workflows/ci.yml`).
- Set up branch protection rules, code owners (`CODEOWNERS`), and automated PR checks on enterprise GitHub repositories.

## Sources & Knowledge Traceability

**Knowledge $\rightarrow$ Source Mapping**:
- **SRC-007** — Git và GitHub toàn tập (TITV) | URL: https://titv.vn/courses-page/git-va-github-toan-tap/ | Lessons 01-24 (Git CLI, Branching, Rebase, Conflicts, Reset/Revert, PRs)

Master Sources Catalog: [`00-sources/learning-sources.md`](../00-sources/learning-sources.md)

## Weaknesses
- Limited experience with GitHub Actions CI/CD workflows.
- No hands-on usage of `git bisect` or `git reflog` recovery in production incidents.

## Missing Knowledge
- **GitHub Actions**: CI/CD workflows, automated build & unit test triggers.
- **Git Power Tools**: `git reflog` (disaster recovery), `git bisect` (automated bug tracing), `git cherry-pick`.
- **Git Enterprise Security**: Signed commits (GPG keys), Branch protection rules.

## Recommended Supplement
1. Practice disaster recovery using `git reflog` to restore accidentally hard-reset commits.
2. Build a basic GitHub Actions CI workflow for Java Maven builds (`.github/workflows/maven.yml`).
