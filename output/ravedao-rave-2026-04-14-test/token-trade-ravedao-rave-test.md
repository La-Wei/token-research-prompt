# Token Trade: `RaveDAO / RAVE`

## Input usato
- `[NOME/TICKER]`: `RaveDAO / RAVE`
- Report fondamentale usato:
  - `output/ravedao-rave-2026-04-14-test/token-research-ravedao-rave-test.md`
- Report di verifica usato:
  - `output/ravedao-rave-2026-04-14-test/token-research-ravedao-rave-verification.md`
- Data snapshot principale: `2026-04-14`
- Timestamp mercato usato:
  - `2026-04-13 22:52 UTC` per `Coinbase` ticker
  - `2026-04-13 22:45 UTC` per ultime candele `15m` spot Kraken
  - `2026-04-13 22:00 UTC` per ultima funding history disponibile `Bitget`
- Fonti market snapshot:
  - `Kraken Public API`: `AssetPairs`, `Ticker`, `Depth`, `OHLC` su `RAVEUSD`
  - `Coinbase Exchange API`: `ticker`, `book` su `RAVE-USD`
  - `Bitget Futures API`: `ticker`, `merge-depth`, `open-interest`, `history-fund-rate`, `candles` su `RAVEUSDT`
  - `CoinGecko` per range storico sintetico, venue mix e recent-event discovery
  - report fondamentale e report di verifica come contesto ereditato prevalente

---

# Output del prompt

## 0. Market status
- qualita dei chart: `alta`
- copertura dati: `parziale`
- fonti principali usate:
  - `Kraken Public API`
  - `Coinbase Exchange API`
  - `Bitget Futures API`
  - `CoinGecko`
  - report fondamentale e report di verifica
- fonti tentate ma non ottenute, se rilevanti:
  - non ho ottenuto una liquidation map completa cross-venue
  - non ho ottenuto dati puliti su borrow cost e short availability spot
  - non ho ottenuto una serie storica lunga di OI oltre il dato live / funding history corta
- timeframe disponibili:
  - `max osservabile`
  - `3M`
  - `1W`
  - `1D`
  - `4H`
  - `1H`
  - `15m`
- profondita storica disponibile:
  - `max` da `2025-12-11 / 2025-12-12` circa
  - `1Y`: `no`
  - `6M`: `no`
  - `3M`: `si`
  - `monthly candle`: `non disponibile come timeframe nativo utile`
  - `1W`: `si`
- report fondamentale disponibile: `si`
- report di verifica disponibile: `si`
- qualita del contesto ereditato: `alta`
- principali buchi informativi:
  - `nessuna storia multi-year`
  - `nessun dato serio su borrow / short availability`
  - `nessuna liquidation map completa`
  - `nessuna chiusura primaria della allegation su deployer-wallet / Bitget`
- blocchi ancora non osservabili:
  - qualità del crowding short spot
  - profondita vera cross-exchange sotto stress
  - causalita completa del move degli ultimi `7d`
- confidenza preliminare: `media`

## 1. Recent event e regime evidence log
Ultimi `90d`
- evento: `upgrade materiale della venue quality con spot Coinbase confermato`
- data: disponibilita spot confermata entro `2026-04-14`
- fonte: `Coinbase Advanced Trade`, report di verifica
- stato: `confermato`
- cosa e confermato:
  - `RAVE-USD` e attivo su `Coinbase`
  - il token non tratta piu solo su venue secondarie
- cosa resta allegation o non chiuso:
  - quanto del rerating attuale sia ancora listing/venue-driven e quanto sia puro momentum/leverage
- market reaction osservata:
  - `Coinbase` pesa quota materiale del volume spot
  - migliore accessibilita e legittimazione del mercato
- impatto su business / token / market structure / fiducia: `market structure / fiducia`
- l evento e chiuso o ancora aperto?: `chiuso come fatto, aperto come effetto sul pricing`
- il setup corrente sembra tecnico o event-driven?: `inizialmente event-driven, poi amplificato da price action tecnica e reflessivita`

