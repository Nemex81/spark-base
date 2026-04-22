---
spark: true
scf_file_role: "config"
scf_version: "1.2.0"
scf_merge_strategy: "replace"
scf_protected: false
scf_owner: "spark-base"
scf_merge_priority: 10
---

# Changelog — spark-base

## [Unreleased]

### Added

- `spark-assistant.agent.md` e `spark-assistant-guide.instructions.md` entrano nel layer base cosi il bootstrap standalone installa entrambi gli agenti user-facing direttamente da `spark-base`.
- I prompt `scf-migrate-workspace` e `scf-update-policy` entrano nel pacchetto base per riflettere le capability ownership-aware e policy-aware del motore corrente.

### Fixed

- Normalizzato il frontmatter dei prompt general-purpose del pacchetto base (`type`, `name`, `description`) per compatibilita con il picker prompt di VS Code e con la validazione SCF.

## [1.2.0] - 2026-04-16

### Added

- Nuova suite di prompt `scf-*` per installazione, rimozione, stato, aggiornamenti e ispezione dei pacchetti SCF dal picker prompt di VS Code.
- Prompt `scf-pre-implementation-audit` per audit read-only dei piani di hardening e delle modifiche ecosistema prima dell'implementazione.

## [1.1.0] - 2026-04-15

### Added

- `spark-guide.agent.md` entra nel layer base come agente user-facing condiviso tra bootstrap iniziale e stack pacchetti.

### Changed

- Il pacchetto richiede `spark-framework-engine >= 2.1.0` per adottare in sicurezza `spark-guide` quando il file era gia' stato bootstrap-pato dal motore.

## [1.0.0] - 2026-04-15

### Added

- Prima release del layer fondazionale SCF.
- 11 agenti base per orchestrazione, validazione, git, release, docs e ricerca.
- Instruction, skill condivise e prompt framework migrati da `scf-master-codecrafter`.

### Notes

- Richiede `spark-framework-engine >= 1.9.0`.