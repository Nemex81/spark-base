---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Definisce i livelli di verbosita disponibili e quando applicarli.
name: verbosity
---


# verbosity

Livelli supportati:

- `standard`
- `collaborator`
- `nerd`

Il default e `standard`; aumentare solo quando il task lo richiede.
