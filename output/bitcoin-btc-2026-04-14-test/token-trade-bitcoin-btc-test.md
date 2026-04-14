# Token Trade: `Bitcoin / BTC`

## Input usato
- `[NOME/TICKER]`: `Bitcoin / BTC`
- Report fondamentale usato:
  - `output/bitcoin-btc-2026-04-14-test/token-research-bitcoin-btc-test.md`
- Report di verifica usato:
  - `output/bitcoin-btc-2026-04-14-test/token-research-bitcoin-btc-verification.md`
- Data snapshot principale: `2026-04-14`
- Fonti market snapshot:
  - `CoinGecko` coin page / market table
  - `CoinGlass` `BTC` overview + `open-interest/BTC`
  - `mempool.space`
  - filing ufficiali `Strategy`
  - `SEC` press releases
  - report fondamentale e report di verifica come contesto ereditato prevalente

---

# Output del prompt

## 0. Market status
- qualita dei chart: `media`
- copertura dati: `parziale`
- fonti principali usate:
  - `CoinGecko`
  - `CoinGlass`
  - `mempool.space`
  - `Strategy 8-K`
  - `SEC`
  - report fondamentale e report di verifica
- fonti tentate ma non ottenute, se rilevanti:
  - non ho ottenuto in questo pass una serie `4H / 1H / 15m` primaria e pulita con OHLC completi
  - non ho ottenuto funding history leggibile e affidabile cross-venue
  - non ho ottenuto una liquidation map vicina e pulita
  - non ho ottenuto borrow cost / short availability spot sufficientemente chiari
  - `TradingView` e stato tentato ma nel pass pubblico mostrava una divergenza troppo ampia sul prezzo spot rispetto a `CoinGecko`, quindi non lo uso come anchor numerica
- timeframe disponibili:
  - `max` come contesto sintetico via `CoinGecko` `ATH / ATL`
  - `1Y` via performance `CoinGecko`
  - `30d`
  - `7d`
  - `24h live range`
  - `1W` solo per proxy da ranges e performance recenti
  - `1D` solo per proxy da ranges e performance recenti
- profondita storica disponibile:
  - `max`: `si, ma in forma sintetica`
  - `1Y`: `si, ma non come serie candle completa in questo pass`
  - `6M`: `solo parziale`
  - `3M`: `no`
  - `monthly candle`: `no`
  - `1W`: `si, ma per proxy`
- report fondamentale disponibile: `si`
- report di verifica disponibile: `si`
- qualita del contesto ereditato: `alta`
- principali buchi informativi:
  - microstruttura intraday reale su `4H / 1H / 15m`
  - funding / basis storici
  - liquidation map vicina
  - lettura precisa del float sugli exchange
- blocchi ancora non osservabili:
  - precisione del trigger intraday
  - crowding di brevissimo periodo
  - qualita di un breakout o breakdown immediato
- confidenza preliminare: `media`

## 1. Recent event e regime evidence log
Ultimi `90d`
- evento: `sequenza di accumulation corporate + backdrop regolatorio USA piu leggibile`
- data:
  - `2026-03-11`
  - `2026-03-17`
  - `2026-03-23`
  - `2026-04-06`
  - `2026-04-13`
- fonte:
  - `SEC`
  - `Strategy 8-K`
  - report di verifica come contesto prevalente
- stato: `confermato`
- cosa e confermato:
  - `SEC` e `CFTC` hanno formalizzato maggiore armonizzazione
  - la `SEC` ha chiarito il perimetro applicativo delle securities laws ai crypto assets
  - `Strategy` ha continuato ad accumulare `BTC` nei filing di marzo e aprile
- cosa resta allegation o non chiuso:
  - l entita esatta del float squeeze
  - il pass-through preciso di questi eventi sul prezzo nel breve
- market reaction osservata:
  - `CoinGecko` live `2026-04-14` mostra:
    - `24h -0.9%`
    - `7d +1.6%`
    - `30d +0.5%`
  - quindi il mercato non tratta questi eventi come shock euforico ancora aperto
- impatto su business / token / market structure / fiducia: `token / market structure / fiducia`
- l evento e chiuso o ancora aperto?: `in evoluzione`
- il setup corrente sembra tecnico o event-driven?: `piu tecnico che event-driven`

