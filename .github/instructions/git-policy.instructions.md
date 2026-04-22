---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "instruction"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
name: git-policy
applyTo: "**"
version: 1.0.0
---


# Git Policy

- Fuori da Agent-Git, Copilot non esegue `git push`, `git merge`, `git commit`, `git rebase`.
- Sono sempre consentiti i comandi read-only: `git status`, `git diff`, `git log`, `git show`, `git branch`.
- I commit proposti devono seguire Conventional Commits.
- Ogni push richiede conferma esplicita `PUSH`.
- Ogni merge richiede conferma esplicita `MERGE`.
