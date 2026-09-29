# Spese mensili

App web installabile (PWA) per gestire le spese mensili. Gratuita, senza account, senza pubblicità e senza tracciamento.

- I dati restano **solo nel browser del tuo dispositivo**: non vengono mai inviati a nessun server.
- Funziona offline dopo il primo caricamento.
- Pulsante «+» che apre un foglio di inserimento (importo grande, categorie a tocco, «Oggi/Ieri», suggerimenti per le descrizioni) e confronto con il mese scorso.
- Inserimento rapido: l'ultima categoria usata resta selezionata e ogni spesa si può duplicare (con la data di oggi).
- Budget mensile: un importo unico valido per ogni mese, con residuo e avviso di superamento.
- Riquadro «Il tuo ritmo»: spese effettive, impegni futuri non ancora pagati, disponibilità dopo gli impegni e media giornaliera sicura per i giorni rimasti nel mese corrente.
- Spese previste mensili: descrizione, importo, categoria e giorno di scadenza; puoi sospenderle, modificarle, eliminarle o segnarle pagate. La data dei mesi più corti viene adattata all'ultimo giorno del mese. Le previsioni non diventano spese effettive fino alla registrazione del pagamento.
- Backup: esporta e importa spese, budget e spese previste in un file `.json`. I vecchi backup sono ancora supportati; l'importazione aggiunge dati senza sovrascrivere quelli già presenti.
- Interfaccia rinnovata con colori caldi, contrasto elevato e supporto al tema scuro del dispositivo.
- Navigazione mobile a tre schede: «Riepilogo», «Movimenti» e «Previste». La selezione del mese resta condivisa; il pulsante «+» è disponibile da ogni scheda.
- CSV nella scheda «Movimenti»; importazione ed esportazione del backup nella sezione «Dati e backup» del riepilogo.

## Pubblicazione su GitHub Pages
1. Crea un repository pubblico (es. `spese`) e carica **solo** i file di questa cartella: `index.html`, `manifest.webmanifest`, `sw.js`, `.nojekyll`, `README.md` e la cartella `icons/`.
2. Settings → Pages → "Deploy from a branch" → branch `main`, cartella `/ (root)` → Save.
3. Dopo circa un minuto l'app è su `https://TUONOME.github.io/spese/`.

Tutti i percorsi sono relativi: funziona con qualsiasi nome di repository.

## Aggiornare l'app
Ricarica i file aggiornati nel repository. Il service worker usa la cache `v5`; per un aggiornamento successivo, incrementa `VERSION` in `sw.js`. Le spese effettive continuano a usare la chiave `spese-mensili-v1` e il loro formato esistente; budget e note di backup non vengono modificati. Le nuove spese previste e i relativi pagamenti sono salvati separatamente.

## Privacy
Non caricare mai i tuoi file di backup (`spese-backup-*.json`) o CSV nel repository: contengono le tue spese.
