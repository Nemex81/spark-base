---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "instruction"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
name: verbosity
applyTo: "**"
version: 1.0.0
---


# Verbosity

- Livello default: standard.
- Espandi solo quando il task e complesso o l'utente chiede dettaglio.
- Per codice e checklist: mai troncato.
- Per spiegazioni: breve, completa, senza ripetizioni.
