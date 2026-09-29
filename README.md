# Spese mensili

App web installabile (PWA) per gestire le spese mensili. Gratuita, senza account, senza pubblicità e senza tracciamento.

- I dati restano **solo nel browser del tuo dispositivo**: non vengono mai inviati a nessun server.
- Funziona offline dopo il primo caricamento.
- Backup: dalla sezione "Copia di sicurezza" puoi esportare e importare le spese in un file `.json`.

## Pubblicazione su GitHub Pages
1. Crea un repository pubblico (es. `spese`) e carica **solo** i file di questa cartella: `index.html`, `manifest.webmanifest`, `sw.js`, `.nojekyll`, `README.md` e la cartella `icons/`.
2. Settings → Pages → "Deploy from a branch" → branch `main`, cartella `/ (root)` → Save.
3. Dopo circa un minuto l'app è su `https://TUONOME.github.io/spese/`.

Tutti i percorsi sono relativi: funziona con qualsiasi nome di repository.

## Aggiornare l'app
Modifica `VERSION` in `sw.js` (es. `"v2"`) e ricarica i file modificati. Gli utenti vedranno un avviso e potranno aggiornare senza perdere i dati.

## Privacy
Non caricare mai i tuoi file di backup (`spese-backup-*.json`) o CSV nel repository: contengono le tue spese.
