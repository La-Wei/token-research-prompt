Analizza il token [NOME/TICKER] come un discretionary crypto trader / market operator focalizzato su:
- price action multi-timeframe
- market structure
- liquidity e liquidation map
- derivati e positioning
- qualita di esecuzione della view

Obiettivo:
capire quale sia la migliore espressione operativa adesso, distinguendo chiaramente tra:
- bias di contesto
- view investment / HODL di lungo periodo
- view spot / positional
- setup tattico
- stato di attivazione del setup
- eseguibilita reale
- priorita di ricerca direzionale derivata dal verdetto fondamentale
- confronto simmetrico tra caso `long` e caso `short`
- strategia probabilistica con scenari, trigger e lato con edge migliore

Prerequisito consigliato:
assumi come input primario l output di `prompt/token-research-prompt.md`, se disponibile.
Questo prompt deve partire da quelle conclusioni e trasformarle in una market expression sensata.
Non deve rifare da zero:
- business quality
- token quality
- tokenomics
- value accrual
- unlock analysis
- right-to-exist test
Se il report fondamentale non e disponibile, dillo subito e abbassa la confidenza soprattutto sulle conclusioni spot / positional.
Se esiste anche il report di verifica, trattalo come contesto prevalente per:
- correzioni materiali del report fondamentale
- eventi recenti
- dispute di governance
- exploit, halt, delisting risk, partner loss o altri thesis-change events

Principio guida:
non confondere mai:
- asset interessante
- asset valido da `HODL` multi-quarter / multi-year
- spot long sensato
- short sensato
- lato prioritario da cercare
- setup tradabile bene
- trade eseguibile bene
- lato con edge probabilistico migliore

Un token bullish di lungo periodo puo essere:
- un buon `HODL`
- un buon spot long-term
- un pessimo long oggi
- un no trade tattico

Un token debole puo essere:
- un pessimo `HODL` ma un buon long di rimbalzo
- un pessimo spot long
- un buon short
- un pessimo short se squeeze, carry o liquidita lo rendono inefficiente

Un token `sopravvalutato` puo essere:
- un ottimo short
- un pessimo short se il mercato e gia troppo short, il perp e in sconto o il carry penalizza la view
- un `no trade` se il lato short e concettualmente giusto ma statisticamente sporco

`No trade` e una conclusione valida.

SIMMETRIA DIREZIONALE OBBLIGATORIA

Non trattare il `long` come direzione di default.
Long e short devono passare lo stesso burden of proof.
Simmetria non significa neutralita artificiale.
Devi testare long e short con lo stesso rigore, ma non dare per forza la stessa priorita operativa ai due lati.

Per ogni asset devi sempre costruire e stressare:
- il miglior caso `long` disponibile adesso
- il miglior caso `short` disponibile adesso
- il motivo per cui uno dei due lati non ha edge sufficiente

Se il verdetto fondamentale ereditato e `sopravvalutato`:
- non saltare automaticamente allo short
- ma non proteggerlo nemmeno artificialmente
- verifica in modo esplicito se esiste uno short con edge reale, buona eseguibilita e buona asimmetria

Se il verdetto fondamentale ereditato e `sottovalutato`:
- non regalare automaticamente il long
- verifica in modo esplicito se esiste davvero un long con edge reale, buona eseguibilita e buona asimmetria

Distingui sempre tra:
- `tesi corretta`
- `lato prioritario da cercare`
- `trade con edge`
- `trade eseguibile sul venue giusto`

PRIORITA DIREZIONALE DERIVATA DAL VERDETTO

Il verdetto fondamentale non decide da solo l entry, ma deve orientare dove cerchi l edge per primo.

Regola base:
- se il verdetto fondamentale ereditato e `sopravvalutato`, il lato prioritario da cercare e `short`
- se il verdetto fondamentale ereditato e `sottovalutato`, il lato prioritario da cercare e `long`
- se il verdetto fondamentale ereditato e `fairly priced`, `non disponibile` o `non analizzabile con rigore sufficiente`, il lato prioritario da cercare e `nessuno`

Questo significa:
- il lato prioritario va cercato per primo
- il lato opposto non e vietato, ma va trattato come `countertrend`, `squeeze continuation` o `mean-reversion tattica`, a seconda del caso
- se scegli il lato opposto, devi spiegare in modo esplicito:
  - perche il lato prioritario non e tradabile adesso
  - perche il lato opposto ha edge migliore nonostante il fondamentale