Ultimi `30d`
- evento: `flow costruttivo di corporate accumulation e chiarezza regolatoria`
- data:
  - `2026-03-17`
  - `2026-03-23`
  - `2026-04-06`
  - `2026-04-13`
- fonte:
  - `SEC`
  - `Strategy`
- stato: `confermato`
- cosa e confermato:
  - la sequenza `Strategy` degli ultimi `30d` passa da `762,099 BTC` a `780,897 BTC`
  - il backdrop USA appare meno confuso che in molti periodi precedenti
- cosa resta allegation o non chiuso:
  - che questo basti da solo a rompere la parte alta del range
- market reaction osservata:
  - `CoinGecko` mostra un `7d range ~ $67,946.57 - $73,538.49`
  - il prezzo resta dentro un range ordinato, non in price discovery
- impatto su business / token / market structure / fiducia: `market structure / fiducia`
- l evento e chiuso o ancora aperto?: `in evoluzione`
- il setup corrente sembra tecnico o event-driven?: `tecnico con sfondo strutturalmente costruttivo`

Ultimi `7d`
- evento: `Strategy 8-K` del `2026-04-13`
- data: `2026-04-13`
- fonte:
  - `Strategy`
  - `CoinGecko`
  - `CoinGlass`
- stato: `confermato`
- cosa e confermato:
  - `Strategy` acquista `13,927 BTC`
  - holdings dichiarate `780,897 BTC`
  - `BTC` spot live tratta in area `~$70,870 - $70,976` a seconda della dashboard
- cosa resta allegation o non chiuso:
  - quanto del move/hold recente sia spot-driven vs derivati-driven
- market reaction osservata:
  - `CoinGecko` live:
    - `24h range ~ $70,617 - $71,524`
    - `7d +1.6%`
  - `CoinGlass` overview:
    - `24h -1.04%`
    - `7d +2.44%`
    - `OI ~ $51.56B`
  - quindi l evento e rilevante come fiducia / accumulation signal, ma il tape non mostra breakout pulito post-filing
- impatto su business / token / market structure / fiducia: `market structure / fiducia`
- l evento e chiuso o ancora aperto?: `chiuso come filing, aperto come implicazione di domanda`
- il setup corrente sembra tecnico o event-driven?: `prevalentemente tecnico`

Mini verdict
- `evento materiale e ancora aperto`
- impatto principale: `market structure / fiducia`
- stato: `in evoluzione`

## 2. Executive view
- Tesi fondamentale ereditata: `BTC` resta l asset monetario crypto strutturalmente piu forte, con token necessario e supply story eccezionalmente pulita, ma il verdetto fondamentale resta `fairly priced`.
- Coerenza col setup attuale: il contesto strutturale e costruttivo e gli eventi recenti non sono bearish, ma il prezzo oggi non offre ancora una dislocazione evidente o un trigger tecnico pulito.
- investment view: `bullish`
- tactical view: `neutral`
- lato prioritario da cercare: `nessuno`
- forza della priorita direzionale: `nessuna`
- lato con edge maggiore adesso: `long`
- stato del setup tattico: `watchlist`
- perche il lato opposto non e preferito: lo short oggi non ha il supporto di un verdetto fondamentale `sopravvalutato`, non ha un trust shock recente e deve combattere un asset con domanda strutturale ancora credibile.
- migliore espressione investment: `accumulate on major pullbacks`
- migliore espressione tattica: `no trade`
- scenario dominante con probabilita stimata: `chop / digestione nel range 40%`
- timeframe dominante della view: `1D`
- motivo principale: asset forte ma non chiaramente a sconto, prezzo nel mezzo del range recente, microstruttura troppo poco pulita per un attivazione immediata.
- rischio principale contro la view: reclaim rapido sopra `~$71,500` e poi `~$73,500` senza pullback, oppure perdita di `~$70,600` che apre una gamba piu debole verso `~$67,950`.
- grado di eseguibilita: `media`

## 3. Investment / long-term context
Copertura reale del contesto secolare
- `max` disponibile: `si, in forma sintetica via CoinGecko ATH / ATL`
- `1Y`: `si, in forma sintetica`
- `6M`: `parziale`
- `3M`: `no`
- `monthly candle`: `non disponibile`

Osservazioni visibili
- `CoinGecko` live `2026-04-14` mostra:
  - prezzo spot `~$70,869.91`
  - performance `30d +0.5%`
  - performance `1y +16.5%`
  - `ATH ~ $126,080` il `2025-10-06`
