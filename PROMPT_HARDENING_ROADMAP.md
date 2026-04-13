# Prompt Hardening Roadmap

## Scope
Questa roadmap copre i tre prompt principali del repo:
- `prompt/token-research-prompt.md`
- `prompt/token-trade-prompt.md`
- `prompt/token-position-setup-prompt.md`

Obiettivo:
- ridurre ambiguita operative
- eliminare conflitti interni di formato
- trasformare meglio una tesi strutturale in un segnale operativo o in una watchlist disciplinata
- comprimere il rumore dove il dato non consente precisione reale

## Findings Prioritari

### 1. Mancanza di `trade activation test`
Severita: `alta`

Problema:
- il trade prompt riesce a separare bene `verdetto fondamentale`, `lato prioritario da cercare` e `lato con edge adesso`
- ma non contiene ancora una soglia esplicita che obblighi il passaggio da `watchlist` a `trade attivo`

Effetto pratico:
- output coerenti ma non abbastanza decisivi
- rischio di chiusure ripetute in `no trade` anche quando il trigger e quasi chiaramente presente

Fix previsto:
- introdurre una sezione `trade activation test`
- definire condizioni minime per passare da:
  - `watchlist`
  - `ordine condizionale`
  - `trade attivo`

### 2. Vincoli di formato incompatibili
Severita: `alta`

Problema:
- alcune sezioni impongono un numero massimo di righe incompatibile con il numero di campi richiesti

Effetto pratico:
- il modello deve scegliere arbitrariamente cosa comprimere o omettere
- aumenta il rischio di output disomogenei

Fix previsto:
- riallineare i limiti di lunghezza ai campi richiesti
- dove serve, sostituire il limite di righe con un limite di frasi o con output telegrafico strutturato

### 3. Priorita direzionale troppo rigida
Severita: `medio-alta`

Problema:
- `sopravvalutato -> short` e `sottovalutato -> long` e concettualmente utile
- ma oggi manca un `confidence gate` legato a:
  - confidenza del verdetto
  - regime event-driven
  - copertura dati

Effetto pratico:
- la priorita puo risultare troppo forte anche quando il fondamentale e ancora poco robusto

Fix previsto:
- introdurre un gate esplicito che degradi la priorita a `debole` o `nessuna` in caso di:
  - confidenza bassa
  - copertura insufficiente
  - evento materiale ancora aperto

### 4. Duplicazioni nel research prompt
Severita: `medio-alta`

Problema:
- `recent event audit` e `source reconciliation` compaiono sia come controlli trasversali sia come sezioni strutturali

Effetto pratico:
- rischio di ripetizione
- maggiore verbosita
- maggiore probabilita di inconsistenza tra sezioni simili

Fix previsto:
- lasciare i controlli trasversali come obbligo metodologico
- rendere le sezioni finali piu sintetiche e non ridondanti
- eliminare doppioni dove il secondo blocco non aggiunge struttura nuova

### 5. Watchlist e ordine quasi eseguibile confusi nel position setup
Severita: `media`

Problema:
- il prompt dice giustamente di non forzare un ordine se il setup non e attivo
- ma poi obbliga comunque a compilare `Order ticket`, `Protective orders` e `Target map`

Effetto pratico:
- una watchlist puo sembrare un ticket quasi pronto
- rischio di falsa precisione operativa

Fix previsto:
- separare esplicitamente il ramo:
  - `trade attivo`
  - `ordine condizionale`
  - `watchlist / no-order`
- nel ramo `watchlist`, rendere opzionali o molto piu leggere le sezioni ordine e protective orders

### 6. Scenario map senza timeframe unico forzato
Severita: `media`

Problema:
- la probabilistic scenario map chiede scenari e probabilita
- ma non forza che tutti gli scenari vivano sullo stesso orizzonte operativo

Effetto pratico:
- possono nascere mappe miste ore / giorni / settimane non confrontabili

Fix previsto:
- introdurre un campo obbligatorio `timeframe comune della scenario map`
- richiedere che tutti gli scenari siano comparabili sullo stesso orizzonte dominante

### 7. Precisione troppo aggressiva nel research per asset opachi
Severita: `media`

Problema:
- il research prompt richiede sempre un livello di ricostruzione molto profondo
- su asset con disclosure scarsa questo produce report lunghi pieni di `non trovato`