- se il lato prioritario e concettualmente giusto ma non ha ancora trigger, timing o carry favorevole, la risposta corretta puo essere `watchlist` o `no trade` a seconda di quanto il setup sia gia disciplinabile
- non dare automaticamente pari priorita operativa ai due lati solo per sembrare neutrale

FORZA DELLA PRIORITA DIREZIONALE

La priorita direzionale non deve essere sempre uguale in intensita.
Classificala sempre come:
- `forte`
- `debole`
- `nessuna`

Guida pratica:
- `forte` se:
  - il verdetto fondamentale e direzionale (`sopravvalutato` o `sottovalutato`)
  - la confidenza del giudizio strutturale e almeno `media`
  - la copertura dati non e `insufficiente`
  - non esiste un evento aperto che renda il tape ancora troppo dominato da shock non digerito
- `debole` se:
  - il verdetto e direzionale ma la confidenza e `bassa`
  - oppure il regime e ancora molto `event-driven`
  - oppure la copertura dati e solo `parziale` sui blocchi che contano per l execution
- `nessuna` se:
  - il verdetto fondamentale ereditato e `fairly priced`, `non disponibile` o `non analizzabile con rigore sufficiente`
  - oppure la copertura dati e troppo debole per usare davvero il fondamentale come bussola operativa

GATE MECCANICO DELLA PRIORITA DIREZIONALE

Non limitarti a una sensazione qualitativa.
Valuta sempre questi `4` gate:
- `gate 1 - verdict`: il verdetto fondamentale e davvero direzionale? `si / no`
- `gate 2 - confidenza`: la confidenza del giudizio strutturale e almeno `media`? `si / no`
- `gate 3 - copertura dati`: la copertura dati e almeno `parziale` senza buchi critici sui blocchi che contano per l execution? `si / no`
- `gate 4 - regime`: il mercato non e piu dominato da un evento aperto o da un possibile `structural break` non digerito? `si / no`

Classificazione obbligatoria:
- `forte` solo se `gate 1 = si` e passano tutti i gate `2 / 3 / 4`
- `debole` se `gate 1 = si` ma fallisce esattamente `1` tra i gate `2 / 3 / 4`
- `nessuna` se `gate 1 = no` oppure falliscono `2` o piu gate tra `2 / 3 / 4`

Hard stops:
- non usare `forte` se la copertura dati e `insufficiente`
- non usare `forte` se il regime e ancora `event-driven` non risolto
- se il fondamentale e direzionale ma la bussola e troppo sporca per guidare l execution, usa `debole` o `nessuna`, non forzare una priorita

Input ideali:
- output o sintesi del `prompt/token-research-prompt.md`, con almeno:
  - business quality
  - token quality
  - market setup strutturale
  - verdict fondamentale
  - rischi principali
  - cosa invalida la tesi fondamentale
- screenshot o chart su timeframe secolari / investment, se disponibili:
  - `max`
  - `1Y`
  - `6M / 3M`
- `monthly candle`, se disponibile
- screenshot o chart su timeframe alti: 1W / 1D
- screenshot o chart su timeframe medi: 4H
- screenshot o chart su timeframe bassi: 1H / 15m, se servono al timing
- dati su volume, open interest, funding, basis, liquidazioni, borrow, spread, depth, se disponibili
- il report fondamentale non sostituisce il setup tecnico, ma deve fare da contesto ereditato

TASSONOMIA TIMEFRAME OBBLIGATORIA

Non usare `HTF` come parola ombrello se questo rende ambigua la lettura.
Separa sempre:
- `secular / investment context`: massimo storico disponibile, poi `1Y`, `6M`, `3M` e `monthly candle`, se disponibile
- `higher timeframe directional`: 1W e 1D
- `mid timeframe`: 4H
- `execution timeframe`: 1H e 15m

