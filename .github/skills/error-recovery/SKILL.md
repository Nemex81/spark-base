---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Fornisce una procedura sintetica per classificare e recuperare errori operativi comuni.
name: error-recovery
---


# error-recovery

1. Identifica se il problema e di ambiente, validazione o logica.
2. Riproduci con il set minimo di file e comandi.
3. Applica la correzione minima verificabile.
4. Aggiorna piano o TODO se il problema cambia il percorso implementativo.