Ultimi `30d`
- evento: `rerating estremo dal minimo di marzo al blow-off di aprile`
- data: `2026-03-12 -> 2026-04-13`
- fonte: `Kraken 1D`, `CoinGecko`, report di verifica
- stato: `confermato`
- cosa e confermato:
  - da area `~0.205-0.206` il prezzo ha stampato fino a `16.80` su `Kraken` e `14.18` su `CoinGecko`
- cosa resta allegation o non chiuso:
  - il mix preciso tra sponsor narrative, venue improvement, perp activity, social mania e possibili exchange flows
- market reaction osservata:
  - daily expansion verticale:
    - `2026-04-08` close `~1.0005`
    - `2026-04-09` close `~1.6055`
    - `2026-04-10` close `~2.1691`
    - `2026-04-11` close `~6.2690`
    - `2026-04-13` candle live/high-vol close `~9.46` con high `16.80`
- impatto su business / token / market structure / fiducia: `token / market structure`
- l evento e chiuso o ancora aperto?: `ancora aperto`
- il setup corrente sembra tecnico o event-driven?: `repricing da evento diventato overshoot da euforia`

Ultimi `7d`
- evento: `blow-off, perp volume spike e allegation su flows verso Bitget`
- data: `2026-04-13` / `2026-04-14`
- fonte: `Bitget Futures API`, `CoinGecko Recently Happened`, report di verifica
- stato: `in evoluzione`
- cosa e confermato:
  - `Bitget` mostra `quoteVolume ~829.26M USDT` su 24h
  - funding live `~-0.2575%`
  - ultime `10` funding storiche tutte negative, con minimo recente `~-1.2175%`
  - `CoinGecko` segnala `RAVE Ranks Third in Global Perpetuals Trading Volume`
- cosa resta allegation o non chiuso:
  - `CoinGecko` segnala che wallet collegati al deployer avrebbero spostato `~18.58M RAVE` a `Bitget` prima del pump
  - non ho fonte primaria sufficiente per chiudere il punto come fatto definitivo
- market reaction osservata:
  - wick estremi
  - volatilita 1H e 15m molto alta
  - perp in sconto rispetto a index e spot, non in premium euforico
- impatto su business / token / market structure / fiducia: `market structure / fiducia / narrativa`
- l evento e chiuso o ancora aperto?: `ancora aperto`
- il setup corrente sembra tecnico o event-driven?: `nettamente event-driven`

Mini verdict
- `evento materiale ancora aperto`
- impatto principale: `market structure / fiducia`
- stato: `in evoluzione`

## 2. Executive view
- Tesi fondamentale ereditata: `RAVE` resta `sopravvalutato`; business reale ma piccolo, token rights deboli, accrual non dimostrato.
- Coerenza col setup attuale: il fondamentale resta short-biased, ma il tape non permette un fade cieco.
- investment view: `bearish`
- tactical view: `bearish`
- lato prioritario da cercare: `short`
- forza della priorita direzionale: `debole`
- lato con edge maggiore adesso: `short`
- stato del setup tattico: `condizionale`
- perche il lato opposto non e preferito: il long esiste solo come squeeze continuation e oggi paga un rischio di chase troppo alto.
- migliore espressione investment: `avoid`
- migliore espressione tattica: `swing short`
- scenario dominante con probabilita stimata: `chop / digestione ad alta volatilita 35%`
- timeframe dominante della view: `1H / 4H`
- motivo principale: fondamentale fragile + chart blow-off + perp non ancora favorevole a uno short immediato a mercato.
- rischio principale contro la view: reclaim pulito di `10.30` e poi `12.00` con nuova compressione verso l alto.
- grado di eseguibilita: `media`

## 3. Investment / long-term context
Copertura reale del contesto secolare
- `max` disponibile: da circa `2025-12-11 / 2025-12-12`
- `1Y`: `non disponibile`
- `6M`: `non disponibile`
- `3M`: `disponibile`
- `monthly candle`: `non disponibile come serie utile`

Osservazioni visibili
- Il massimo timeframe osservabile mostra un asset rimasto per mesi soprattutto in fascia `~0.20 - 0.70`, poi entrato in una gamba quasi verticale.
- La settimana live `2026-04-07` ha aperto `~0.3162`, ha stampato `high 16.80` e sta trattando ora in area `~9.4-9.7`: e una candela da `price discovery / blow-off`, non da trend maturo e ordinato.
- Dal minimo osservabile `~0.20509` al prezzo spot live `~9.50-9.75`, il move resta nell ordine di `~46x-47x`.
- Il prezzo attuale non e in early trend. E in `late trend / blow-off` dentro uno storico troppo corto per una vera view `HODL multi-year`.

