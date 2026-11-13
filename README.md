# Sito delle app (GitHub Pages)

Questa cartella diventa il repository `grogworks.github.io` e viene pubblicata su `https://grogworks.github.io/`.

## Struttura: una cartella per app

```
index.html            elenco di tutte le app + contatti
.nojekyll             pubblica i file così come sono (serve per le cartelle che iniziano con il punto)
recshelf/
  index.html          scheda dell'app
  privacy.html        informativa → URL da mettere in Play Console
  icon.svg
<prossima-app>/
  index.html
  privacy.html
```

URL privacy di RecShelf: `https://grogworks.github.io/recshelf/privacy.html`

## Nuova app
1. Copia la cartella `recshelf/` con il nome della nuova app (minuscolo, senza spazi).
2. Sostituisci testi, icona (`icon.svg`), link Play Store e informativa.
3. Aggiungi il riquadro in `index.html`.

## Informativa privacy
Il testo originale è nell'app: `RecShelf/app/src/main/assets/privacy.html`.
Dopo ogni modifica, ricopialo qui in `recshelf/privacy.html`, così app e sito dicono la stessa cosa.

## App con un dominio proprio (es. recshelf.app)
Serve solo per i link che aprono l'app (`recshelf.app/add`). Quel sito sta in un repository a parte
(`RecShelf/store/site/`), con il file `CNAME` che contiene il dominio. Questo sito resta com'è.
