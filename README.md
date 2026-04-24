# spark-base

Layer fondazionale del SPARK Code Framework.

Questo repository contiene i componenti general-purpose condivisi tra i plugin SCF:

- 13 agenti installabili (`11` agenti base piu `spark-guide.agent` e `spark-assistant.agent`)
- 7 instruction trasversali comuni a qualsiasi progetto
- 29 skill condivise di framework, accessibilita, semver, changelog e governance
- 29 prompt utente piu `README.md` nella cartella `.github/prompts/`
- 4 file di configurazione comuni, incluso `.github/copilot-instructions.md`

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

Il manifest corrente del pacchetto e `package-manifest.json` schema `2.1`, versione `1.2.0`, con 83 file gestiti.

## Compatibilita

- `spark-framework-engine` >= 2.4.0
- VS Code con GitHub Copilot

## Maintainer

Nemex81
