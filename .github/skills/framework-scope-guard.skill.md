---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Protegge il layer master da richieste fuori scope o non coperte dai plugin installati.
name: framework-scope-guard
---


# framework-scope-guard

- Se il task richiede competenze non presenti, non improvvisare: instrada ad Agent-Research.
- Se il task chiede modifiche fuori perimetro framework, esplicitalo prima di procedere.
- Se un dispatcher non trova capability compatibili, ferma l'esecuzione automatica e segnala il fallback.
