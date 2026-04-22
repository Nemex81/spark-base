---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Regole per costruire messaggi commit coerenti con Conventional Commits.
name: conventional-commit
---


# conventional-commit

Formato: `tipo(scope): descrizione`.

Tipi consigliati:

- `feat`
- `fix`
- `docs`
- `refactor`
- `test`
- `chore`

Scope: usare componente o area principale toccata.
