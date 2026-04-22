---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "instruction"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
name: model-policy
applyTo: "**"
version: 1.0.0
---


# Model Policy

- Leggi il contesto reale prima di modificare file.
- Non fare refactor non richiesti.
- Se esistono piu approcci validi, dichiara il trade-off principale.
- Le modifiche multi-file richiedono piano o checklist condivisa.
- Gli agenti dispatcher non implementano direttamente: instradano o fanno fallback.
