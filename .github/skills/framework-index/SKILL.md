---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Catalogo navigabile di agenti, skill, instruction e runtime MCP installati nel framework.
name: framework-index
---


# framework-index

- Parti da `.github/AGENTS.md`.
- Integra con `scf://agents-index` per i plugin attivi.
- Riporta master agents, plugin agents, skill e instruction in sezioni separate.