- Con prezzo spot `~$70.9k`, `BTC` resta circa `43.8%` sotto ATH.
- Questo e coerente con un asset in:
  - `post-blowoff consolidation`
  - non `price discovery`
  - non `panic regime`
- Il lato strutturale che sostiene il caso investment non arriva dal breve:
  - necessity del token
  - supply hard-capped
  - assenza di unlock discrezionali
  - domanda da balance sheet / treasury
  - ruolo di benchmark collateral / reserve asset crypto

Cosa supporta un caso `HODL multi-quarter / multi-year`
- `BTC` resta il bene monetario crypto con tesi piu semplice e piu difficile da diluire.
- `FDV ~= market cap` e non esiste il rischio classico da foundation / VC unlock.
- La verifica conferma che il `market setup` strutturale resta `favorevole`.
- Il lato corporate / institutional accumulation continua a esistere come driver non banale.

Cosa smentisce o limita un caso `HODL multi-quarter / multi-year`
- `BTC` non distribuisce cash flow all holder passivo.
- Il market cap e gia enorme e il mercato conosce bene la qualita dell asset.
- Una parte grande del prezzo resta funzione di premium monetario e narrative persistence, non di yield.
- Il security budget di lungo periodo resta un tema aperto, anche se non thesis-breaking oggi.

Cosa invalida la tesi investment
- rottura della narrativa `reserve asset`
- trust shock serio su custodia / ETF rails / infrastruttura periferica
- compressione persistente del premium monetario
- perdita di credibilita del lato hard-money / collateral benchmark

Chiusura sezione
- bias `investment / long-term`: `bullish`
- confidenza del caso investment: `media`

## 4. Higher timeframe context
`1W`
- trend primario: `bullish`
- struttura: rimbalzo ordinato dal `7d low ~ $67,946.57` verso la parte mediana del range, ma senza breakout confermato sopra il massimo recente `~$73,538.49`
- regime: `range recovery / continuation attempt`, non `blow-off`
- livelli chiave:
  - `~$67,950` supporto weekly inferiore del tratto recente
  - `~$70,600 - $71,000` pivot / supporto weekly intermedio
  - `~$71,500` prima resistenza
  - `~$73,500` area di offerta weekly
  - `~$75,000 - $78,000` area di estensione solo dopo breakout pulito
- premium o discount rispetto al range HTF: `mid-range`
- dove il chart invalida la tesi HTF:
  - deterioramento netto sotto `~$70,600`
  - peggioramento piu serio sotto `~$67,950`
  - danno piu materiale sotto `~$65,000`

`1D`
- trend primario: `neutral`
- struttura: consolidazione ordinata tra `~$70.6k` e `~$71.5k` dentro un range `7d` ancora piu ampio `~$67.9k - $73.5k`
- regime: `digestione / indecisione`, non impulso pulito
- osservazioni chiave via `CoinGecko` e `CoinGlass`:
  - `CoinGecko` live:
    - `24h -0.9%`
    - `7d +1.6%`
    - `24h range ~ $70,617.48 - $71,524.35`
    - `7d range ~ $67,946.57 - $73,538.49`
  - `CoinGlass` overview:
    - `24h -1.04%`
    - `7d +2.44%`
- livelli chiave:
  - `~$70,600`
  - `~$71,500`
  - `~$67,950`
  - `~$73,500`
- premium o discount rispetto al range HTF: `centro del range`
- dove il chart invalida la tesi `1D`:
  - close daily sotto `~$70,600`
  - peggioramento piu netto sotto `~$67,950`

Chiusura sezione
- bias `1W`: `bullish`
- bias `1D`: `neutral`

## 5. Mid timeframe structure
Osservazioni `4H`
- Non ho ottenuto una serie `4H` primaria pulita in questo pass, quindi non dichiaro pattern intraday che non posso vedere.
- Il proxy piu onesto e:
  - prezzo live `~$70,870 - $70,976`
  - supporto immediato in area `~$70,600 - $71,000`
  - massimo 24h `~$71,524`
  - massimo 7d `~$73,538`
- La struttura intermedia leggibile per proxy sembra una `compressione / attesa`, non un breakout gia maturo e neppure un breakdown gia confermato.
- Il momentum non e bearish in modo forte.
- Il problema e la pulizia del trigger, non la liquidita del mercato.