Se un timeframe non e disponibile, dillo esplicitamente.
Non inferire una tesi da `HODL multi-year` usando solo `1D` o `4H`.
Se l asset e abbastanza maturo da avere storico lungo, non fermarti a `7d`, `30d` o all ultima gamba di mercato.
Per asset come `BTC`, `ETH`, `SOL`, `AAVE`, `UNI` o altri nomi con anni di storia, la lettura investment deve guardare indietro abbastanza da coprire piu regimi di mercato, non solo il mese corrente.
Un bias `1W bullish` puo convivere con un `1D iper-esteso` e con un `bias operativo neutral`.
Nel verdetto finale specifica sempre almeno:
- `bias secular / investment`
- `bias 1W`
- `bias 1D`
- `bias operativo`
- `orizzonte holding implicito`
Se il massimo timeframe disponibile e troppo corto per una lettura multi-year, dichiaralo esplicitamente e abbassa la confidenza sul caso `HODL`.

EVENT E REGIME DISCOVERY OBBLIGATORIA

Prima di leggere il chart come se nulla fosse, verifica sempre cosa e successo negli ultimi `7d`, `30d` e `90d`, se rilevanti.

Controlla almeno:
- governance dispute / founder conflict / key person exit
- exploit / halt / outage / oracle failure / security incident
- listing / delisting / perdita di partner chiave / cambio market maker
- unlock, emission changes, treasury actions, fee switch o buyback changes
- launch prodotto o announcement che ha spostato davvero prezzo e positioning
- indagini, cause, enforcement o warning regolatori

Per ogni evento materiale indica sempre:
- data esatta
- fonte primaria o migliore fonte disponibile
- stato: confermato / contestato / smentito / in evoluzione
- cosa e successo davvero
- cosa e solo allegation o narrativa
- market reaction osservata: prezzo, volume, OI, funding, liquidazioni, se disponibili
- se il move attuale appare:
  - continuation tecnica
  - repricing da evento
  - overshoot da panico/euforia
  - regime change potenziale

Se non trovi eventi materiali, scrivilo esplicitamente in una riga.

SOURCE DISCOVERY OBBLIGATORIA

Se l utente non fornisce chart o screenshot, non fermarti subito.
Prima di dichiarare i timeframe "insufficienti", cerca attivamente fonti affidabili che permettano di ricostruire il setup.

Ordine di priorita consigliato:
- API o chart ufficiali del protocollo / exchange principale
- API o chart ufficiali del venue derivato piu liquido, se diverso dal venue spot
- TradingView
- CoinMarketCap
- CoinGecko
- dashboard di mercato terze solo come fallback

Cerca sempre, se disponibile:
- `max history` per il contesto secolare / investment
- `1Y`
- `6M`
- `3M`
- `monthly candle` per il contesto secolare / investment
- `1W` per il bias alto
- `1D` per il directional context
- `4H` per la struttura intermedia
- `1H / 15m` per il timing
Se non trovi `max / 1Y / 6M / 3M / monthly candle`, dichiara esplicitamente che il massimo timeframe disponibile e `1W` e non fingere una view `HODL` di anni.

Per token trattati su Hyperliquid, cerca prima di tutto:
- `candleSnapshot` per 15m / 1h / 4h / 1d / 1w
- `l2Book`
- eventuali feed trades / websocket / info endpoint ufficiali

Se il token tratta spot su una venue e perp su un altra, puoi usare entrambe, ma distingui sempre:
- quale fonte descrive lo spot
- quale fonte descrive il perp / positioning

Se esiste una fonte che offre OHLC reali multi timeframe, non accontentarti di proxy tipo solo `7d`, `30d` o range aggregati.
Puoi concludere `copertura dati insufficiente` solo dopo aver esplicitato:
- quali fonti hai provato
- quali timeframe sei riuscito a ottenere
- quali blocchi restano davvero non osservabili

Per la parte `investment / HODL` non basta quasi mai una singola finestra `7d / 30d`.
Se l asset ha abbastanza storia, devi almeno provare a leggere:
- un chart `max` o il piu lungo possibile
- `1Y`
- un timeframe che mostri il regime intermedio (`6M / 3M`) e, se disponibile, `monthly candle`

FRAMEWORK PROBABILISTICO OBBLIGATORIO

Non basta dire `bullish`, `bearish` o `sopravvalutato`.
Devi sempre costruire una lettura probabilistica condizionale.

Regole:
- usa probabilita soggettive ma disciplinate
- usa percentuali arrotondate in blocchi da `5%` o `10%`, non pseudo-precisione tipo `53%`
- la somma degli scenari deve fare `100%`
- preferisci il lato con migliore combinazione di:
  - probabilita
  - payoff potenziale
  - qualita di esecuzione
  - costo di carry / funding / borrow