Effetto pratico:
- rumore
- costo cognitivo alto
- minore leggibilita

Fix previsto:
- introdurre un meccanismo esplicito di `compressione per opacita`
- se mancano i dati per chiudere waterfall / supply / treasury con rigore, comprimere la sezione e alzare il rischio analitico invece di ripetere assenze

## Edge Cases Da Testare
- token appena listati o con meno di `3-6 mesi` di storia
- asset `event-driven` con perp in sconto e funding negativo
- asset `spot-only` o senza short disponibile
- asset con fondamentale debole ma chart molto forte
- asset opachi / culture coin / branded token / business fortemente offchain

## Stato Attuale
- `Fase 1`: `completata`
- `Fase 2`: `completata`
- `Fase 3`: `completata`
- `Fase 4`: `completata`
- prompt oggi piu avanti: `token-trade-prompt.md`
- prompt ancora piu pesante da rifinire: `token-research-prompt.md`
- caveat di repo da risolvere o almeno documentare: `prompt/token-position-setup-prompt.md` e escluso dal normale tracking git

## Piano di Esecuzione

### Fase 1. Hardening strutturale `completata`
- sistemati i limiti di formato incompatibili
- aggiunto `trade activation test`
- aggiunto `confidence gate` qualitativo alla priorita direzionale
- forzato timeframe comune per la scenario map

Output atteso:
- meno chiusure vaghe in `no trade`
- piu chiarezza tra `tesi`, `priorita`, `trigger`, `attivazione`

### Fase 2. Riduzione del rumore `completata`
- mitigata la duplicazione nel research prompt
- introdotta compressione esplicita per asset opachi
- chiarito quando comprimere invece di riempire sezioni con `non trovato`

Output atteso:
- research piu leggibile senza allentare troppo la severita

### Fase 3. Execution branch clarity `completata`
- distinto meglio `trade attivo`, `ordine condizionale`, `watchlist`
- corretto il degrado del position setup quando il lato e giusto ma non ancora attivo

Output atteso:
- meno pseudo-ticket
- migliore separazione tra idea valida e ordine davvero eseguibile

### Fase 4. Audit finale `completata`
- verificati i finding iniziali
- verificato che `RAVE` continui a produrre un output coerente
- isolati i punti ancora `parzialmente chiusi`

Output atteso:
- baseline audit chiara da cui partire per il round successivo

### Fase 5. Empirical test matrix `prossima`
Obiettivo:
- smettere di validare i prompt solo su `RAVE`
- verificare che il framework distingua davvero archetipi diversi senza collassare sempre su `avoid`

Suite minima da testare:
1. `large cap maturo`
   - esempi candidati: `ETH`, `AAVE`
   - cosa deve provare: distinzione chiara tra `HODL`, `spot hold`, `swing` e bias multi-timeframe coerente
2. `token appena listato`
   - cosa deve provare: priorita direzionale piu prudente, scenario map non troppo sicura, spazio per `watchlist`
3. `asset event-driven con narrativa forte`
   - cosa deve provare: lato prioritario corretto ma nessuna attivazione anticipata senza trigger
4. `asset spot-only o short non disponibile`
   - cosa deve provare: edge teorico separato da eseguibilita reale su venue
5. `asset opaco / culture coin / branded token`
   - cosa deve provare: compressione del research senza report gonfio e ripetitivo
6. `caso con swing long davvero attivo`
   - cosa deve provare: il prompt sa anche dire `attivo`, non solo `watchlist`
7. `caso con swing short davvero attivo`
   - cosa deve provare: il framework non ha bias long e sa produrre un short operativo pulito

Deliverable:
- almeno `1 report completo` per ciascun archetipo
- nota finale per ogni caso: `decisione giusta / troppo prudente / troppo aggressiva / ancora ambigua`

### Fase 6. Decision engine hardening `prossima`
Obiettivo:
- rendere meno qualitativa la logica che collega `verdetto fondamentale` a `lato prioritario`
- rendere piu meccanica la differenza tra `attivo`, `condizionale`, `watchlist`, `no-order`

Interventi previsti:
- formalizzare meglio `forza della priorita direzionale`
- aggiungere gate piu espliciti su:
  - `confidenza del verdetto`
  - `copertura dati`
  - `regime event-driven`
  - `frizione di execution`
- allineare i nomi degli stati tra trade prompt e position setup prompt

