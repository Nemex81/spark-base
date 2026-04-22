---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Definisce gate minimi di completezza semantica per findings, design, plan e validation report.
name: semantic-gate
---


# semantic-gate

Un deliverable passa il gate solo se contiene:

- obiettivo;
- input/contesto;
- esito verificabile;
- rischi o limiti residui.
