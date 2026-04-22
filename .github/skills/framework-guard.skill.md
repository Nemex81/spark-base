---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Definisce il blocco standard per modifiche ai componenti del framework SCF.
name: framework-guard
---


# framework-guard

- Verifica se il task e framework-scope o application-scope.
- Se tocchi `.github/**`, dichiara esplicitamente il perimetro.
- Non mischiare nello stesso changeset framework e codice applicativo se evitabile.
