# Token Trade: `Bitcoin / BTC`

## 0. Market status
- qualita dei chart: `alta`
- copertura dati: `parziale`
- fonti principali usate:
  - `Kraken Spot API` per `spot anchor` e OHLC `max / monthly / 1W / 1D / 4H / 1H / 15m`
  - `Binance Futures API` per `perp anchor`, funding, open interest e near-book depth
  - report fondamentale `token-research-bitcoin-btc-test.md`
  - report di verifica `token-research-bitcoin-btc-verification.md`
- fonti tentate ma non ottenute, se rilevanti:
  - non ho una liquidation map primaria completa e same-timestamp
  - non ho basis e borrow cost cross-venue puliti nello stesso snapshot
- `spot anchor principale` usato + timestamp:
  - `Kraken Spot` ticker fetch same-day `2026-04-14`
  - last trade osservata: `~$74,392.90`
  - cross-check OHLC live spot su candle corrente: `~$74.39k`
- `perp anchor principale` usato + timestamp:
  - `Binance Futures BTCUSDT premiumIndex`
  - timestamp API: `2026-04-14T12:41:26Z`
  - mark price: `$74,369.95`
  - index price: `$74,402.98`
  - last funding rate: `0.00003134` (`~0.0031%`, leggermente positivo)
  - next funding: `2026-04-14T16:00:00Z`
- timeframe disponibili:
  - `max` tramite weekly history Kraken dal `2013`
  - `monthly candle`
  - `1W`
  - `1D`
  - `4H`
  - `1H`
  - `15m`
- profondita storica disponibile:
  - `max`: `si`
  - `1Y`: `si`
  - `6M`: `si`
  - `3M`: `si`
  - `monthly candle`: `si`
  - `1W`: `si`
- report fondamentale disponibile: `si`
- report di verifica disponibile: `si`
- qualita del contesto ereditato: `alta`
- principali buchi informativi:
  - niente liquidation heatmap primaria completa
  - niente borrow cost / short availability cross-venue
  - open interest primario su singola venue, non su tutto il complesso derivati
- blocchi ancora non osservabili:
  - carry completo cross-venue
  - basis curva completa
  - cluster di liquidazioni aggregati
- note di riconciliazione se le fonti market divergono materialmente:
  - `Kraken Spot` e `Binance perp` sono coerenti entro pochi basis points nello snapshot operativo
  - il report di verifica ha gia mostrato che `CoinGlass` e utile per contesto derivati aggregato, ma troppo live per diventare anchor finale dei livelli
- confidenza preliminare: `media`

## 1. Recent event e regime evidence log
- `2026-04-13`
  - evento: `CoinShares Digital Asset Fund Flows`
  - fonte: `CoinShares`
  - stato: `confermato`
  - cosa e confermato: inflows settimanali digital asset `~$1.1B`, Bitcoin `~$871M`
  - cosa resta allegation o non chiuso: nulla di materiale oltre all interpretazione sul follow-through dei flussi
  - market reaction osservata: recupero settimanale del prezzo e rafforzamento del tono risk-on su BTC
  - impatto su business / token / market structure / fiducia: `market structure / fiducia`
  - l evento e chiuso o ancora aperto?: `aperto come tema, non come shock`
  - il setup corrente sembra tecnico o event-driven?: `piu tecnico che event-driven`
- `2026-04-13`
  - evento: `Strategy 8-K`
  - fonte: `Strategy`
  - stato: `confermato`
  - cosa e confermato: ulteriori `13,927 BTC` acquistati; holdings totali `780,897 BTC`
  - cosa resta allegation o non chiuso: nulla di strutturalmente opaco sul filing
  - market reaction osservata: supporto alla narrativa di corporate absorption del float
  - impatto su business / token / market structure / fiducia: `market structure / narrativa`
  - l evento e chiuso o ancora aperto?: `aperto come tema`
  - il setup corrente sembra tecnico o event-driven?: `event tailwind, ma non shock aperto`
- `2026-03-25`
  - evento: `CoinShares Bitcoin Mining Report Q1 2026`
  - fonte: `CoinShares`
  - stato: `confermato`
  - cosa e confermato: fee income ancora sotto l `1%` del total block reward nel periodo discusso; hashprice compresso
  - cosa resta allegation o non chiuso: la velocita con cui il fee market maturera nel lungo periodo
  - market reaction osservata: piu pressione sul miner complex che shock diretto sul price action di BTC
  - impatto su business / token / market structure / fiducia: `business / token`
  - l evento e chiuso o ancora aperto?: `aperto come tema strutturale, non come tape shock`
  - il setup corrente sembra tecnico o event-driven?: `tecnico`
