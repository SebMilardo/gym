# GRIT — Piano di allenamento

GRIT è una piccola web app installabile per seguire un programma di allenamento di 24 settimane. Non richiede un account né un processo di build: è una pagina statica pubblicata su GitHub Pages.

**Apri l'app:** <https://sebmilardo.github.io/gym/>

## Funzionalità

- Tre sedute settimanali con esercizi, timer e progressione di corsa.
- Avviando **Avvia intervalli + GPS**, parte il timer a intervalli e la registrazione GPS della corsa.
- Durante la corsa mostra distanza, durata e un tracciato schematico.
- Salva i progressi nel browser e permette di esportare o importare un backup JSON.
- Dopo il primo caricamento online, il service worker rende disponibile la shell dell'app anche offline.

## Installazione su Android

1. Apri l'app in Chrome e scegli **⋮ → Installa app** oppure **Aggiungi a schermata Home**.
2. Per aggiornare l'app installata, collegati a Internet, chiudila completamente e riaprila. Se necessario, apri la stessa pagina in Chrome e ricaricala.

## GPS e dati

Concedi all'app il permesso di accedere alla posizione quando richiesto. Il GPS richiede un contesto sicuro, come HTTPS (GitHub Pages) o localhost. La traccia e gli altri progressi sono conservati nel browser e non vengono inviati a un server dall'app. I backup esportati includono i dati GPS: custodiscili come dati personali. Cancellare i dati del sito elimina anche i progressi salvati.

## Sviluppo e pubblicazione

Per provare l'app in locale, servi la cartella con un server statico, per esempio:

```sh
python3 -m http.server 8000
```

Poi apri <http://localhost:8000/>. Le modifiche pubblicate su `main` vengono distribuite su GitHub Pages dal workflow in `.github/workflows/pages.yml`.
