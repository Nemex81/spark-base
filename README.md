# spark-base

Layer fondazionale del SPARK Code Framework.

Questo repository contiene i componenti general-purpose condivisi tra i plugin SCF:

- 11 agenti base per orchestrazione, validazione, git, release, docs e ricerca
- instruction trasversali comuni a qualsiasi progetto
- skill condivise di framework, accessibilita, semver, changelog e governance
- prompt framework riutilizzabili nel workspace utente

## Installazione

Tramite il server MCP `spark-framework-engine`:

```python
scf_install_package("spark-base")
```

## Ruolo architetturale

`spark-base` non contiene logica language-specific e non contiene i componenti CORE-CRAFT.
I plugin superiori si appoggiano a questo layer:

- `scf-master-codecrafter` aggiunge design, code routing e context MCP
- `scf-pycode-crafter` aggiunge agenti, instruction e reference Python-specifici

## Compatibilita

- `spark-framework-engine` >= 1.9.0
- VS Code con GitHub Copilot

## Maintainer

Nemex81