Conflitto o allineamento con HTF
- Il `4H proxy` resta allineato al `1W` costruttivo.
- Il conflitto e soprattutto con il `1D`, che oggi appare piu da range che da trend.
- Quindi:
  - contesto grande buono
  - execution di breve ancora mediocre

Dove si invalida la tesi su timeframe medio
- per una lettura costruttiva: ritorno sotto `~$70,600`
- per una lettura di deterioramento piu serio: perdita di `~$67,950`
- per riattivare continuation pulita: reclaim di `~$71,500` e poi acceptance sopra `~$73,500`

## 6. Lower timeframe timing
Osservazioni `1H`
- Non ho una lettura `1H` sufficientemente pulita da chiamare `trigger attivo`.
- Di conseguenza non tratto il move corrente come breakout confermato gia eseguibile.

Osservazioni `15m`
- Anche il `15m` non e osservabile con rigore sufficiente in questo pass.
- Questo abbassa soprattutto la precisione del timing, non la lettura direzionale di contesto.

Trigger di entrata possibili
- long solo:
  - su pullback difeso in area `~$70,600 - $71,000`
  - oppure su reclaim di `~$71,500`
  - con conferma piu forte se poi arriva acceptance sopra `~$73,500`
- short solo:
  - su failed reclaim dell area `~$71,500`
  - oppure su breakdown sotto `~$70,600` con mancato reclaim
  - oppure su spike respinto vicino a `~$73,500`

Conferme richieste
- per il long:
  - tenuta chiara del blocco `~$70,600 - $71,000`
  - oppure reclaim di `~$71,500` senza rapido riassorbimento
  - meglio ancora acceptance sopra `~$73,500`
- per lo short:
  - rejection pulita di `~$71,500` o `~$73,500`
  - oppure close debole sotto `~$70,600` con retest fallito

Rischio di chase
- `medio-alto` sul long a prezzo corrente
- `medio-alto` sullo short, perche manca un catalyst bearish serio

Rischio di fake breakout / fake breakdown
- `medio`
- piu alto del normale per la mancanza di una lettura intraday precisa

Timing migliore
- `aspettare`
- long `su pullback` o `su reclaim`
- short solo `su failed reclaim` o `su breakdown`

## 7. Derivatives e positioning
Fatti verificabili
- `CoinGlass` overview `2026-04-14`:
  - prezzo live `~$70,975.67`
  - futures volume 24h `~$42.45B`
  - spot volume 24h `~$2.99B`
  - open interest `~$51.56B`
  - liquidazioni futures 24h `~$36.04M`
  - `24h -1.04%`
  - `7d +2.44%`
- `CoinGecko` live `2026-04-14`:
  - spot volume globale 24h `~$28.10B`
  - market cap `~$1.4186T`
- ratio utili:
  - `OI / market cap ~3.63%`
  - `futures volume / CoinGecko spot volume ~1.51x`
- `CoinGlass open-interest/BTC` conferma che l `OI` su BTC e molto materiale, ma non mi da in questo pass un funding snapshot leggibile abbastanza da usarlo come trigger

Dati mancanti
- funding live leggibile e affidabile
- basis storica
- long/short crowding pulito cross-venue
- borrow cost
- short availability
- liquidation map vicina

Inferenze operative
- Il mercato derivati su `BTC` e molto grande, ma non in modo anomalo rispetto alla scala dell asset.
- `OI ~3.6%` della market cap segnala leva materiale ma non necessariamente crowding terminale.
- Il rapporto futures / spot segnala un asset molto giocato dai derivati, quindi sensibile a flush e squeeze.
- Il positioning quindi:
  - non conferma uno short facile
  - non regala neppure un long aggressivo di continuation

Conclusione operativa
- il positioning `non contraddice` la struttura costruttiva
- ma `non la conferma` abbastanza da trasformare il long in trade attivo
- squeeze risk e flush risk restano entrambi reali
- carry: `non valutabile con precisione sufficiente`