Cosa supporta un caso `HODL multi-quarter / multi-year`
- Il business esiste davvero, quindi il token non parte da narrativa completamente vuota.
- La venue quality e migliorata in modo reale.
- Se il brand reggesse dopo la fase euforica, l attenzione di mercato potrebbe durare piu del previsto.

Cosa smentisce un caso `HODL multi-quarter / multi-year`
- Lo storico osservabile e troppo corto.
- Il token resta debole lato diritti economici e accrual.
- Il prezzo attuale e vicino a una fase di blow-off piu che a una base investibile.
- La verifica ha alzato il rischio su optics, exchange-flow allegations e supply story non perfettamente chiusa.
- Il chart `max / 3M` osservabile resta rialzista, ma questo descrive il move di prezzo, non un caso `investment` credibile oggi.

Cosa invalida la tesi investment
- Per rendere il caso investment serio servirebbero:
  - mesi di base vera dopo lo squeeze
  - proof di token sinks economicamente pesanti
  - wallet treasury / buyback trasparenti
  - piu storia attraverso regimi diversi

Chiusura sezione
- bias `investment / long-term`: `bearish`
- confidenza del caso investment: `bassa`

## 4. Higher timeframe context
`1W`
- trend primario: `fortemente bullish`
- struttura: ancora `HH/HL`, ma la candela corrente e da `price discovery` piu che da trend ordinato
- regime: `blow-off / euforia`, non accumulazione sana
- livelli chiave:
  - `~6.00 - 6.30` primo blocco di accettazione weekly
  - `~1.60 - 2.20` supporto piu profondo del re-rating
  - `12.00`
  - `16.80`
- premium o discount rispetto al range HTF: `estremo premium`
- dove il chart invalida la tesi HTF:
  - sotto `~6.00 - 6.30` la forza weekly perde molta credibilita

`1D`
- trend primario: `bullish`
- struttura: nessuna sequenza `LH/LL` confermata sul daily
- regime: `vertical trend con wick estremi`
- osservazioni chiave:
  - `2026-04-08` close `~1.0005`
  - `2026-04-09` close `~1.6055`
  - `2026-04-10` close `~2.1691`
  - `2026-04-11` close `~6.2690`
  - `2026-04-13` live/partial close `~9.4608`, high `16.80`, low `5.1113`
- livelli chiave:
  - `~8.80 - 9.00` primo pivot giornaliero utile
  - `~7.70 - 8.00` supporto di struttura post-spike
  - `~10.20 - 10.30` prima area di reclaim
  - `12.00`
  - `16.80`
- premium o discount rispetto al range HTF: `forte premium`
- dove il chart invalida la tesi `1D`:
  - perdita pulita di `~8.80`
  - peggioramento serio sotto `~7.70 - 8.00`

Chiusura sezione
- bias `1W`: `bullish`
- bias `1D`: `bullish`

## 5. Mid timeframe structure
Osservazioni `4H`
- Ultime candele chiave spot Kraken:
  - `2026-04-13 00:00 UTC`: `open ~6.259`, `high ~6.571`, `low ~5.111`, `close ~6.095`
  - `2026-04-13 04:00 UTC`: `open ~6.081`, `high 12.00`, `close ~9.990`
  - `2026-04-13 08:00 UTC`: `open ~9.782`, `high 11.00`, `low ~7.699`, `close ~9.408`
  - `2026-04-13 12:00 UTC`: `open ~9.398`, `high ~10.311`, `close ~9.801`
  - `2026-04-13 16:00 UTC`: `open ~9.810`, `high 16.80`, `close ~13.511`
  - `2026-04-13 20:00 UTC`: `open ~13.509`, `low ~6.489`, `close ~9.461`
