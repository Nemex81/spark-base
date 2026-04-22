---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "instruction"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
name: framework-guard
applyTo: "**"
version: 1.0.0
---


# Framework Guard

- Proteggi i file framework sotto `.github/**` da modifiche accidentali.
- Se il task richiede scrittura su componenti protetti, verifica prima il perimetro richiesto.
- Le modifiche al framework devono restare separate dal codice applicativo.
- Non autorizzare sblocchi impliciti: i cambi di perimetro vanno dichiarati esplicitamente.
