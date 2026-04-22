---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Pattern per interrogare il framework SCF e descriverne struttura, agenti e tool runtime.
name: framework-query
---


# framework-query

- Per agenti: usa `scf://agents-index` o il relativo tool MCP.
- Per versioni: usa `scf_get_framework_version()`.
- Per runtime: usa `scf_get_runtime_state()` o `scf://runtime-state`.
- Mantieni le risposte orientate al task dell'utente, non a un dump completo.