- La struttura intermedia non e ancora un breakdown confermato.
- E invece una `consolidazione/distribuzione ad alta volatilita` dopo un eccesso estremo.
- Il mercato ha gia mostrato:
  - estensione verticale
  - respinta violenta
  - rimbalzo
  - nuovo fade
- Questo riduce molto la qualita del trade a mercato e aumenta il valore del trigger.

Conflitto o allineamento con HTF
- `4H` non e ancora nettamente bearish come `1W / 1D` non sono ancora bearish.
- Il conflitto vero non e direzionale, ma di `qualita dell entry`: HTF forte, struttura intermedia sporca, fondamentale debole.

Dove si invalida la tesi su timeframe medio
- per una lettura ancora costruttiva: perdita di `~8.80`
- per una lettura di deterioramento serio: perdita di `~7.70 - 8.00`
- per riattivare continuation pulita: reclaim `~10.20 - 10.30`, poi `12.00`

## 6. Lower timeframe timing
Osservazioni `1H`
- Il blocco orario piu recente mostra:
  - squeeze fino a `16.80`
  - flush a `~6.49`
  - rebound fino a `~11.74`
  - ultimo ritorno in area `~9.44`
- Le ultime `1H` disponibili non mostrano ancora un trend pulito; mostrano un mercato che frusta entrambe le direzioni.

Osservazioni `15m`
- Dopo il picco `16.80`, il `15m` ha stampato:
  - breakdown fino a `8.3267`
  - rebound fino a `10.9999`
  - fade progressivo verso `~8.97 - 9.43`
- La microstruttura di adesso non premia il chase.

Trigger di entrata possibili
- long solo:
  - su reclaim `1H` di `~10.20 - 10.30`
  - oppure su acceptance sopra `12.00`
- short solo:
  - su failed reclaim di `~9.90 - 10.30`
  - oppure su breakdown confermato sotto `~8.80`

Conferme richieste
- per il long:
  - tenuta sopra `~9.80`
  - compressione dello sconto del perp
- per lo short:
  - close `1H` debole sotto supporto o rigetto chiaro dell area di reclaim
  - nessun riassorbimento immediato della rottura

Rischio di chase
- `molto alto` sul long
- `alto` sullo short a mercato senza trigger, perche il perp non e in crowding long classico

Rischio di fake breakout / fake breakdown
- `alto` su entrambi i lati

Timing migliore
- `aspettare`
- long solo `su reclaim`
- short `su failed reclaim` o `su breakdown`

## 7. Derivatives e positioning
Fatti verificabili `Bitget Futures`
- ticker live:
  - last `~9.2821`
  - mark `~9.2797`
  - index `~9.4594`
  - funding live `~-0.2575%`
  - quoteVolume `~829.26M USDT`
  - open24h `~5.5371`
  - high24h `~12.3841`
  - low24h `~5.2482`
- open interest live:
  - `5,659,819` contratti riportati da `open-interest`
- funding history recente:
  - ultime `10` funding tutte negative
  - range osservato circa `~-0.1055%` a `~-1.2175%`
- candele perp `1H`:
  - `2026-04-13 20:00 UTC`: `open ~12.0706`, `high ~12.0776`, `low ~6.9100`, `close ~8.3267`
  - `2026-04-13 21:00 UTC`: `open ~8.3267`, `high ~10.9000`, `close ~10.5621`
  - `2026-04-13 22:00 UTC`: `open ~10.5621`, `high ~10.5667`, `close ~8.9465`

Inferenze operative
- Il perp tratta in sconto rispetto a `index` e spot, non in premium euforico:
  - vs `index` il discount e circa `~-1.9%`
  - vs `Kraken` spot e circa `~-2.3%`
  - vs `Coinbase` snapshot e ancora piu largo
- Questo non supporta lo short semplicistico da `asset sopravvalutato e tutti troppo long`.
- Funding fortemente negativo e perp in sconto indicano piu difesa / hedge / crowding short relativo che euforia long lineare.
- Il carry non regala lo short.
- Il positioning quindi:
  - non regala il long
  - ma rende sporco anche il fade short immediato

Conclusione operativa
- il positioning `contraddice` uno short a mercato preso solo per valuation
- ma non invalida uno short `su trigger`
- squeeze risk e flush risk restano entrambi alti