Costruisci almeno questi scenari sul timeframe dominante della tesi:
- `continuation bullish`
- `reversion / breakdown bearish`
- `chop / nessuna risoluzione`
- `event extension` solo se davvero rilevante

Per ogni scenario indica:
- probabilita stimata
- trigger / condizione di attivazione
- path di prezzo atteso
- trade o non-trade preferito
- cosa invalida quello scenario

Se nessun lato ha aspettativa abbastanza buona dopo spread, slippage, carry e rischio squeeze:
- concludi `no trade`

CLASSIFICATORE DELLO STATO TATTICO

Usa sempre una di queste classi finali:
- `attivo`
- `condizionale`
- `watchlist`
- `no-trade`

Definizioni:
- `attivo`: trigger gia presente, invalidazione chiara, lato con `EV` migliore definito, eseguibilita almeno `media`
- `condizionale`: trigger preciso e disciplinabile ma non ancora attivo; si puo gia preparare un ordine condizionale
- `watchlist`: esiste una direzione o un edge teorico, ma trigger, invalidazione o execution non sono ancora abbastanza puliti per chiamarlo trade
- `no-trade`: nessun lato supera davvero costi, carry, squeeze risk, execution friction o inaffidabilita del prezzo

Mapping verso il prompt di execution:
- `attivo` -> `ordine valido adesso`
- `condizionale` -> `ordine condizionale`
- `watchlist` -> `watchlist`
- `no-trade` -> `no-order`

GATE MECCANICO DELLO STATO TATTICO

Per evitare ambiguita tra `condizionale`, `watchlist` e `no-trade`, valuta sempre questi gate sul lato con `EV` migliore adesso.
Quel lato e il vero `lato candidato all attivazione`, e puo coincidere oppure no con il lato prioritario derivato dal fondamentale.

Gate obbligatori:
- `gate A - lato candidato`: esiste un lato con `EV` migliore chiaramente identificabile? `si / no`
- `gate B - trigger definito`: esiste un trigger preciso e osservabile? `si / no`
- `gate C - trigger attivo`: il trigger e gia presente adesso? `si / no`
- `gate D - invalidazione disciplinabile`: l invalidazione e chiara e abbastanza vicina? `si / no`
- `gate E - execution`: execution almeno `media` senza blocker straordinario da venue / carry / squeeze / evento aperto? `si / no`

Classificazione obbligatoria:
- `attivo` solo se `A / B / C / D / E = si`
- `condizionale` se `A / B / D / E = si` ma `C = no`
- `watchlist` se esiste una direzione plausibile ma manca ancora almeno uno tra `B`, `D` o `E` senza che il caso sia del tutto invalidato
- `no-trade` se `A = no` oppure se nessun lato supera davvero costi, carry, execution friction o affidabilita del prezzo

REGOLE DI RIGORE

- Non inventare livelli, pattern o dati non visibili nei chart forniti.
- Se i chart sono incompleti, vecchi o poco leggibili, dillo chiaramente.
- Non e ammissibile fermarsi a proxy aggregati se esistono chart o API ragionevolmente accessibili con OHLC reali multi-timeframe.
- Se mancano dati su OI, funding, borrow, liquidita o liquidazioni, non fingere precisione.
- Non trattare un dump o squeeze da governance shock, exploit o delisting fear come semplice `healthy pullback` o `breakout` senza verificare prima l evento.
- Distingui sempre tra:
  - movimento tecnico ordinario
  - reazione a evento confermato
  - reazione a allegation / rumor
  - structural break ancora aperto
- Distingui sempre tra osservazioni visibili sui grafici, inferenze operative e scenari condizionali.
- Distingui sempre tra:
  - tesi strutturale ereditata dal prompt fondamentale
  - investment case multi-quarter / multi-year
  - market expression attuale
  - timing operativo
- Specifica sempre in quale timeframe vive la tesi.
- Specifica sempre cosa invalida la tesi sul timeframe rilevante.
- Non usare una frase tipo `bias HTF: bullish` se in realta stai comprimendo segnali diversi tra `monthly / secular`, `1W` e `1D`.
- Se i timeframe alti divergono, esplicitalo. Esempio corretto:
  - `bias secular bullish`
  - `1W bullish`
  - `1D bullish ma iper-esteso`
  - `operativo neutral`
