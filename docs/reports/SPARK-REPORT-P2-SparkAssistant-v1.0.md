# Report P2 — spark-assistant Plugin Manager narrative

## Metadata

- Data: 2026-05-08
- Branch: main (spark-base)
- Task: Aggiornamento narrativo spark-assistant.agent.md

## File modificati

| File | Tipo modifica | Righe aggiunte | Righe rimosse |
|------|--------------|----------------|---------------|
| `.github/agents/spark-assistant.agent.md` | update | 32 | 0 |

## Tool Plugin Manager rilevati nell'engine

**Famiglia Package (store-based, tracking manifest):**

| Tool | Descrizione breve |
|------|------------------|
| `scf_list_available_packages` | Lista pacchetti SCF disponibili nel registry remoto |
| `scf_get_package_info` | Descrizione, dipendenze e compatibilità di un pacchetto |
| `scf_list_installed_packages` | Lista pacchetti installati nel workspace corrente |
| `scf_plan_install` | Pianifica installazione: file scrivibili, preservati, conflitti |
| `scf_install_package` | Installa un pacchetto SCF nel store dell'engine (tracked) |
| `scf_remove_package` | Rimuove un pacchetto SCF installato |
| `scf_check_updates` | Rileva aggiornamenti disponibili per i pacchetti installati |
| `scf_update_package` | Aggiorna un singolo pacchetto preservando file modificati dall'utente |
| `scf_update_packages` | Aggiorna tutti i pacchetti installati in batch |
| `scf_apply_updates` | Applica aggiornamenti pianificati dopo conferma |

**Famiglia Plugin Dual-Mode (download diretto, no tracking engine):**

| Tool | Descrizione breve |
|------|------------------|
| `scf_list_plugins` | Lista plugin disponibili per download diretto (esclude mcp_only) |
| `scf_install_plugin` | Scarica plugin direttamente in `.github/` senza store e senza tracking |
| `scf_plugin_list` | Lista plugin installati + disponibili (store-based, via PluginManagerFacade) |
| `scf_plugin_install` | Installa plugin via store PluginManagerFacade |
| `scf_plugin_remove` | Rimuove plugin via store |
| `scf_plugin_update` | Aggiorna plugin via store |

## Gap rilevati in Fase 2

**Q1 — Tool MCP che coprono il dominio Plugin Manager:**
16 tool totali in due famiglie (Package store-based e Plugin Dual-Mode). Dettaglio nella tabella sopra.

**Q2 — spark-assistant.agent.md cita già qualcuno di questi tool?**
Sì: `scf_list_available_packages` (Flusso A, step 3), `scf_get_package_info` (Flusso B, step 1),
`scf_plan_install` (Flusso B, step 3), `scf_install_package` (Flusso B, step 4).
Nessun tool della famiglia Plugin Dual-Mode era citato.

**Q3 — `scf_install_package` e `scf_install_plugin` sono lo stesso tool?**
No, sono tool distinti con comportamento diverso:
- `scf_install_package`: store-based, registra nel manifest engine, supporta rollback e conflict resolution.
- `scf_install_plugin`: download diretto in `.github/`, nessun tracking engine, l'utente possiede i file.
Il Flusso B gestisce correttamente `scf_install_package`. La sezione nuova aggiunge il percorso
`scf_install_plugin` come alternativa per i plugin in modalità diretta.

**Q4 — C'è una sezione "auto-presentazione" nell'agente attuale?**
No. La sezione "Identita e perimetro" descrive il perimetro dell'agente ma non è una sequenza
operativa di risposta all'utente. La nuova sezione "Presentazione e primo orientamento" è stata
inserita come primo punto di ingresso narrativo, posizionata dopo "Identita e perimetro" e prima
del "Flusso A" per rispettare la gerarchia logica esistente.

**Q5 — spark-guide copre già il Plugin Manager?**
Parzialmente: spark-guide ha responsabilità di "Orientamento" (spiega cosa sono i pacchetti) e
"Routing operativo" (passa il task a spark-assistant). Non esegue operazioni Plugin Manager.
Il confine rispettato: spark-guide descrive e delega, spark-assistant esegue. La sezione nuova
usa esclusivamente verbi operativi e include rimando esplicito a spark-guide per descrizioni
architetturali, eliminando sovrapposizioni.

## Divergenze dalla spec del prompt

| Placeholder del prompt | Tool reale usato | Motivo |
|-----------------------|-----------------|--------|
| `scf_list_plugins` | `scf_list_plugins` | Tool esiste nell'engine (tools_plugins.py, Dual-Mode) |
| `scf_get_plugin_info` | `scf_get_package_info` | Tool `scf_get_plugin_info` non esiste. Il più vicino funzionalmente è `scf_get_package_info` (tools_packages_query.py), che accetta qualsiasi `package_id` |
| `scf_install_plugin` | `scf_install_plugin` | Tool esiste nell'engine (tools_plugins.py, Dual-Mode) |
| `scf_version: "1.5.0"` | `scf_version: "1.7.3"` | Il prompt suggeriva "1.5.0" ma `package-manifest.json` di spark-base è alla versione 1.7.3. Aggiornato alla versione corrente del pacchetto per coerenza con il versionamento reale. |

## Anomalie gestite

Nessuna anomalia rilevata. Tutti i file prerequisiti erano presenti e leggibili.
`scf_get_plugin_info` assente nell'engine: gestito come TYPE-I (tool non citato sostituito
con il più vicino funzionalmente, documentato qui).

## Checklist Fase 4

- [x] Frontmatter YAML valido (nessuna chiave duplicata, indentazione corretta, stringhe quotate)
- [x] Markdownlint: H1→H2 gerarchici corretti, nessuna riga blank multipla, nessuno spazio trailing
- [x] Nomi tool verificati contro engine (tutti i 6 tool citati nella nuova sezione esistono in `spark/boot/tools_*.py`)
- [x] Nessuna sovrapposizione con spark-guide (sezione nuova usa solo verbi operativi + rimando esplicito)
- [x] Tono coerente con regole operative (diretto, tecnico, orientato all'azione)
- [x] Sezione nuova posizionata prima del Flusso A