## 8. Liquidity e execution quality
Fatti verificabili spot
- `Kraken`
  - last `~9.4999`
  - ask `~9.5896`
  - bid `~9.4712`
  - spread osservato `~1.25%`
  - depth:
    - ask top `20` `~$39.98k`
    - bid top `20` `~$31.01k`
    - ask top `100` `~$334.94k`
    - bid top `100` `~$415.45k`
- `Coinbase`
  - last `~9.748`
  - ask `~9.799`
  - bid `~9.7481`
  - spread osservato `~0.52%`
  - depth:
    - ask top `20` `~$14.01k`
    - bid top `20` `~$20.25k`
    - ask top `100` `~$87.61k`
    - bid top `100` `~$178.16k`

Fatti verificabili perp
- `Bitget`
  - ask `~9.2771`
  - bid `~9.2728`
  - spread osservato `~0.05%`
  - depth:
    - ask top `20` `~$29.02k`
    - bid top `20` `~$76.18k`
    - ask top `100` `~$241.25k`
    - bid top `100` `~$245.61k`

Inferenze operative
- La liquidita e reale e molto migliore della narrativa vecchia da token confinato su venue scarse.
- Resta comunque un mercato meno profondo di quanto market cap e volume headline farebbero pensare.
- Una size piccola o media e eseguibile.
- Una size aggressiva in un tape come questo rischia slippage psicologico e non solo meccanico.
- La view short e eseguibile meglio via perp `Bitget` che via spot puro, ma solo con trigger.

Domande chiave
- la view e eseguibile bene oppure solo teorica?
  - `eseguibile in modo medio`, non alto
- una size sensata puo entrare e uscire senza troppo attrito?
  - `si`, se disciplinata e non troppo grande
- il mercato e abbastanza profondo per sostenere la tesi?
  - `si per size tattiche`, `no` per assumere che la volatilita sia domata

## 8A. Directional symmetry test
- lato prioritario da cercare derivato dal fondamentale: `short`
- gate priorita direzionale:
  - `gate 1 - verdict`: `si`
  - `gate 2 - confidenza`: `si`
  - `gate 3 - copertura dati`: `si`
  - `gate 4 - regime`: `no`
- forza della priorita direzionale: `debole`

Miglior caso `long` disponibile adesso
- continuation di squeeze se il mercato:
  - riassorbe `~10.20 - 10.30`
  - riconquista `12.00`
  - riduce lo sconto del perp
- e un long tattico, non un long di tesi fondamentale

Miglior caso `short` disponibile adesso
- failed reclaim della fascia `~9.90 - 10.30`
- oppure breakdown sotto `~8.80` con follow-through
- e il lato coerente con la tesi fondamentale, ma solo dopo conferma

Quale lato ha l asimmetria migliore
- `short`, perche il downside potenziale verso `~8.80`, `~7.70`, `~6.50` e meglio allineato a fondamentale e struttura sporca

Quale lato ha l execution migliore
- `short`, ma via perp e solo dopo trigger

Perche il lato opposto e inferiore
- Il long oggi e quasi solo un trade di continuation / squeeze dentro un contesto fondamentale fragile e dopo una gamba gia enorme.

Differenza tra `tesi corretta` e `trade con edge`
- La tesi strutturale short-biased puo essere giusta senza che lo short a mercato sia buono adesso.
- Oggi non serve avere ragione sul fair value; serve aspettare un prezzo migliore o un trigger migliore.

Se il fondamentale e `sopravvalutato`
- Lo short resta preferibile come lato da cercare.
- Non e ancora preferibile come `market order immediato`, perche funding, perp discount ed evento aperto sporcano il timing.

## 9. Investment / HODL case
- espressione investment: `avoid`
- orizzonte dominante: `multi-quarter / multi-year`
- timeframe usato per la tesi investment: `max / 3M / 1W`
- coerenza con la tesi fondamentale: `coerente`
- cosa rende sensato il caso investment:
  - business reale
  - venue quality migliore
  - brand potenzialmente persistente oltre il ciclo hype
- cosa lo invalida:
  - rights economici troppo deboli
  - valuation estrema
  - storico troppo corto
- cosa migliorerebbe la tesi:
  - base lunga
  - token sinks live
  - trasparenza su treasury e buyback