- Non chiamare `HODL multi-year` una view costruita solo su `1W / 1D` se lo storico disponibile non consente davvero una lettura di anni.
- Non ricalcolare da zero le parti gia coperte dal prompt fondamentale, salvo errori evidenti o contraddizioni forti con il prezzo o con i dati di mercato.
- Se il chart o il positioning contraddicono la tesi fondamentale, non riscrivere tutta la tesi: spiega il mismatch tra fair value view e setup operativo.
- Non forzare una view.
- Non confondere un buon chart con un buon risk/reward.
- Non confondere un buon risk/reward con una buona eseguibilita.
- Non usare linguaggio assoluto tipo `partira sicuramente`, `reversal confermato`, `short ovvio` o `breakout pulito` se il dato non lo supporta chiaramente.
- Se un evento materiale e ancora aperto e impedisce di capire se il move sia tecnico o strutturale, `no trade` resta un output preferibile a una view inventata.
- Se il setup non e abbastanza chiaro ma una direzione resta plausibile, usa `watchlist`; usa `no trade` solo quando nessun lato e davvero disciplinabile.

ORDINE DI LAVORO OBBLIGATORIO

1. Leggi prima il report fondamentale, se disponibile, ed estrai la tesi strutturale ereditata.
2. Leggi il report di verifica, se disponibile, e preferiscilo in caso di conflitto.
3. Verifica gli eventi recenti e stabilisci se il mercato sta reagendo a un `event shock` ancora aperto.
4. Se i chart non sono gia forniti, fai source discovery e recupera prima lo storico lungo disponibile: `max / 1Y / 6M / 3M / monthly candle`, poi `1W / 1D / 4H / 1H / 15m`.
5. Leggi prima il contesto `secular / investment`, se i dati lo permettono.
6. Leggi poi `1W / 1D`.
7. Verifica allineamento o conflitto sul `4H`.
8. Solo alla fine valuta il timing su `1H / 15m`, se serve.
9. Traduci il verdetto fondamentale in una priorita di ricerca direzionale:
  - `long`
  - `short`
  - `nessuna`
10. Classifica anche la forza di quella priorita:
  - `forte`
  - `debole`
  - `nessuna`
11. Poi integra positioning, funding, OI, liquidita e squeeze risk.
12. Esegui un `trade activation test` esplicito.
13. Solo dopo decidi:
  - lo stato del setup tattico
  - il lato con `EV` migliore adesso
  - se quel lato e gia `attivo`, solo `condizionale`, solo `watchlist` o `no-trade`
14. Poi decidi qual e la migliore espressione per:
  - `investment / HODL`
  - `spot / positional`
  - `swing long`
  - `swing short`
  - `no trade`

MAPPA OPERATIVA OBBLIGATORIA

Per evitare duplicazioni o omissioni, usa sempre questa mappa:
- `event e regime discovery`:
  - serve come metodo di lavoro
  - deve emergere nella sezione `1. Recent event e regime evidence log`
- `source discovery`:
  - deve emergere nella sezione `0. Market status`
  - devi dire quali fonti hai usato o tentato se la copertura resta debole
- `priorita direzionale`:
  - deve chiudersi in `8A. Directional symmetry test`
  - e poi in `14. Decisione finale`
- `framework probabilistico`:
  - deve chiudersi in `12A. Probabilistic scenario map`
- `trade activation test`:
  - deve usare il lato con `EV` migliore adesso come `lato candidato all attivazione`
  - deve chiudersi in `12B. Trade activation test`
- `stato tattico finale`:
  - deve essere coerente tra `12B`, `13` e `14`

STRUTTURA OBBLIGATORIA

0. Market status
- qualita dei chart: alta / media / bassa
- copertura dati: completa / parziale / insufficiente
- fonti principali usate
- fonti tentate ma non ottenute, se rilevanti
- timeframe disponibili
- profondita storica disponibile: max / 1Y / 6M / 3M / monthly candle / 1W o equivalente
- report fondamentale disponibile: si / no
- report di verifica disponibile: si / no
- qualita del contesto ereditato: alta / media / bassa
- principali buchi informativi
- blocchi ancora non osservabili
- confidenza preliminare: alta / media / bassa

1. Recent event e regime evidence log
Compila sempre questa sezione, anche se la risposta e `nessun evento materiale`.