- `2026-01-05` e `2026-01-10`
  - evento: `wallet migration bug` e rilascio `30.2`
  - fonte: `Bitcoin Core`
  - stato: `confermato`
  - cosa e confermato: bug wallet reale, poi fix e release management
  - cosa resta allegation o non chiuso: nessun consensus break confermato
  - market reaction osservata: evento chiuso, non dominante sul tape attuale
  - impatto su business / token / market structure / fiducia: `fiducia / software operations`
  - l evento e chiuso o ancora aperto?: `chiuso`
  - il setup corrente sembra tecnico o event-driven?: `tecnico`

Mini verdict
- `nessun evento materiale aperto`
- impatto principale: `market structure`
- stato: `chiuso / in evoluzione solo come tema di flusso`

## 2. Executive view
- tesi fondamentale ereditata: `BTC` e asset di qualita alta ma `fairly priced`; nessuna priorita direzionale strutturale forte dal fondamentale
- coerenza rispetto al setup attuale: il chart non contraddice il fondamentale; mostra una ricostruzione tecnica solida, non uno squeeze irrazionale contro tesi
- investment view: `bullish`
- tactical view: `neutral`
- lato prioritario da cercare: `nessuno`
- forza della priorita direzionale: `nessuna`
- lato con edge maggiore adesso: `long`
- stato del setup tattico: `condizionale`
- perche il lato opposto non e preferito: shortare un `1W / 1D` in recovery con funding solo lievemente positivo e senza event shock aperto e inferiore finche `74k` non cede in modo pulito
- migliore espressione investment: `HODL if already in`
- migliore espressione tattica: `swing long`
- scenario dominante con probabilita stimata: `continuation bullish`, `40%`
- timeframe dominante della view: `1D -> 4H`
- motivo principale: trend settimanale e giornaliero in riallineamento rialzista, ma entrata tattica ancora da attivare
- rischio principale contro la view: fallimento sotto `74k` con breakdown verso il blocco `73k / 71.7k`
- grado di eseguibilita: `alta`

## 3. Investment / long-term context
Fatti osservabili:
- storico `max` disponibile via weekly candles Kraken dal `2013`
- ATH osservabile nella serie: `~$126,198.10`
- prezzo operativo corrente: `~$74.39k`
- distanza dall ATH: `~-41.1%`
- close settimanale di circa `52` settimane fa: `~$84.0k`
- prezzo attuale vs close di un anno fa: `~-11.5%`
- monthly candle corrente:
  - open `~$68.86k`
  - high `~$74.97k`
  - low `~$67.73k`
  - close live `~$74.39k`
- monthly candle precedente:
  - open `~$67.86k`
  - high `~$71.99k`
  - low `~$64.96k`
  - close `~$68.86k`

Lettura:
- Il regime secolare non appare `blow-off`; appare piu `ricostruzione dentro un bull di lungo periodo`.
- Il drawdown dal massimo resta pesante, ma il prezzo sta ricostruendo sopra il minimo rilevante degli ultimi `90d` in area `~$60.5k`.
- La lettura investment resta positiva perche:
  - il caso strutturale di Bitcoin non e stato invalidato
  - il prezzo non e in euforia secolare tipo nuovo ATH
  - il monthly sta migliorando dopo un trimestre debole
- La lettura investment non implica `compra adesso a qualunque prezzo`; implica che il caso multi-quarter resta vivo.

Cosa supporta un caso `HODL`
- qualita fondamentale alta e verificata
- hard cap e structure di supply eccezionale
- prezzo ancora sotto ATH e dentro una fase di recovery, non di parabola finale

Cosa smentisce o peggiora il caso `HODL`
- ritorno sotto il pivot macro `~$60.5k`
- deterioramento serio della narrativa di reserve asset o shock su custody / regolazione / market access

Chiusura sezione
- bias `investment / long-term`: `bullish`
- confidenza del caso investment: `media`

## 4. Higher timeframe context
`1W`
- trend primario: `bullish`
- struttura: `HH / HL` nelle ultime settimane osservabili
- current week live:
  - open `~$71.09k`
  - high `~$74.97k`
  - low `~$70.47k`
  - close live `~$74.39k`
- previous week:
  - open `~$68.10k`
  - high `~$72.85k`
  - low `~$65.69k`
  - close `~$71.11k`
- livelli chiave `1W`:
  - resistenza: `~$75.0k`, poi `~$76.0k`
  - supporto: `~$70.5k`, poi `~$65.0k`