Target:
- meno casi borderline interpretati in modo diverso da run a run
- piu probabilita che due esecuzioni simili producano la stessa classe finale

### Fase 7. Research prompt simplification `prossima`
Obiettivo:
- intervenire non solo con istruzioni anti-duplicazione, ma anche sulla struttura

Interventi previsti:
- eliminare dove possibile i doppioni metodologici ancora presenti
- introdurre un ramo piu esplicito `full diligence` vs `opacity-compressed`
- chiarire quali sezioni sono obbligatorie sempre e quali diventano sintetiche in assenza di disclosure seria

Target:
- report piu corti sugli asset opachi
- meno rischio che il prompt premi verbosita al posto di rigore

### Fase 8. Release discipline e regression control `prossima`
Obiettivo:
- trasformare l hardening in un processo ripetibile, non in una patch una tantum

Interventi previsti:
- creare una mini suite di benchmark interni
- conservare output `prima / dopo` dei casi principali
- annotare regressioni osservate dopo ogni modifica importante ai prompt
- decidere in modo esplicito se `prompt/token-position-setup-prompt.md` deve restare escluso da git o va tracciato

Target:
- ogni modifica futura ai prompt deve poter essere verificata contro un corpus minimo noto

## Review Mirate Da Eseguire

### Review 1. Trade prompt
- verificare se esiste ancora qualche strada che permette un `no trade` ambiguo nonostante trigger quasi attivo
- verificare se `forza della priorita direzionale` e abbastanza chiara da produrre esiti stabili
- verificare se il prompt sa emettere con naturalezza sia `swing long attivo` sia `swing short attivo`

### Review 2. Research prompt
- cercare ridondanze residue tra controlli trasversali e sezioni finali
- verificare se il ramo `opacity compression` riduce davvero il rumore o resta solo cosmetico
- controllare se il framework resta leggibile su progetti con disclosure minima

### Review 3. Position setup prompt
- verificare che `watchlist` non si trasformi piu in ticket quasi eseguibile
- verificare che `ordine condizionale` e `watchlist` non collassino nella stessa cosa
- verificare che il prompt degradi bene quando manca la venue short o la liquidita

### Review 4. Cross-prompt consistency
- verificare coerenza lessicale tra `research -> trade -> position setup`
- verificare che un `edge short` nel trade prompt non venga poi tradotto in setup long senza motivazione forte
- verificare che `HODL` e `trade tattico` restino separati e non si contaminino

## Acceptance Criteria

### Trade prompt
- deve sempre dichiarare:
  - `lato prioritario da cercare`
  - `forza della priorita direzionale`
  - `lato con edge maggiore adesso`
  - `stato del setup tattico`
- la scenario map deve usare un solo orizzonte dominante
- se il trigger e davvero presente e l execution e almeno media, il prompt non deve chiudere in `no trade` vago

### Research prompt
- non deve ripetere meccanicamente `recent event audit` e `source reconciliation`
- deve poter comprimere bene asset opachi senza perdere il punto analitico
- deve esplicitare quando una conclusione e limitata da dati mancanti, non solo accumulare assenze

### Position setup prompt
- se lo stato e `watchlist` o `no-order`, non deve sembrare un ticket eseguibile
- deve separare chiaramente `idea valida ma non attiva` da `ordine pronto`
- deve degradare bene l eseguibilita in base a venue, liquidita e disponibilita del lato short

### Sistema complessivo
- i prompt devono produrre esiti distinti su archetipi distinti
- il framework non deve avere bias implicito long
- il framework non deve nemmeno avere bias difensivo che porta sempre a `avoid`

## Audit Output Atteso
Alla fine del prossimo ciclo, l audit dovra dichiarare esplicitamente:
- cosa e stato corretto in modo definitivo
- cosa e migliorato ma resta parzialmente aperto
- quali archetipi hanno ancora prodotto esiti deboli o ambigui
- quale prompt resta il collo di bottiglia principale
- se la repo hygiene e stata chiusa oppure no

## Prossime Azioni Immediate
1. Eseguire la `Fase 5` su una suite minima di archetipi reali.
2. Usare i fallimenti emersi per chiudere la `Fase 6` e la `Fase 7`.
3. Chiudere la `Fase 8` con benchmark interni e decisione esplicita sul tracking git del `position setup prompt`.