Per gli ultimi `7d`, `30d` e `90d`, se rilevanti:
- evento
- data
- fonte
- stato: confermato / contestato / smentito / in evoluzione
- cosa e confermato
- cosa resta allegation o non chiuso
- market reaction osservata
- impatto su business / token / market structure / fiducia
- l evento e chiuso o ancora aperto?
- il setup corrente sembra tecnico o event-driven?

Chiudi con un mini verdict:
- nessun evento materiale / evento materiale ma transitorio / evento materiale ancora aperto / structural break possibile
- impatto principale: business / token / market structure / fiducia / narrativa
- stato: chiuso / in evoluzione / non risolto

2. Executive view
Massimo 16 righe:
- tesi fondamentale ereditata in 1-2 righe
- coerenza o divergenza rispetto al setup attuale
- investment view: bullish / bearish / neutral / non valutabile
- tactical view: bullish / bearish / neutral
- lato prioritario da cercare: long / short / nessuno
- forza della priorita direzionale: forte / debole / nessuna
- lato con edge maggiore adesso: long / short / nessuno
- stato del setup tattico: attivo / condizionale / watchlist / no-trade
- perche il lato opposto non e preferito
- migliore espressione investment: accumulate / HODL / avoid / non valutabile
- migliore espressione tattica: spot accumulate / spot hold / swing long / swing short / no trade
- scenario dominante con probabilita stimata
- timeframe dominante della view
- motivo principale
- rischio principale contro la view
- grado di eseguibilita

3. Secular / investment context
Analizza prima il massimo storico disponibile:
- `max`, se disponibile
- `1Y`
- `6M / 3M`
- `monthly candle`, se disponibile
Se questi timeframe non sono disponibili, dichiaralo esplicitamente e non forzare una tesi `HODL`.
- regime secolare: bull / bear / range / ricostruzione / distribuzione
- distanza da ATH e da drawdown profondi rilevanti
- posizione attuale dentro il ciclo storico osservabile
- se il prezzo attuale e in early trend, mid trend, late trend o blow-off
- cosa supporta o smentisce un caso `HODL multi-quarter / multi-year`
- cosa invalida la tesi investment
Chiudi sempre con:
- bias `secular / investment`
- confidenza del caso investment: alta / media / bassa

4. Higher timeframe context
Analizza separatamente `1W` e `1D`, se disponibili.
- trend primario
- struttura: HH/HL o LH/LL
- regime: trend / range / compressione / distribuzione / accumulazione
- livelli chiave
- premium o discount rispetto al range HTF
- dove il chart invalida la tesi HTF
Chiudi sempre distinguendo:
- bias `1W`
- bias `1D`

5. Mid timeframe structure
Analizza 4H:
- struttura intermedia
- momentum
- consolidazione o continuazione
- reclaim, rejection, sweep, breakdown, breakout se presenti
- conflitto o allineamento con HTF
- dove si invalida la tesi su timeframe medio

6. Lower timeframe timing
Analizza 1H e 15m solo per timing, non per costruire da zero la tesi:
- trigger di entrata possibili
- conferme richieste
- rischio di chase
- rischio di fake breakout / fake breakdown
- timing migliore: subito / su pullback / su reclaim / su breakdown / aspettare

7. Derivatives e positioning
Analizza, se disponibili:
- open interest
- funding
- basis
- long/short crowding
- liquidazioni vicine
- borrow cost
- short availability
Domande chiave:
- il positioning supporta o contraddice la view?
- c e rischio di squeeze o flush violento?
- il carry aiuta o penalizza la view?

8. Liquidity e execution quality
Analizza:
- liquidita spot reale
- profondita del book
- spread
- slippage potenziale
- qualita delle venue
- concentrazione della liquidita
- presenza di livelli magnete o zone di liquidita ovvie
Domande chiave:
- la view e eseguibile bene oppure solo teorica?
- una size sensata puo entrare e uscire senza troppo attrito?
- il mercato e abbastanza profondo per sostenere la tesi?

8A. Directional symmetry test
Compila sempre questa sezione, anche se il risultato finale e `no trade`.
- lato prioritario da cercare derivato dal fondamentale
- forza della priorita direzionale
- miglior caso `long` disponibile adesso
- miglior caso `short` disponibile adesso
- quale lato ha l asimmetria migliore
- quale lato ha l execution migliore
- perche il lato opposto e inferiore
- differenza tra `tesi corretta` e `trade con edge`
- se il fondamentale e `sopravvalutato`: perche lo short e preferibile oppure perche non lo e ancora
- se il fondamentale e `sottovalutato`: perche il long e preferibile oppure perche non lo e ancora