`1D`
- trend primario: `bullish`, ma dopo una gamba rapida
- struttura: range expansion rialzista seguita da consolidazione vicino ai massimi del giorno precedente
- current day live:
  - open `~$74.44k`
  - high `~$74.95k`
  - low `~$74.03k`
  - close live `~$74.39k`
- previous day:
  - open `~$70.75k`
  - high `~$74.97k`
  - low `~$70.60k`
  - close `~$74.44k`
- livelli chiave `1D`:
  - breakout line: `~$74.95k / $75.0k`
  - supporto vicino: `~$74.0k`
  - supporto successivo: `~$73.0k`
  - resistenza successiva: `~$75.998k` circa `30D high`

Chiusura sezione
- bias `1W`: `bullish`
- bias `1D`: `bullish`

## 5. Mid timeframe structure
- Il `4H` e in `continuation / consolidazione alta`, non in breakdown.
- Sequenza recente `4H`:
  - impulso da `~$70.8k` a `~$72.5k`
  - secondo impulso a `~$73.5k`
  - terzo impulso a `~$74.97k`
  - poi digestione sopra `~$74.0k`
- Ultimi blocchi `4H` osservabili:
  - high locale: `~$74.97k`
  - supporto locale: `~$74.03k`
  - supporto intermedio piu pulito: `~$73.04k`
  - supporto inferiore successivo: `~$71.73k`
- Il `4H` resta allineato con `1W / 1D`, ma il rischio di chase e alto perche il prezzo sta consolidando sotto breakout.
- Invalidation della tesi `4H`:
  - perdita netta dell area `~$74.0k`
  - e soprattutto conferma di perdita del blocco `~$73.0k`

## 6. Lower timeframe timing
- `1H` e `15m` mostrano compressione, non trigger gia attivo.
- Ultime `8` candele `1H`:
  - high: `~$74.95k`
  - low: `~$74.20k`
- Ultime `32` candele `15m`:
  - high: `~$74.95k`
  - low: `~$74.20k`
- Lettura timing:
  - il long non va inseguito nel mezzo del box `~$74.2k - $75.0k`
  - il long migliora su:
    - reclaim / acceptance sopra `~$75.0k`
    - oppure pullback controllato in `~$74.0k - $74.2k` seguito da reazione pulita
  - lo short migliora solo su perdita confermata di `~$74.0k` e failure to reclaim
- timing migliore:
  - `su reclaim` per il long breakout
  - `su pullback` per il long di supporto
  - `su breakdown` solo per lo short
  - `aspettare` nel mezzo del range

## 7. Derivatives e positioning
- `Binance Futures` `2026-04-14T12:41:26Z`
  - mark price: `$74,369.95`
  - index price: `$74,402.98`
  - last funding rate: `0.00003134`
  - lettura funding: `lievemente positiva`, non estrema
  - next funding: `2026-04-14T16:00:00Z`
- `Binance Futures` `openInterest`
  - raw OI: `95,809.250`
  - nota: e dato primario di singola venue, non aggregato cross-venue
- `CoinGlass` context ereditato dalla verifica same-day:
  - OI aggregato `~$57.03B`
  - futures volume 24h `~$82.07B`
- Lettura positioning:
  - non vedo un crowding long tossico tipo funding fortemente estremo
  - l OI resta alto abbastanza da amplificare moves se il box `74k / 75k` si rompe
  - il carry non sabota il long, ma non regala nemmeno uno squeeze short meccanico evidente

Conclusione sezione
- il positioning `non contraddice` il caso long
- il rischio principale e un flush rapido di leva se `74k` salta

## 8. Liquidity e execution quality
- `Binance Futures depth` snapshot same-day:
  - best bid `74367.90`
  - best ask `74368.00`
  - spread osservato: `~$0.10`
- `Kraken Spot` e `Binance Futures` sono entrambi profondi e puliti per BTC.
- L eseguibilita reale di `BTC` e alta:
  - spread minimo
  - venue di qualita alta
  - attrito basso per size sensata
- Livelli magnete piu ovvi:
  - `~$75.0k` come breakout / stop magnet
  - `~$74.0k` come supporto decisionale
  - `~$73.0k` come next downside acceptance zone

Conclusione sezione
- la view e eseguibile bene, non solo teorica
- una size sensata puo entrare e uscire con attrito basso

## 8A. Directional symmetry test
- lato prioritario da cercare derivato dal fondamentale: `nessuno`
- forza della priorita direzionale: `nessuna`
- miglior caso `long` disponibile adesso:
  - continuation di un `1W / 1D` gia riallineato al rialzo
  - breakout sopra `~$75.0k` verso `~$76.0k` e poi `~$78.0k`
  - funding non punitivo e execution ottima
