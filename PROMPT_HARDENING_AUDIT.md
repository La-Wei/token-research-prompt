# Prompt Hardening Audit

## Scope
Audit post-intervento sui file:
- `prompt/token-research-prompt.md`
- `prompt/token-trade-prompt.md`
- `prompt/token-position-setup-prompt.md`

Obiettivo:
- verificare se i finding iniziali sono stati chiusi o solo mitigati
- identificare rischi residui
- definire i prossimi test utili

## Esito Sintetico
- esito generale: `miglioramento materiale, con alcuni punti ancora parzialmente aperti`
- area migliorata di piu: `trade prompt`
- area migliorata ma ancora sensibile: `research prompt`
- area resa piu robusta operativamente: `position setup prompt`

## Audit Per Finding

### 1. Mancanza di `trade activation test`
- severita iniziale: `alta`
- stato dopo il fix: `chiuso`
- cosa e stato fatto:
  - introdotto `trade activation test`
  - aggiunti `stato del setup tattico`
  - aggiunta regola che impedisce il `no trade` vago se il trigger e davvero attivo
- riferimenti:
  - [token-trade-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-trade-prompt.md:334)
  - [token-trade-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-trade-prompt.md:536)
  - [token-trade-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-trade-prompt.md:608)
- nota:
  - il prompt ora distingue in modo piu netto `attivo / condizionale / non attivo`

### 2. Vincoli di formato incompatibili
- severita iniziale: `alta`
- stato dopo il fix: `chiuso`
- cosa e stato fatto:
  - `Executive view` portato a `Massimo 14 righe`
  - `Inherited setup` portato a `massimo 9 righe`
- riferimenti:
  - [token-trade-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-trade-prompt.md:375)
  - [token-position-setup-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-position-setup-prompt.md:197)

### 3. Priorita direzionale troppo rigida
- severita iniziale: `medio-alta`
- stato dopo il fix: `parzialmente chiuso`
- cosa e stato fatto:
  - introdotta `forza della priorita direzionale`
  - definizione di casi `forte / debole / nessuna`
  - esplicitato che priorita `debole` non equivale a comando operativo
- riferimenti:
  - [token-trade-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-trade-prompt.md:94)
  - [token-trade-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-trade-prompt.md:112)
  - [token-trade-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-trade-prompt.md:577)
  - [token-trade-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-trade-prompt.md:603)
- rischio residuo:
  - la classificazione `forte / debole / nessuna` resta comunque qualitativa
  - un futuro hardening potrebbe renderla ancora piu meccanica con gate piu espliciti su `event-driven` e `copertura dati`

### 4. Duplicazioni nel research prompt
- severita iniziale: `medio-alta`
- stato dopo il fix: `parzialmente chiuso`
- cosa e stato fatto:
  - introdotta `Opacity compression rule`
  - la sezione sviluppi recenti ora dice di sintetizzare il controllo trasversale invece di duplicarlo
  - la sezione finale `Source reconciliation` ora dice di riportare solo divergenze residue
- riferimenti:
  - [token-research-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-research-prompt.md:91)
  - [token-research-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-research-prompt.md:399)
  - [token-research-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-research-prompt.md:544)
  - [token-research-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-research-prompt.md:594)
- rischio residuo:
  - le sezioni duplicate esistono ancora come struttura
  - oggi il rischio e mitigato da istruzioni anti-ripetizione, ma non eliminato del tutto

### 5. Watchlist e ordine quasi eseguibile confusi nel position setup
- severita iniziale: `media`
- stato dopo il fix: `chiuso`
- cosa e stato fatto:
  - aggiunto `setup state gating`
  - aggiunto ramo `watchlist`
  - resi espliciti i casi in cui ticket e protective orders diventano `watchlist template` o `n.a.`
- riferimenti:
  - [token-position-setup-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-position-setup-prompt.md:99)
  - [token-position-setup-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-position-setup-prompt.md:173)
  - [token-position-setup-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-position-setup-prompt.md:237)
  - [token-position-setup-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-position-setup-prompt.md:265)
  - [token-position-setup-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-position-setup-prompt.md:284)
  - [token-position-setup-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-position-setup-prompt.md:315)