9. Investment / HODL case
Compila solo se ha davvero senso e se la profondita storica lo consente:
- espressione investment: accumulate now / accumulate on major pullbacks / HODL if already in / avoid / non valutabile
- orizzonte dominante: multi-quarter / multi-year
- timeframe usato per la tesi investment: max / 1Y / 6M / 3M / monthly candle
- coerenza con la tesi fondamentale: coerente / parzialmente coerente / in conflitto
- cosa rende sensato il caso investment
- cosa lo invalida
- cosa migliorerebbe la tesi
- cosa la peggiorerebbe

10. Spot / positional case
Compila solo se ha davvero senso:
- espressione spot: accumulate now / accumulate on pullbacks / hold if already in / avoid
- tipo di caso: positional multi-week / multi-month
- timeframe usato per la tesi spot: 1W / 1D / 4H
- coerenza con la tesi fondamentale: coerente / parzialmente coerente / in conflitto
- cosa rende sensato il caso spot
- cosa lo invalida
- cosa migliorerebbe la tesi
- cosa la peggiorerebbe

11. Swing long case
Compila sempre.
- trigger long
- livello o zona di entrata
- invalidazione
- primi target
- timeframe dominante
- stato del case: attivo / condizionale / watchlist / no-trade
- condizione che trasformerebbe il long in no trade

12. Swing short case
Compila sempre.
- trigger short
- livello o zona di entrata
- invalidazione
- primi target
- timeframe dominante
- stato del case: attivo / condizionale / watchlist / no-trade
- condizione che trasformerebbe lo short in no trade

12A. Probabilistic scenario map
Costruisci una tabella mentale o scritta con almeno `3` scenari:
- timeframe comune della scenario map
- scenario `1`: nome breve
- probabilita stimata
- trigger / condizione
- path di prezzo atteso
- lato favorito: long / short / nessuno
- migliore espressione: swing long / swing short / spot hold / no trade
- invalidazione dello scenario

Chiudi la sezione con:
- scenario dominante
- scenario piu pericoloso contro la tua view
- lato con `EV` migliore adesso: long / short / nessuno

12B. Trade activation test
Compila sempre questa sezione prima del `no-trade test`.
Rispondi in modo secco:
- qual e il lato con `EV` migliore adesso / candidato all attivazione: long / short / nessuno
- questo lato coincide con il lato prioritario oppure no?
- il lato candidato all attivazione ha un trigger attivo adesso?
- l invalidazione e chiara e abbastanza vicina da rendere il trade disciplinabile?
- l eseguibilita e almeno `media`?
- spread, slippage, carry o squeeze risk stanno ancora sabotando il setup?
- un evento aperto impedisce ancora di trattare il prezzo come base affidabile?

Regola di chiusura:
- se il lato candidato all attivazione e definito
- e il suo trigger e `attivo`
- e l invalidazione e chiara
- e l eseguibilita e almeno `media`
- e non c e un blocker straordinario da evento / carry / venue
allora non chiudere con un `no trade` vago: devi classificare il setup come `attivo`.

Chiudi sempre con:
- stato del setup tattico: attivo / condizionale / watchlist / no-trade
- motivo del lato candidato all attivazione
- motivo principale della classificazione

13. No-trade test
Rispondi in modo secco:
- il setup e troppo sporco?
- il risk/reward e insufficiente?
- la liquidita o il positioning peggiorano troppo l esecuzione?
- la view e piu teorica che praticabile?
- un evento ancora aperto rende il prezzo non affidabile come base operativa?
- aspettare darebbe un setup migliore?
- uno dei due lati ha davvero edge probabilistico netto dopo costi e carry?

Regola di chiusura:
- se `A / B / D / E = si` ma il trigger non e ancora attivo, preferisci `condizionale`
- se un lato ha edge teorico ma manca ancora un trigger preciso o un invalidazione pulita, preferisci `watchlist`
- usa `no-trade` solo se nessun lato resta davvero valido dopo costi, carry, execution e affidabilita del prezzo

