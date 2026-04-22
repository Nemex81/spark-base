---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Matrice sintetica dei comandi git consentiti, vietati e delegati ad Agent-Git.
name: git-execution
---


# git-execution

## Consentiti read-only

- `git status`
- `git diff`
- `git log`
- `git show`

## Consentiti solo via Agent-Git

- `git commit`
- `git push`
- `git merge`
- `git tag`

## Vietati in autonomia

- `git reset --hard`
- `git rebase`
- force push su branch condivisi
