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

## [2026-05-19]

### Migrazione agenti multi-repo (spark-base 2.3.0 / spark-ops 1.4.0 / registry)

- Agent-Git e Agent-Welcome migrati da spark-base v2.2.0 a spark-ops v1.4.0.
- Agent-Release rimosso da spark-ops (errata classificazione): resta esclusivamente in spark-base.
- spark-assistant.agent.md e spark-guide.agent.md rimossi da spark-base (workspace agent nativi di spark-ops v1.3.0+).
- spark-base bumped: 2.2.0 → 2.3.0. spark-ops bumped: 1.3.0 → 1.4.0.
- Registry aggiornato: spark-base 2.3.0, spark-ops 1.4.0, spark-ops repo_url corretto verso spark-framework-engine.
- SHA spark-base: 6c0498f (main). SHA spark-ops/ENGINE: 20be743 (workspace-slim-registry-sync-20260511).

## [2026-04-24]

### MSI cleanup

- Rimossi i duplicati legacy `-MSI` e `-MSI-2` residui sotto `.github/` per consolidare i componenti canonici del framework e ridurre il debt di manutenzione senza cambiare il comportamento operativo.

### Framework unlock

- Framework unlock usato per riallineare i riferimenti documentali all'engine `spark-framework-engine >= 2.4.0` nei file protetti `copilot-instructions.md` e `AGENTS.md`, con ripristino del flag `framework_edit_mode: false` al termine del batch.

## [2026-04-17]

### Changed

- OWN-A: normalizzati i front matter SCF dei file markdown sotto .github/, aggiornato il manifest del pacchetto allo schema 2.1 con files_metadata e allineati gli asset protetti del framework.