- miglior caso `short` disponibile adesso:
  - failure sotto `~$74.0k` e poi accelerazione verso `~$73.0k / $71.7k`
  - sarebbe trade di breakdown, non short da valutazione
- quale lato ha l asimmetria migliore: `long`
- quale lato ha l execution migliore: `pari`, ma il long ha contesto migliore
- perche il lato opposto e inferiore:
  - shortare qui significa andare contro `1W / 1D` senza funding o euforia abbastanza estremi da compensare
- differenza tra `tesi corretta` e `trade con edge`:
  - tesi corretta: Bitcoin resta forte ma non structural cheap
  - trade con edge: solo il lato che rompe il box con trigger pulito
- conclusione della simmetria:
  - `long` vince non perche il fondamentale lo impone, ma perche il chart lo rende il lato operativo migliore se scatta il trigger

## 9. Investment / HODL case
- espressione investment: `HODL if already in`
- orizzonte dominante: `multi-quarter / multi-year`
- timeframe usato per la tesi investment: `max / 1Y / 6M / 3M / monthly candle`
- coerenza con la tesi fondamentale: `coerente`
- cosa rende sensato il caso investment:
  - asset strutturalmente forte
  - monthly in miglioramento
  - prezzo ancora molto sotto ATH, quindi non in blow-off
- cosa lo invalida:
  - perdita del pivot macro `~$60.5k`
  - shock strutturale che rompa la narrativa di reserve asset
- cosa migliorerebbe la tesi:
  - consolidamento sopra `~$75k`
  - prosecuzione dei flussi istituzionali
- cosa la peggiorerebbe:
  - failure multi-month e ritorno sotto il blocco `65k / 60.5k`

## 10. Spot / positional case
- espressione spot: `hold if already in`
- tipo di caso: `positional multi-week / multi-month`
- timeframe usato per la tesi spot: `1W / 1D / 4H`
- coerenza con la tesi fondamentale: `coerente`
- cosa rende sensato il caso spot:
  - `1W` e `1D` sono rialzisti
  - il prezzo ha gia rimesso in piedi una sequenza di rialzo
- cosa lo invalida:
  - perdita di `~$74.0k` seguita da accettazione sotto `~$73.0k`
- cosa migliorerebbe la tesi:
  - breakout e tenuta sopra `~$75.0k`
- cosa la peggiorerebbe:
  - rejection multipla su `~$75.0k` con funding in salita e prezzo che torna nel range

## 11. Swing long case
- trigger long:
  - `1H close` sopra `~$75.0k`
  - oppure pullback in `~$74.0k - $74.2k` con reclaim pulito e tenuta
- livello o zona di entrata:
  - breakout entry `~$75.0k - $75.2k`
  - support entry solo se il pullback viene assorbito senza perdere `~$74.0k`
- invalidazione:
  - ritorno sotto `~$74.2k` per il breakout trade
  - sotto `~$73.8k` per il support trade
- primi target:
  - `~$75.998k`
  - poi `~$77.5k - $78.0k`
- timeframe dominante: `1D -> 4H -> 1H`
- stato del case: `condizionale`
- condizione che trasformerebbe il long in no trade:
  - break marginale sopra `~$75k` senza acceptance e con immediato rientro nel box

## 12. Swing short case
- trigger short:
  - perdita di `~$74.0k` con failure to reclaim su `1H`
  - conferma piu forte se il prezzo perde anche il blocco `~$73.0k`
- livello o zona di entrata:
  - `~$73.9k - $74.1k` su breakdown / failed reclaim
- invalidazione:
  - ritorno sopra `~$74.95k / $75.0k`
- primi target:
  - `~$73.0k`
  - poi `~$71.7k`
- timeframe dominante: `4H -> 1H`
- stato del case: `watchlist`
- condizione che trasformerebbe lo short in no trade:
  - funding che resta contenuto e prezzo che continua a difendere `~$74k` senza breakdown

## 13. Probabilistic scenario map
- timeframe comune della scenario map: `1D / 4H`
- scenario `1`: `continuation bullish`
  - probabilita stimata: `40%`
  - trigger / condizione: `1H` e poi `4H` acceptance sopra `~$75.0k`
  - path di prezzo atteso: `~$75.0k -> $76.0k -> $77.5k / $78.0k`
  - lato favorito: `long`
  - migliore espressione: `swing long`
  - invalidazione dello scenario: failure immediata sotto `~$74.2k`