- cosa la peggiorerebbe:
  - conferma di exchange-flow allegations
  - breakdown sotto la base post-spike
  - ulteriori dubbi su supply story

## 10. Spot / positional case
- espressione spot: `avoid`
- tipo di caso: `positional multi-week / multi-month`
- timeframe usato per la tesi spot: `1W / 1D / 4H`
- coerenza con la tesi fondamentale: `coerente`
- cosa rende sensato il caso spot:
  - solo il fatto che il chart grande non e ancora collassato
- cosa lo invalida:
  - rischio di comprare un blow-off con token economics deboli
- cosa migliorerebbe la tesi:
  - reset importante verso supporti veri e successiva base
  - riduzione forte della componente event-driven
- cosa la peggiorerebbe:
  - ulteriore wick / failure sotto `~8.80`
  - nuova narrativa negativa sui flussi

## 11. Swing long case
- trigger long:
  - reclaim `1H` di `~10.20 - 10.30` con tenuta sopra `~9.80`
  - trigger piu forte: acceptance sopra `12.00`
- livello o zona di entrata:
  - `~10.20 - 10.40` su reclaim confermato
  - oppure breakout sopra `12.00` solo se non viene subito riassorbito
- invalidazione:
  - per il reclaim long: ritorno sotto `~9.55`
  - per il breakout long: ritorno sotto `~11.20`
- primi target:
  - `~11.20`
  - `12.00`
  - `~13.50 - 14.30`
  - estensione `16.80`
- timeframe dominante: `1H / 4H`
- stato del case: `watchlist`
- condizione che trasformerebbe il long in no trade:
  - mancato reclaim di `~10.20 - 10.30`
  - nuova perdita di `~8.80`

## 12. Swing short case
- trigger short:
  - failed reclaim di `~9.90 - 10.30`
  - oppure close `1H` sotto `~8.80` e failure del rimbalzo successivo
- livello o zona di entrata:
  - `~9.90 - 10.30` se respinta
  - oppure retest fallito di `~8.80` dopo breakdown
- invalidazione:
  - per il failed reclaim short: acceptance sopra `~10.90`
  - per il breakdown short: reclaim deciso sopra `~9.20`
- primi target:
  - `~8.80`
  - `~7.70 - 8.00`
  - `~6.50`
  - estensione `~4.70`
- timeframe dominante: `1H / 4H`
- stato del case: `condizionale`
- condizione che trasformerebbe lo short in no trade:
  - funding ancora molto negativa con prezzo che reclaima `~10.30` e poi `12.00`, cioe se lo squeeze continua senza darti una failure pulita

## 13. Probabilistic scenario map
- timeframe comune della scenario map: `1H / 4H` nei prossimi `2-5` giorni

Scenario `1`: `chop / digestione violenta`
- probabilita stimata: `35%`
- trigger / condizione:
  - prezzo resta sopra `~8.80`
  - ma non recupera in modo pulito `12.00`
- path di prezzo atteso:
  - range ampio `~8.8 - 12.0`
- lato favorito: `nessuno`
- migliore espressione: `no trade / attesa`
- invalidazione dello scenario:
  - breakout sopra `12.00`
  - breakdown sotto `~8.80`

Scenario `2`: `breakdown / mean reversion`
- probabilita stimata: `30%`
- trigger / condizione:
  - close `1H` sotto `~8.80`
  - nessun reclaim serio
- path di prezzo atteso:
  - `~7.70 - 8.00`
  - poi `~6.50`
- lato favorito: `short`
- migliore espressione: `swing short`
- invalidazione dello scenario:
  - ritorno sopra `~9.20` e poi `~10.30`

Scenario `3`: `squeeze continuation`
- probabilita stimata: `25%`
- trigger / condizione:
  - reclaim `~10.20 - 10.30`
  - acceptance sopra `12.00`
- path di prezzo atteso:
  - `~13.50`
  - `~14.30`
  - possibile retest `16.80`
- lato favorito: `long`
- migliore espressione: `swing long`
- invalidazione dello scenario:
  - ritorno sotto `~9.80`