### 6. Scenario map senza timeframe unico forzato
- severita iniziale: `media`
- stato dopo il fix: `chiuso`
- cosa e stato fatto:
  - introdotto il campo `timeframe comune della scenario map`
- riferimenti:
  - [token-trade-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-trade-prompt.md:520)

### 7. Precisione troppo aggressiva nel research per asset opachi
- severita iniziale: `media`
- stato dopo il fix: `parzialmente chiuso`
- cosa e stato fatto:
  - introdotta `Opacity compression rule`
  - aggiunta regola finale per comprimere le sezioni troppo opache invece di moltiplicare i `non trovato`
- riferimenti:
  - [token-research-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-research-prompt.md:91)
  - [token-research-prompt.md](/Users/coding/Documents/GitHub/token-research-prompt/prompt/token-research-prompt.md:594)
- rischio residuo:
  - il research prompt resta deliberatamente molto esigente
  - su asset fortemente offchain o poco trasparenti, il rischio di verbosita resta piu alto che negli altri prompt

## Edge Case Audit

### Token appena listati o con meno di `3-6 mesi` di storia
- stato: `migliorato`
- motivo:
  - migliore distinzione tra `HODL` e trade
  - priorita direzionale ora puo essere `debole`
  - manca ancora un test empirico post-fix su un case reale appena listato

### Asset `event-driven` con perp in sconto e funding negativo
- stato: `migliorato molto`
- motivo:
  - il nuovo `trade activation test` e la priorita `short debole/forte` aiutano a non forzare lo short prima del trigger

### Asset `spot-only` o con short non disponibile
- stato: `migliorato`
- motivo:
  - il `position setup prompt` ora degrada meglio verso `watchlist` o `no-order`
- rischio residuo:
  - conviene testare un caso reale senza venue short disponibile

### Asset con fondamentale debole ma chart molto forte
- stato: `migliorato molto`
- motivo:
  - la coppia `lato prioritario da cercare` + `lato con edge maggiore adesso` + `trade activation test` e ora molto piu robusta

### Asset opachi / culture coin / branded token / business offchain
- stato: `migliorato ma ancora sensibile`
- motivo:
  - il `research prompt` sa comprimere meglio
- rischio residuo:
  - resta il tipo di asset piu difficile per il research framework

## Cosa Regge Bene
- la separazione `research -> trade -> execution` resta giusta
- la tassonomia timeframe del `trade prompt` resta forte
- la distinzione `HODL / spot hold / swing / no trade` resta corretta
- `lato prioritario da cercare` e ora piu utile perche ha anche una `forza`
- il `position setup prompt` ora distingue molto meglio `condizionale` e `watchlist`

## Rischi Residui
- il `research prompt` e ancora il blocco piu pesante e meno elegante del sistema
- la `forza della priorita direzionale` resta qualitativa e non ancora pienamente meccanica
- i nuovi prompt non sono ancora stati stressati su una suite ampia di asset molto diversi
- `prompt/token-position-setup-prompt.md` e presente su disco ma risulta escluso tramite `.git/info/exclude`, quindi i suoi cambiamenti non emergono nel normale `git status`

## Prossimi Test Consigliati
- un asset appena listato con storico molto corto
- un large cap maturo tipo `ETH` o `AAVE`
- un asset `spot-only`
- un asset con vero setup `swing long attivo`
- un asset con vero setup `swing short attivo`

## Verdetto Finale
- roadmap: `creata`
- hardening strutturale: `eseguito`
- audit finale: `eseguito`
- stato complessivo: `solido ma non definitivo`
- giudizio finale:
  - i bug piu pericolosi del framework operativo sono stati chiusi
  - il sistema ora distingue meglio tra tesi, priorita, attivazione e ordine
  - il prossimo salto di qualita verra da test ripetuti su casi diversi, non da altra teoria astratta
