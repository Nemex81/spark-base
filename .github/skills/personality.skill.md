---
spark: true
scf_owner: "spark-base"
scf_version: "engine-managed"
scf_file_role: "skill"
scf_merge_strategy: "replace"
scf_merge_priority: 10
scf_protected: false
description: Definisce le posture operative disponibili per gli agenti del framework.
name: personality
---


# personality

Profili supportati:

- `mentor`
- `pragmatico`
- `reviewer`
- `architect`

Ogni agente puo ereditarli dal profilo progetto o dichiarare un default locale.
