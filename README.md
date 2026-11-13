# Sito delle app (GitHub Pages)

Questa cartella diventa il repository `grogworks.github.io` e viene pubblicata su `https://grogworks.github.io/`.

## Struttura: una cartella per app

```
index.html            elenco di tutte le app + contatti
.nojekyll             pubblica i file così come sono (serve per le cartelle che iniziano con il punto)
recshelf/
  index.html          scheda dell'app
  privacy.html        informativa in inglese → URL da mettere in Play Console
  it/privacy.html     informativa in italiano
  fr/privacy.html     informativa in francese
  icon.svg
  config.json         tag Amazon e interruttore «Sostieni», letti dall'app (vedi sotto)
<prossima-app>/
  index.html
  privacy.html
```

URL privacy di RecShelf: `https://grogworks.github.io/recshelf/privacy.html`

## Nuova app
Per il codice Android riutilizzabile (pagina «Sostieni», lettura di config.json) vedi `~/AndroidStudioProjects/grogworks-kit/README.md`.

1. Copia la cartella `recshelf/` con il nome della nuova app (minuscolo, senza spazi).
2. Sostituisci testi, icona (`icon.svg`), link Play Store e informativa.
3. Aggiungi il riquadro in `index.html`.

## Informativa privacy
Il testo originale è nell'app: `RecShelf/app/src/main/assets/privacy.html` (italiano, francese, inglese).
Dopo ogni modifica, aggiorna qui le tre pagine (`privacy.html`, `it/privacy.html`, `fr/privacy.html`),
così app e sito dicono la stessa cosa.

## Tag Amazon e pagina «Sostieni» (`recshelf/config.json`)
L'app scarica questo file al massimo una volta al giorno. Per attivare l'affiliazione scrivi i tuoi tag:

```json
{
  "amazon": {
    "it": { "tag": "iltuotag-21" },
    "fr": { "tag": "iltuotagfr-21" }
  },
  "support": { "enabled": false }
}
```

- `support.enabled`: `true` mostra nel menu Altro la pagina «Sostieni RecShelf» (contributi con Google Play).
  Accendila solo dopo aver creato in Play Console i prodotti `support_small`, `support_medium`, `support_large`.

- `it` = programma Affiliazione Amazon.it, `fr` = Partenaires Amazon.fr (sono due iscrizioni separate).
- Il file è **pubblico**, come tutto il sito: va bene, perché i tag compaiono comunque in ogni link Amazon.
  Non mettere mai qui password o chiavi.
- L'app accetta solo lettere, numeri e trattini; un tag vuoto = link senza affiliazione.
- I telefoni vedono il cambio entro un giorno (e dopo aver aperto l'app).

## App con un dominio proprio (es. recshelf.app)
Serve solo per i link che aprono l'app (`recshelf.app/add`). Quel sito sta in un repository a parte
(`RecShelf/store/site/`), con il file `CNAME` che contiene il dominio. Questo sito resta com'è.
