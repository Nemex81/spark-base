---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Criteri per scegliere bump patch, minor o major in base all'impatto della modifica.
name: semver-bump
---


# semver-bump

- patch: fix e manutenzione.
- minor: nuove feature backward-compatible.
- major: breaking change o contratti pubblici incompatibili.
