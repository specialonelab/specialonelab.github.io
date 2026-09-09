# specialonelab.github.io

Sito statico (una pagina, bilingue IT/EN) per la vetrina personale di Andrea Saturnino.
Nessun build: è tutto in `index.html`.

## File
- `index.html` — il sito completo (HTML + CSS + JS inline)

## Pubblicare su GitHub Pages (senza usare git, dal browser)

1. **Account GitHub** su https://github.com/signup
   - Perché l'indirizzo sia esattamente `specialonelab.github.io`, l'**owner** del repo deve chiamarsi `specialonelab`. Due strade:
     - registri l'account con username `specialonelab`, **oppure**
     - hai già un account → crei un'**Organizzazione** gratuita chiamata `specialonelab`
       (in alto a destra: `+` → *New organization* → piano *Free*).
2. **Nuovo repository**: `+` → *New repository*
   - Owner: `specialonelab`
   - Repository name: **`specialonelab.github.io`** (esatto, tutto minuscolo)
   - Visibilità: *Public*
   - *Create repository*
3. **Carica il file**: nella pagina del repo vuoto → link *"uploading an existing file"*
   → trascina `index.html` → *Commit changes*
4. **Attiva Pages**: repo → *Settings* → *Pages*
   - Source: *Deploy from a branch* → Branch: `main` → cartella `/ (root)` → *Save*
   - (per i siti `*.github.io` spesso si attiva da solo)
5. Dopo 1–3 minuti il sito è online su **https://specialonelab.github.io**

## Aggiornare il sito in futuro
Repo → apri `index.html` → icona matita *(Edit)* → modifica → *Commit changes*.
Il sito si aggiorna da solo in un minuto.

## Contenuti
I testi vengono dalla "Presentazione Professionale IT & Privacy" (profilo consulenza IT & Privacy / DPO).
Sezioni: hero, "Chi sono e cosa faccio", "Tre ambiti di competenza" (3 card),
"Progetti su misura" + "Il mio metodo di lavoro", "Lavoriamo insieme" (email).
Email pubblica: `andrea.saturnino72@gmail.com`.

## Come modificare un testo
Ogni stringa esiste **due volte** e vanno cambiate entrambe:
1. nell'HTML visibile (elemento con attributo `data-i18n="chiave"`)
2. nell'oggetto JavaScript `I18N` a fondo pagina, sotto `it:` **e** `en:` per la stessa `chiave`

Lo switch IT/EN in alto a destra usa proprio l'oggetto `I18N`.

## Se un domani vuoi il dominio specialonelab.com
1. Compri il dominio da un registrar (~10–13 €/anno).
2. Aggiungi al repo un file `CNAME` contenente `specialonelab.com`.
3. Nel DNS del registrar: record A `@` → `185.199.108.153`, `.109.153`, `.110.153`, `.111.153`;
   record CNAME `www` → `specialonelab.github.io`.
4. Settings → Pages → *Custom domain* `specialonelab.com` → attendi il check → *Enforce HTTPS*.
