---
spark: true
scf_owner: "spark-base"
scf_version: "1.2.0"
scf_file_role: "config"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
---

# Framework Changelog

## [2026-04-24]

### Framework unlock

- Framework unlock usato per riallineare i riferimenti documentali all'engine `spark-framework-engine >= 2.4.0` nei file protetti `copilot-instructions.md` e `AGENTS.md`, con ripristino del flag `framework_edit_mode: false` al termine del batch.

## [2026-04-17]

### Changed

- OWN-A: normalizzati i front matter SCF dei file markdown sotto .github/, aggiornato il manifest del pacchetto allo schema 2.1 con files_metadata e allineati gli asset protetti del framework.