## 8. Liquidity e execution quality
Fatti verificabili
- `CoinGecko` market table `2026-04-14` mostra spot book profondi e spread stretti:
  - `Coinbase Exchange BTC/USD`:
    - spread `0.01%`
    - `+2% depth ~ $18.79M`
    - `-2% depth ~ $21.47M`
  - `Binance BTC/USDT`:
    - spread `0.01%`
    - `+2% depth ~ $14.54M`
    - `-2% depth ~ $19.32M`
  - `Kraken BTC/USD`:
    - spread `0.01%`
    - `+2% depth ~ $18.11M`
    - `-2% depth ~ $20.24M`
- `CoinGecko` live mostra volume spot globale 24h `~$28.10B`
- `CoinGlass` live mostra futures volume 24h `~$42.45B` e `OI ~ $51.56B`

Inferenze operative
- La liquidita di `BTC` e reale, profonda e multi-venue.
- Questo e un asset eseguibile molto bene; il problema non e la frizione, ma il fatto che il prezzo oggi non stia offrendo ancora un edge pulito.
- Una size sensata puo entrare e uscire senza attrito anomalo sulle venue maggiori.
- La view quindi e `eseguibile`, ma l execution quality alta non trasforma automaticamente un setup mediocre in buon trade.

Domande chiave
- la view e eseguibile bene oppure solo teorica?
  - `eseguibile bene`
- una size sensata puo entrare e uscire senza troppo attrito?
  - `si`
- il mercato e abbastanza profondo per sostenere la tesi?
  - `si`

## 8A. Directional symmetry test
- lato prioritario da cercare derivato dal fondamentale: `nessuno`
- gate priorita direzionale:
  - `gate 1 - verdict`: `no`
  - `gate 2 - confidenza`: `si`
  - `gate 3 - copertura dati`: `si`
  - `gate 4 - regime`: `si`
- forza della priorita direzionale: `nessuna`

Miglior caso `long` disponibile adesso
- pullback ordinato e difeso in area `~$70,600 - $71,000`
- oppure reclaim di `~$71,500`
- con seconda gamba solo se poi arriva acceptance sopra `~$73,500`
- e un long coerente con:
  - `investment view` bullish
  - struttura weekly ancora costruttiva
  - assenza di catalyst bearish recente

Miglior caso `short` disponibile adesso
- failed reclaim in area `~$71,500`
- oppure spike respinto in area `~$73,500`
- oppure breakdown sotto `~$70,600` e poi `~$67,950`
- e uno short tattico di range / failure, non uno short supportato da priorita fondamentale

Quale lato ha l asimmetria migliore
- `long`, ma solo in forma condizionata da prezzo migliore o reclaim pulito

Quale lato ha l execution migliore
- `long`
- perche si muove a favore di:
  - struttura grande
  - liquidita
  - contesto fondamentale non bearish

Perche il lato opposto e inferiore
- Lo short non ha il supporto di un verdetto `sopravvalutato`.
- Combatte un asset con:
  - qualita strutturale alta
  - eventi recenti non negativi
  - demand narrative ancora viva
- Ha senso solo come trade tattico di failure, non come lato da cercare per primo.

Differenza tra `tesi corretta` e `trade con edge`
- La tesi corretta oggi non e `BTC va shortato`.
- Non e neppure `BTC va comprato a mercato senza aspettare`.
- La tesi corretta e: asset strutturalmente forte, prezzo non chiaramente cheap, struttura di breve da range, timing immediato mediocre.
- Quindi il lato con edge potenziale puo essere `long`, ma il trade adesso resta ancora da costruire.

Se il fondamentale e `fairly priced`
- non esiste una priorita automatica
- il lato da cercare diventa quello con migliore combinazione di struttura, execution e prezzo
- oggi questo favorisce il `long` come lato da monitorare, non come market order immediato

## 9. Investment / HODL case
- espressione investment: `accumulate on major pullbacks`
- orizzonte dominante: `multi-quarter / multi-year`
- timeframe usato per la tesi investment: `max / 1Y / 30d`
- coerenza con la tesi fondamentale: `coerente`
- cosa rende sensato il caso investment:
  - token necessario
  - supply hard-capped
  - assenza di dilution discrezionale
  - role as reserve / benchmark collateral asset
  - contesto di accumulation corporate ancora presente
- cosa lo invalida:
  - rottura della narrativa `reserve asset`
  - trust shock periferico serio
  - compressione persistente del premium monetario
- cosa migliorerebbe la tesi:
  - drawdown verso supporti migliori
  - prosecuzione credibile dell assorbimento da balance sheet
  - tenuta del market structure nonostante leva alta
