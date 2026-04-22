---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Impone conferma esplicita e elenco impatti prima di eliminare file o directory.
name: file-deletion-guard
---


# file-deletion-guard

- Non eliminare file senza conferma utente esplicita.
- Elenca sempre i path coinvolti e il motivo.
- Se il file appartiene al framework, verifica anche il perimetro `framework-guard`.