14. Decisione finale
Chiudi sempre con:
- verdict fondamentale ereditato: sottovalutato / fairly priced / sopravvalutato / non analizzabile con rigore sufficiente / non disponibile
- stato evento/regime: pulito / rumor-driven / event-driven / structural-break risk
- bias secular / investment: bullish / bearish / neutral / non disponibile
- bias 1W: bullish / bearish / neutral / non valutabile
- bias 1D: bullish / bearish / neutral / non valutabile
- bias operativo: bullish / bearish / neutral
- lato prioritario da cercare: long / short / nessuno
- forza della priorita direzionale: forte / debole / nessuna
- lato con edge maggiore adesso: long / short / nessuno
- lato candidato all attivazione: long / short / nessuno
- stato del setup tattico: attivo / condizionale / watchlist / no-trade
- migliore espressione investment: accumulate / HODL / avoid / non valutabile
- migliore espressione tattica: spot accumulate / spot hold / swing long / swing short / no trade
- scenario dominante con probabilita stimata
- timeframe dominante della tesi
- orizzonte holding implicito: intraday / swing multi-day / swing multi-week / positional multi-month / investment multi-quarter / multi-year
- coerenza con la tesi fondamentale: alta / media / bassa / non valutabile
- conviction: alta / media / bassa
- eseguibilita: alta / media / bassa
- invalidation della tesi
- se spot: logica di accumulo o di hold
- se swing: entry logic / invalidation / target logic
- motivo principale del verdetto in massimo 3 frasi

REGOLE FINALI

- Un asset bullish di fondo puo restare `no trade`.
- Un asset bullish di fondo puo essere `spot accumulate` ma non `swing long`.
- Un asset bearish di fondo puo restare `no trade`.
- Un asset bearish di fondo puo offrire uno short tattico.
- Un asset debole puo offrire un long di rimbalzo, ma chiamalo per quello che e.
- Dai pari rigore analitico a long e short, ma non pari priorita operativa quando il fondamentale fornisce una direzione strutturale forte.
- Se il fondamentale e fortemente `sopravvalutato`, cerca prima setup short e tratta i long come continuation / squeeze tattico finche non dimostrano edge superiore.
- Se il fondamentale e fortemente `sottovalutato`, cerca prima setup long e tratta gli short come washout / mean-reversion tattica finche non dimostrano edge superiore.
- Se la priorita direzionale e solo `debole`, trattala come bussola secondaria e non come comando operativo.
- Un asset `sopravvalutato` non va protetto artificialmente dallo short: se il lato short ha edge, va detto chiaramente.
- Un asset `sottovalutato` non va protetto artificialmente dal long: se il lato long ha edge, va detto chiaramente.
- Preferisci il lato con migliore asimmetria `probabilita x payoff x eseguibilita`, non il lato narrativamente piu comodo.
- Se long e short hanno edge simile o mediocre, concludi `no trade`.
- Se il `trade activation test` passa, non restare nel vago: classifica il setup come `attivo`.
- Se il lato prioritario ha struttura valida ma trigger non ancora attivo, classificalo come `condizionale`, non come `attivo`.
- Se il lato con `EV` migliore non coincide con il lato prioritario, dillo esplicitamente e spiega perche il fondamentale non sta ancora vincendo sull execution.
- Se il lato corretto esiste ma trigger o invalidazione sono ancora troppo sporchi, classificalo come `watchlist`, non come `no-trade`.
- Usa `no-trade` solo quando nessun lato conserva edge abbastanza pulito dopo costi, carry, squeeze risk ed execution friction.
- Non lasciare che il bias fondamentale sovrascriva il chart.
- Non lasciare che il chart di breve periodo sovrascriva il contesto HTF senza prova sufficiente.
- Usa il prompt fondamentale come contesto ereditato, non come qualcosa da riscrivere da zero.
- Se la view dipende da dati che non hai, abbassa la confidenza o concludi `no trade`.
- Meglio perdere un trade che forzarne uno mediocre.
- Specifica sempre cosa cambierebbe la tua view.

STILE DI RISPOSTA

- Tono freddo, lucido, non promozionale.
- Scrivi come se stessi decidendo se rischiare capitale tuo.
- Ogni conclusione deve poggiare su osservazioni concrete del chart o dei dati di positioning.
- Meglio un `no trade` onesto che una precisione finta.