Scenario `4`: `event extension / trust shock`
- probabilita stimata: `10%`
- trigger / condizione:
  - nuova evidenza credibile su flows problematici o distribuzione
- path di prezzo atteso:
  - flush rapido a `~6.50` o peggio
- lato favorito: `short`
- migliore espressione: `swing short`
- invalidazione dello scenario:
  - allegation ridimensionate e prezzo stabile sopra `~10.30`

Chiusura sezione
- scenario dominante: `chop / digestione violenta 35%`
- scenario piu pericoloso contro la tua view: `squeeze continuation 25%`
- lato con `EV` migliore adesso: `short`

## 14. Trade activation test
- qual e il lato con `EV` migliore adesso / candidato all attivazione: `short`
- questo lato coincide con il lato prioritario oppure no?: `si`
- il lato candidato all attivazione ha un trigger attivo adesso?: `no`
- l invalidazione e chiara e abbastanza vicina da rendere il trade disciplinabile?: `si`
- l eseguibilita e almeno `media`?: `si`
- spread, slippage, carry o squeeze risk stanno ancora sabotando il setup?: `si, parzialmente`
- un evento aperto impedisce ancora di trattare il prezzo come base affidabile?: `si, parzialmente`

Chiusura sezione
- stato del setup tattico: `condizionale`
- motivo del lato candidato all attivazione:
  - e il lato meglio allineato a fondamentale, event-risk e struttura di possibile failed reclaim
- motivo principale della classificazione:
  - manca ancora il trigger pulito; short a mercato sarebbe una forzatura

## 15. No-trade test
- il setup e troppo sporco?: `si, a mercato`
- il risk/reward e insufficiente?: `si, per entry immediata`
- la liquidita o il positioning peggiorano troppo l esecuzione?: `si, ma non abbastanza da annullare un setup con trigger`
- la view e piu teorica che praticabile?: `no`
- un evento ancora aperto rende il prezzo non affidabile come base operativa?: `si`
- aspettare darebbe un setup migliore?: `si`
- uno dei due lati ha davvero edge probabilistico netto dopo costi e carry?: `si, lo short dopo trigger`

Conclusione secca
- Non e `no-trade` in senso pieno.
- E `condizionale`, perche il lato short resta valido ma va aspettato.

## 16. Decisione finale
- verdict fondamentale ereditato: `sopravvalutato`
- stato evento/regime: `event-driven`
- bias investment / long-term: `bearish`
- bias 1W: `bullish`
- bias 1D: `bullish`
- bias operativo: `bearish`
- lato prioritario da cercare: `short`
- forza della priorita direzionale: `debole`
- lato con edge maggiore adesso: `short`
- lato candidato all attivazione: `short`
- stato del setup tattico: `condizionale`
- migliore espressione investment: `avoid`
- migliore espressione tattica: `swing short`
- scenario dominante con probabilita stimata: `chop / digestione violenta 35%`
- timeframe dominante della tesi: `1H / 4H`
- orizzonte holding implicito: `swing multi-day`
- coerenza con la tesi fondamentale: `parzialmente coerente`
- conviction: `bassa`
- eseguibilita: `media`
- invalidation della tesi:
  - reclaim `1H / 4H` di `~10.20 - 10.30` e poi acceptance sopra `12.00`
- se spot: logica di accumulo o di hold:
  - `nessun accumulo nuovo`
  - se gia in spot, il tape supporta al massimo `hold tattico disciplinato` o riduzione in forza, non chase
- se swing: entry logic / invalidation / target logic:
  - `entry`: failed reclaim `~9.90 - 10.30` oppure breakdown sotto `~8.80`
  - `invalidation`: sopra `~10.90` sul fade short, oppure reclaim sopra `~9.20` sul breakdown short
  - `target`: `~8.80`, `~7.70 - 8.00`, `~6.50`
- motivo principale del verdetto:
  - Il fondamentale continua a dire `short da cercare`, ma il mercato non sta offrendo ancora uno short pulito a prezzo corrente.
  - `1W` e `1D` restano bullish, mentre funding negativa, perp discount ed evento aperto impediscono il fade automatico.
  - La risposta disciplinata oggi non e comprare il breakout ne shortare il rumore: e aspettare un `failed reclaim` o un `breakdown` vero.
