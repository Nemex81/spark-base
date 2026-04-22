---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Strategia di rollback dopo fallimenti post-commit o modifiche parziali non valide.
name: rollback-procedure
---


# rollback-procedure

- Commit non pushato: preferisci reset soft tramite Agent-Git.
- Commit gia pushato: preferisci revert tramite Agent-Git.
- Dopo rollback, riapri la checklist TODO della fase interessata.