- cosa la peggiorerebbe:
  - rallentamento netto dei grandi compratori
  - perdita di `~$67,950`
  - regime piu aggressivamente risk-off senza nuova domanda strutturale

## 10. Spot / positional case
- espressione spot: `hold if already in`
- tipo di caso: `positional multi-week / multi-month`
- timeframe usato per la tesi spot: `1W / 1D / 4H proxy`
- coerenza con la tesi fondamentale: `parzialmente coerente`
- cosa rende sensato il caso spot:
  - struttura grande ancora costruttiva
  - nessun thesis-break recente
  - liquidita molto profonda
  - backdrop regolatorio e corporate non negativo
- cosa lo invalida:
  - perdita di `~$70,600`
  - peggioramento piu deciso sotto `~$67,950`
- cosa migliorerebbe la tesi:
  - pullback pulito su supporto
  - reclaim di `~$71,500`
  - acceptance sopra `~$73,500`
- cosa la peggiorerebbe:
  - failed reclaim di `~$71,500`
  - breakdown sotto `~$70,600`

## 11. Swing long case
- trigger long:
  - pullback difeso in area `~$70,600 - $71,000`
  - oppure reclaim di `~$71,500`
  - con seconda conferma solo dopo acceptance sopra `~$73,500`
- livello o zona di entrata:
  - `~$70,600 - $71,100` su tenuta del pullback
  - `~$71,500 - $71,900` su reclaim confermato
- invalidazione:
  - sotto `~$67,700 - $67,950` per il long su pullback
  - ritorno deciso sotto `~$70,600` per il long di reclaim
- primi target:
  - `~$71,500`
  - `~$73,500`
  - estensione solo dopo acceptance piu pulita verso `~$75,000 - $78,000`
- timeframe dominante: `1D / 4H proxy`
- stato del case: `watchlist`
- condizione che trasformerebbe il long in no trade:
  - perdita di `~$70,600`
  - oppure reclaim sporco subito riassorbito sotto `~$70,600`

## 12. Swing short case
- trigger short:
  - failed reclaim in area `~$71,500`
  - oppure rejection piu alta in area `~$73,500`
  - oppure breakdown sotto `~$70,600` con mancato reclaim
- livello o zona di entrata:
  - `~$71,300 - $71,800` se il reclaim fallisce
  - `~$73,300 - $73,800` se il breakout alto fallisce
  - retest fallito di `~$70,600` dopo breakdown
- invalidazione:
  - acceptance sopra `~$72,000` sullo short da failed reclaim basso
  - acceptance sopra `~$74,000 - $74,500` sullo short da failed breakout alto
  - ritorno sopra `~$71,000` sullo short da breakdown
- primi target:
  - `~$70,600`
  - `~$67,950`
  - estensione solo se il mercato apre una gamba piu debole verso `~$65,000`
- timeframe dominante: `1D / 4H proxy`
- stato del case: `watchlist`
- condizione che trasformerebbe lo short in no trade:
  - mercato che tiene sopra `~$71,500`
  - oppure acceptance sopra `~$73,500`

## 13. Probabilistic scenario map
- timeframe comune della scenario map: `1D` nei prossimi `3-10` giorni

Scenario `1`: `chop / digestione nel range`
- probabilita stimata: `40%`
- trigger / condizione:
  - il prezzo tiene `~$70,600`
  - ma non rompe in modo pulito `~$71,500` e `~$73,500`
- path di prezzo atteso:
  - oscillazione tra `~$68,000` e `~$73,500`
- lato favorito: `nessuno`
- migliore espressione: `no trade`
- invalidazione dello scenario:
  - reclaim confermato sopra `~$71,500` e poi `~$73,500`
  - breakdown sotto `~$67,950`

Scenario `2`: `continuation bullish`
- probabilita stimata: `35%`
- trigger / condizione:
  - reclaim di `~$71,500`
  - poi acceptance sopra `~$73,500`
- path di prezzo atteso:
  - test di `~$75,000`
  - possibile estensione verso `~$78,000`
- lato favorito: `long`
- migliore espressione: `swing long`
- invalidazione dello scenario:
  - ritorno sotto `~$70,600`

Scenario `3`: `reversion / breakdown bearish`
- probabilita stimata: `25%`
- trigger / condizione:
  - perdita di `~$70,600`
  - poi mancato recupero di `~$70,600 - $71,000`