- scenario `2`: `chop / nessuna risoluzione`
  - probabilita stimata: `35%`
  - trigger / condizione: permanenza dentro il box `~$74.0k - $75.0k`
  - path di prezzo atteso: range e falsa rottura da entrambi i lati
  - lato favorito: `nessuno`
  - migliore espressione: `no trade / spot hold`
  - invalidazione dello scenario: breakout confermato o breakdown confermato
- scenario `3`: `reversion / breakdown bearish`
  - probabilita stimata: `25%`
  - trigger / condizione: perdita di `~$74.0k` e failure to reclaim
  - path di prezzo atteso: `~$74.0k -> $73.0k -> $71.7k`
  - lato favorito: `short`
  - migliore espressione: `swing short`
  - invalidazione dello scenario: recupero veloce sopra `~$75.0k`

Chiusura sezione
- scenario dominante: `continuation bullish`
- scenario piu pericoloso contro la view: `breakdown bearish sotto $74k`
- lato con `EV` migliore adesso: `long`

## 14. Trade activation test
- qual e il lato con `EV` migliore adesso / candidato all attivazione: `long`
- questo lato coincide con il lato prioritario oppure no?: `no`, perche il fondamentale non da priorita strutturale
- il lato candidato all attivazione ha un trigger attivo adesso?: `no`
- l invalidazione e chiara e abbastanza vicina da rendere il trade disciplinabile?: `si`
- l eseguibilita e almeno `media`?: `si`, `alta`
- spread, slippage, carry o squeeze risk stanno ancora sabotando il setup?: `no`
- un evento aperto impedisce ancora di trattare il prezzo come base affidabile?: `no`

Chiusura sezione
- stato del setup tattico: `condizionale`
- motivo del lato candidato all attivazione:
  - allineamento `1W / 1D / 4H` ancora costruttivo
  - funding non estremo
  - execution ottima
- motivo principale della classificazione:
  - il lato giusto c e, ma il trigger non e ancora attivo mentre il prezzo resta nel mezzo-alto del box

## 15. No-trade test
- il setup e troppo sporco?: `no`
- il risk/reward e insufficiente?: `solo se inseguito dentro il box`
- la liquidita o il positioning peggiorano troppo l esecuzione?: `no`
- la view e piu teorica che praticabile?: `no`
- un evento ancora aperto rende il prezzo non affidabile come base operativa?: `no`
- aspettare darebbe un setup migliore?: `si`
- uno dei due lati ha davvero edge probabilistico netto dopo costi e carry?: `si`, il long se scatta il trigger

Chiusura sezione
- `no-trade` non e il risultato migliore
- il risultato corretto e `condizionale`, perche trigger e invalidazione sono gia disciplinabili ma non attivi

## 16. Decisione finale
- verdict fondamentale ereditato: `fairly priced`
- stato evento/regime: `pulito`
- bias investment / long-term: `bullish`
- bias 1W: `bullish`
- bias 1D: `bullish`
- bias operativo: `neutral`
- lato prioritario da cercare: `nessuno`
- forza della priorita direzionale: `nessuna`
- lato con edge maggiore adesso: `long`
- lato candidato all attivazione: `long`
- stato del setup tattico: `condizionale`
- migliore espressione investment: `HODL if already in`
- migliore espressione tattica: `swing long`
- scenario dominante con probabilita stimata: `continuation bullish`, `40%`
- timeframe dominante della tesi: `1D -> 4H`
- orizzonte holding implicito: `swing multi-day / multi-week`
- coerenza con la tesi fondamentale: `coerente`
- conviction: `media`
- eseguibilita: `alta`
- invalidation della tesi:
  - tattica: perdita di `~$74.0k` e soprattutto del blocco `~$73.0k`
  - strutturale piu larga: ritorno sotto `~$60.5k`
- se spot: logica di accumulo o di hold:
  - `hold if already in`
  - nuovo accumulo meglio su pullback, non nel mezzo del box alto
- se swing: entry logic / invalidation / target logic:
  - entry solo sopra `~$75.0k` con acceptance oppure su pullback tenuto in `~$74.0k - $74.2k`
  - invalidazione sotto `~$74.2k` / `~$73.8k` a seconda del trigger
  - target `~$75.998k` poi `~$77.5k - $78.0k`
- motivo principale del verdetto in massimo 3 frasi:
  - Bitcoin ha una struttura `1W / 1D` rialzista e non e dominato da un evento aperto, quindi il lato long resta il candidato operativo migliore.
  - Pero il fondamentale `fairly priced` non concede una priorita direzionale forte e il prezzo sta consolidando subito sotto una resistenza evidente in area `~$75k`.
  - La risposta corretta adesso non e inseguire: e preparare un `swing long` solo se il trigger si attiva davvero.