- path di prezzo atteso:
  - ritorno su `~$67,950`
  - possibile test di `~$65,000`
- lato favorito: `short`
- migliore espressione: `swing short`
- invalidazione dello scenario:
  - reclaim veloce sopra `~$71,500`

Chiusura sezione
- scenario dominante: `chop / digestione nel range 40%`
- scenario piu pericoloso contro la tua view: `reversion / breakdown bearish 25%`
- lato con `EV` migliore adesso: `long`

## 14. Trade activation test
- qual e il lato con `EV` migliore adesso / candidato all attivazione: `long`
- questo lato coincide con il lato prioritario oppure no?: `no`
- il lato candidato all attivazione ha un trigger attivo adesso?: `no`
- l invalidazione e chiara e abbastanza vicina da rendere il trade disciplinabile?: `no`
- l eseguibilita e almeno `media`?: `si`
- spread, slippage, carry o squeeze risk stanno ancora sabotando il setup?: `no, non in modo decisivo`
- un evento aperto impedisce ancora di trattare il prezzo come base affidabile?: `no`

Chiusura sezione
- stato del setup tattico: `watchlist`
- motivo del lato candidato all attivazione:
  - la struttura grande favorisce piu un long su prezzo migliore o reclaim pulito che uno short di convinzione
- motivo principale della classificazione:
  - esiste una direzione plausibile, ma senza trigger attivo e senza microstruttura intraday pulita l ingresso immediato resta poco disciplinabile

## 15. No-trade test
- il setup e troppo sporco?: `no`
- il risk/reward e insufficiente?: `si, a prezzo corrente`
- la liquidita o il positioning peggiorano troppo l esecuzione?: `no`
- la view e piu teorica che praticabile?: `si, sul timing immediato`
- un evento ancora aperto rende il prezzo non affidabile come base operativa?: `no`
- aspettare darebbe un setup migliore?: `si`
- uno dei due lati ha davvero edge probabilistico netto dopo costi e carry?: `no, non ancora`

Conclusione secca
- Non e `no-trade` in senso pieno.
- E `watchlist`, perche il lato long resta il piu interessante da monitorare ma non e ancora abbastanza pulito da attivare.

## 16. Decisione finale
- verdict fondamentale ereditato: `fairly priced`
- stato evento/regime: `in evoluzione`
- bias investment / long-term: `bullish`
- bias 1W: `bullish`
- bias 1D: `neutral`
- bias operativo: `neutral`
- lato prioritario da cercare: `nessuno`
- forza della priorita direzionale: `nessuna`
- lato con edge maggiore adesso: `long`
- lato candidato all attivazione: `long`
- stato del setup tattico: `watchlist`
- migliore espressione investment: `accumulate on major pullbacks`
- migliore espressione tattica: `no trade`
- scenario dominante con probabilita stimata: `chop / digestione nel range 40%`
- timeframe dominante della tesi: `1D`
- orizzonte holding implicito: `swing multi-day`
- coerenza con la tesi fondamentale: `parzialmente coerente`
- conviction: `bassa`
- eseguibilita: `media`
- invalidation della tesi:
  - perdita di `~$70,600`
  - deterioramento piu serio sotto `~$67,950`
- se spot: logica di accumulo o di hold:
  - `accumulo solo su pullback importante`
  - `se gia in posizione, hold disciplinato finche il blocco ~70,600 / 67,950 non cede`
- se swing: entry logic / invalidation / target logic:
  - `entry`: pullback difeso `~$70,600 - $71,000` oppure reclaim di `~$71,500`
  - `invalidation`: sotto `~$67,700 - $67,950` sul pullback long, oppure ritorno sotto `~$70,600` sul reclaim long
  - `target`: `~$71,500`, poi `~$73,500`, poi eventuale estensione `~$75,000 - $78,000`
- motivo principale del verdetto:
  - `BTC` resta l asset monetario crypto strutturalmente piu forte, ma il fondamentale non offre una priorita direzionale perche il token non appare chiaramente a sconto.
  - Il backdrop recente e costruttivo, ma il prezzo attuale tratta ancora piu da range che da breakout affidabile.
  - La risposta disciplinata oggi non e inseguire ne shortare a caso, ma aspettare un pullback o un reclaim migliore e trattare il setup come `watchlist`.
