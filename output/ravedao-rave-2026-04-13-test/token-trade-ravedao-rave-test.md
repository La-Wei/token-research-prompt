# Test Prompt: `token-trade-prompt.md`

## Input usato
- `[NOME/TICKER]`: `RaveDAO / RAVE`
- Report fondamentale usato:
  - `token-research-ravedao-rave-test.md`
  - `token-research-ravedao-rave-verification.md`
- Data snapshot principale: `2026-04-13`
- Timestamp mercato usato:
  - `2026-04-13 12:02 UTC`
  - `2026-04-13 14:05 Europe/Rome`
- Fonti market snapshot:
  - `Kraken Spot API`: `OHLC` su `RAVEUSD` per `max disponibile / 1w / 1d / 4h / 1h / 15m`
  - `Kraken Spot API`: `ticker`, `depth`
  - `Coinbase Exchange API`: `product`, `ticker`, `book`
  - `Binance Futures API`: `exchangeInfo`, `premiumIndex`, `openInterest`, `openInterestHist`, `fundingRate`, `depth`, `klines`
  - report fondamentale e report di verifica come contesto ereditato prevalente

---

# Output del prompt

## 0. Market status
- qualita dei chart: `alta`
- copertura dati: `parziale`
- timeframe disponibili: `max disponibile (~4 mesi) / 3M implicito / 1M finestra / 1W / 1D / 4H / 1H / 15m`
- profondita storica disponibile: `max da 2025-12-12`, `1Y no`, `6M no`, `3M si`, `1M si`, `1W si`
- report fondamentale disponibile: `si`
- report di verifica disponibile: `si`
- qualita del contesto ereditato: `alta`
- principali buchi informativi: `nessun vero storico multi-year`, `borrow / short availability`, `liquidation map cross-exchange completa`, `basis storica lunga`, `wallet mapping che chiuda con rigore la causalita del rally`
- confidenza preliminare: `media`

## 1. Recent event e regime shock audit
Ultimi `90d`
- evento: `Coinbase roadmap -> accesso spot confermato`
- data: `2026-02-04` roadmap pubblica; `2026-04-13` disponibilita `RAVE-USD` confermata sulla pagina ufficiale `Coinbase Advanced Trade`
- fonte: `Coinbase Markets`, `Coinbase Advanced Trade`, report di verifica
- stato: `confermato`
- cosa e confermato: `RAVE` ha migliorato accesso, venue quality e legittimazione di mercato
- cosa resta allegation o non chiuso: quanta parte del rerating attuale dipenda ancora da questo catalyst e quanta da reflexivity / leverage / float dynamics
- market reaction osservata: nel trimestre il mercato passa da area ATL di marzo a price discovery verticale di aprile, con volumi spot e perp molto piu alti
- impatto su business / token / market structure / fiducia: `token + market structure + fiducia`
- l evento e chiuso o ancora aperto?: `chiuso come fatto, aperto come effetto sul pricing`
- il setup corrente sembra tecnico o event-driven?: `inizialmente event-driven, poi amplificato da repricing tecnico e reflexive follow-through`

Ultimi `30d`
- evento: `rerating estremo senza rerating equivalente del token accrual`
- data: `2026-03-12 -> 2026-04-13`
- fonte: `Kraken 1D`, `CoinGecko`, report di verifica
- stato: `confermato`
- cosa e confermato: il prezzo passa da area ATL `~0.205-0.206` a massimo intraday `12.00` su Kraken nello stesso mese
- cosa resta allegation o non chiuso: la causalita precisa del move resta mista tra venue improvement, momentum, leverage e narrativa
- market reaction osservata: circa `46.1x` da ATL osservato a spot live Kraken `~9.4563`; profondita e turnover crescono molto ma il waterfall economico del token non mostra un upgrade equivalente
- impatto su business / token / market structure / fiducia: `token + market structure`
- l evento e chiuso o ancora aperto?: `ancora aperto come regime di prezzo`
- il setup corrente sembra tecnico o event-driven?: `repricing da evento diventato overshoot da euforia / squeeze`

Ultimi `7d`
- evento: `blow-off expansion con perp in sconto e funding negativo`
- data: `2026-04-09 -> 2026-04-13`
- fonte: `Kraken Spot API`, `Coinbase Exchange API`, `Binance Futures API`
- stato: `confermato`
- cosa e confermato: su `Kraken 1D` il token chiude `2026-04-09` a `~1.0005`, `2026-04-10` a `~1.6055`, `2026-04-11` a `~2.1691`, `2026-04-12` a `~6.2690`, mentre il `2026-04-13` stampa finora `high 12.00` e `last ~9.4563`
- cosa resta allegation o non chiuso: se l impulso stia ancora pulendo posizioni short / hedge oppure se sia gia entrato in una fase distributiva ad alta volatilita
- market reaction osservata: `Coinbase` spot `~9.3850`, `Kraken` spot `~9.4563`, `Binance` perp mark `~8.8040`; il perp tratta circa `-6.2% / -6.9%` sotto spot e le ultime `12` letture funding sono tutte negative mentre l `OI` sale verso `~$103M-$105M`
- impatto su business / token / market structure / fiducia: `market structure + token`
- l evento e chiuso o ancora aperto?: `ancora aperto`
- il setup corrente sembra tecnico o event-driven?: `nettamente event-driven, con componente di squeeze / dislocazione ancora irrisolta`

Mini verdict
- `evento materiale ancora aperto`
- impatto principale: `market structure / token / fiducia`
- stato: `in evoluzione`

## 2. Executive view
- La tesi fondamentale ereditata resta `sopravvalutato`: business reale ma piccolo, token rights deboli, accrual poco dimostrato, venue migliori ma valuation molto avanti.
- Il setup di mercato non trasforma automaticamente questa tesi in short immediato: `1W` e `1D` restano violentemente bullish, mentre il perp tratta in sconto con funding negativo.
- investment view: `bearish`, ma con confidenza bassa per un vero `HODL multi-year` dato che lo storico osservabile e troppo corto.
- tactical view: `neutral`
- lato prioritario da cercare: `short`
- lato con edge maggiore adesso: `nessuno`
- perche il lato opposto non e preferito: il long fresco e troppo esteso; lo short e il lato da cercare, ma non ancora eseguibile bene senza breakdown / failed reclaim pulito
- migliore espressione investment: `avoid`
- migliore espressione tattica: `no trade`
- scenario dominante con probabilita stimata: `chop / digestione alta 35%`
- timeframe dominante della view: `4H / 1D`
- motivo principale: il mismatch tra fondamentale e chart esiste, ma non offre ancora un ingresso con asimmetria pulita su nessuno dei due lati
- rischio principale contro la view: continuation sopra `~10.00` e poi `12.00` con compressione della dislocazione perp
- grado di eseguibilita: `media`

## 3. Secular / investment context
Copertura reale del contesto secolare
- `max` disponibile: da `2025-12-12` a `2026-04-13`
- `1Y`: `non disponibile`
- `6M`: `non disponibile`
- `3M`: `disponibile`
- `1M`: `disponibile come finestra daily`, non come base seria per una tesi `HODL multi-year`

Osservazioni visibili
- Il massimo storico osservabile mostra un asset che ha passato mesi soprattutto tra `~0.21` e `~0.56`, poi e entrato in una gamba verticale culminata con `ATH intraday 12.00`.
- Dal minimo osservato `~0.2051` al prezzo live `~9.4563` il move e di circa `46.1x`.
- Dal picco intraday `12.00` il prezzo attuale e ancora solo `~21.2%` sotto ATH: non e un asset depresso di lungo, e un asset ancora vicino al blow-off high.
- La posizione nel ciclo osservabile non e `early trend`; e `late trend / blow-off` dentro uno storico troppo corto per inferenze di anni.

Cosa supporta un caso `HODL multi-quarter / multi-year`
- Il business esiste davvero, quindi il progetto non e una shell vuota.
- La venue quality e migliorata in modo materiale.
- Se il brand sopravvive oltre la gamba speculativa, il token puo restare rilevante come oggetto di attenzione di mercato.

Cosa smentisce un caso `HODL multi-quarter / multi-year`
- Non esiste profondita storica sufficiente per validare una tesi `HODL multi-year`.
- Il token resta debole sul piano dei diritti economici e del value accrual.
- La market cap e l `FDV` attuali appaiono molto avanti rispetto alla scala del business dichiarato.
- Lo storico recente suggerisce price discovery violenta, non una base matura da investimento paziente.

Cosa invalida la tesi investment
- Per alzare davvero la qualita del caso `HODL` servirebbero mesi di base, proof of token sinks monetizzabili, reporting di wallet treasury / buyback e piu storia attraverso regimi diversi.
- Senza questi elementi, chiamarlo `HODL di anni` sarebbe prematuro.

Chiusura sezione
- bias `secular / investment`: `non valutabile con rigore per un HODL multi-year`; il massimo osservabile resta comunque `bullish ma in fase blow-off`
- confidenza del caso investment: `bassa`

## 4. Higher timeframe context
`1W`
- trend primario: `fortemente bullish`
- struttura: `HH/HL`, con settimana live che apre `~0.3162` e stampa finora `high 12.00`, `last ~9.4563`
- regime: `price discovery / blow-off`, non trend ordinato
- livelli chiave: `~6.00-6.30` primo blocco di accettazione importante; `~2.17-2.30` supporto weekly piu profondo; `~10.00` prima area da riconquistare in close; `12.00` massimo osservato
- premium o discount rispetto al range HTF: `forte premium`
- dove il chart invalida la tesi HTF: la forza weekly si deteriora in modo serio sotto `~6.00`, e ancora di piu sotto `~2.17-2.30`

`1D`
- trend primario: `bullish`
- struttura: nessuna `LH/LL` pulita; la sequenza daily e ancora di espansione
- regime: `vertical trend / blow-off`
- giornate chiave:
  - `2026-04-09`: `close ~1.0005`
  - `2026-04-10`: `close ~1.6055`
  - `2026-04-11`: `close ~2.1691`
  - `2026-04-12`: `close ~6.2690`
  - `2026-04-13` live: `open ~6.2594`, `high 12.00`, `low ~5.1113`, `last ~9.4563`
- livelli chiave: `~7.70-8.00` primo supporto daily vicino; `~6.00-6.30` supporto piu importante del breakdown test; `~10.00` resistenza intermedia; `12.00` massimo
- premium o discount rispetto al range HTF: `estremo premium`, vicino alla parte alta dell intero range osservato
- dove il chart invalida la tesi `1D`: perdita di `~7.70-8.00` apre mean reversion piu seria; perdita di `~6.00-6.30` cambia davvero il tono daily

Chiusura sezione
- bias `1W`: `bullish`
- bias `1D`: `bullish`

## 5. Mid timeframe structure
Osservazioni `4H`
- ultime candele chiave:
  - `2026-04-12 20:00 UTC`: `open ~4.6647`, `high 6.75`, `close ~6.2690`
  - `2026-04-13 00:00 UTC`: `open ~6.2594`, `high ~6.5710`, `low ~5.1113`, `close ~6.0954`
  - `2026-04-13 04:00 UTC`: `open ~6.0806`, `high 12.00`, `close ~9.9900`
  - `2026-04-13 08:00 UTC`: `open ~9.7820`, `high 11.00`, `low ~7.6985`, `close ~9.4078`
  - `2026-04-13 12:00 UTC` live: `open ~9.3983`, `high ~9.4563`, `low ~9.3231`
- La struttura intermedia non e ancora in breakdown: e una consolidazione alta dopo una gamba estrema.
- Il momentum e meno pulito rispetto alla fase `6 -> 12`, ma non si vede ancora un inversione `4H` confermata.
- Il mercato sta decidendo se trasformare `~7.70-8.00` in base oppure se rifiutare tutta la parte alta del blow-off.

Conflitto o allineamento con HTF
- `4H` ancora allineato con la forza `1W / 1D`.
- L allineamento non basta per comprare bene: il problema e la qualita del risk/reward, non la direzione nuda del chart.

Dove si invalida la tesi su timeframe medio
- per una lettura ancora costruttiva: perdere `~7.70-8.00` peggiora molto la struttura
- per una lettura davvero deteriorata: perdita di `~6.00-6.30`
- per riattivare continuation pulita: acceptance sopra `~10.00`, poi `12.00`

## 6. Lower timeframe timing
Osservazioni `1H`
- alle `07:00 UTC` il mercato stampa `high 12.00` e chiude l ora a `~9.99`
- nelle due ore successive scarica fino a `~7.7720` e `~7.6985`, poi stabilizza tra `~8.97` e `~9.46`
- le ultime ore mostrano piu assorbimento che trend lineare

Osservazioni `15m`
- dopo il flush il mercato oscilla in un range rumoroso
- ultime chiusure osservate: `~9.2371`, `~9.4669`, `~9.4705`, `~9.4078`, `~9.4563`
- zona micro attuale: `~9.32-9.67`

Trigger di entrata possibili
- long solo:
  - `su pullback hold` in area `~8.80-9.00` con reclaim `1H` di `~9.60-9.70`
  - oppure `su acceptance` sopra `~10.00`, meglio ancora sopra `12.00`
- short solo:
  - `su failed reclaim` della fascia `~9.60-10.00` dopo perdita dei supporti
  - oppure `su breakdown` confermato sotto `~8.80`, con struttura molto piu interessante sotto `~7.70`

Conferme richieste
- per il long: tenuta del pullback senza nuovo allargamento dello sconto del perp
- per lo short: perdita di supporti con follow-through del prezzo, non solo spike

Rischio di chase
- `alto` sul long, perche il mercato ha gia fatto una gamba verticale eccezionale
- `alto` sullo short, perche il perp non segnala euforia long classica e il squeeze risk resta vivo

Timing migliore
- `aspettare`

## 7. Derivatives e positioning
Fatti verificabili
- `Binance Futures premiumIndex`:
  - mark `~8.8040`
  - index `~9.3172`
  - estimated settle `~9.4148`
  - funding live `~-0.7148%`
  - next funding `2026-04-13 13:00 UTC`
- `Binance OI` live:
  - `11,751,343` contratti
  - circa `~$103.5M` notionals sul mark live
- `openInterestHist` nell ultima ora circa:
  - contratti da `~11.44M` a `~11.77M`
  - notional da `~$102.5M` a `~$104.8M`
  - variazione approssimativa: `+2.2%`
- funding history recente:
  - ultime `12` letture tutte negative
  - range approssimativo `~-0.27%` a `~-0.70%`

Inferenze operative
- Il positioning contraddice lo short semplicistico da `asset sopravvalutato`: il perp non tratta in euphoric premium, ma in sconto rilevante contro index e spot.
- Il carry non aiuta lo short: funding negativo significa che la pressione lato perp e gia scarica / difensiva, non ancora euforica.
- L `OI` che sale mentre funding resta negativo suggerisce leva ancora attiva in un contesto non pulito, con rischio di squeeze e flush in entrambe le direzioni.
- Non ho dati affidabili su `borrow cost`, `short availability` e `liquidation map` completa; quindi non va finta una precisione che non c e.

Conclusione operativa
- il positioning non regala un long a mercato
- ma penalizza anche il fade short immediato
- questo e uno dei motivi principali per cui la lettura corretta resta `neutral / no trade`

## 8. Liquidity e execution quality
Fatti verificabili
- `Kraken Spot`:
  - last `~9.4563`
  - spread osservato `~0.59%`
  - top `20` bid depth `~$61.7k`
  - top `20` ask depth `~$76.1k`
  - top `100` bid depth `~$301.0k`
  - top `100` ask depth `~$294.3k`
- `Coinbase Spot`:
  - last `~9.3850`
  - spread osservato `~0.14%`
  - top `20` bid depth `~$6.3k`
  - top `20` ask depth `~$21.9k`
  - top `100` bid depth `~$121.1k`
  - top `100` ask depth `~$138.1k`
- `Binance Perp`:
  - mark `~8.8040`
  - spread osservato `~0.018%`
  - top `20` bid depth `~$2.0k`
  - top `20` ask depth `~$4.0k`
  - top `100` bid depth `~$15.9k`
  - top `100` ask depth `~$12.7k`

Inferenze operative
- La liquidita spot e reale e molto migliore della tesi vecchia da venue marginali.
- La liquidita resta comunque concentrata e meno profonda di un large-cap; dentro una fase di blow-off questo conta molto.
- Una size piccola o media e eseguibile, ma il costo vero non e solo lo spread: e la volatilita del contesto.

Livelli magnete / zone di liquidita
- `~9.30-9.40` supporto micro attuale
- `~8.80-9.00` primo blocco da timing
- `~7.70-8.00` zona che decide se il pullback resta costruttivo o no
- `~10.00` prima soglia di continuation
- `12.00` massimo / liquidity grab evidente

Giudizio di esecuzione
- la view e `eseguibile` ma non `facile`
- una size sensata entra e esce, ma l edge oggi e peggiore della tradabilita teorica del mercato
- esecuzione complessiva: `media`

## 8A. Directional symmetry test
- lato prioritario da cercare derivato dal fondamentale: `short`
- miglior caso `long` disponibile adesso:
  - il lato long ha una logica solo se il mercato dimostra che il flush da `12 -> 7.7` e stato assorbito
  - trigger migliori: `hold` di `~8.80-9.00` con reclaim `~9.60-9.70`, oppure acceptance sopra `~10.00` e poi `12.00`
  - a favore: `1W` e `1D` restano bullish, spot piu forte del perp, funding negativo limita il rischio di euforia long classica
- miglior caso `short` disponibile adesso:
  - il lato short ha una logica solo se il mercato smette di difendere la parte alta del range
  - trigger migliori: failed reclaim `~9.60-10.00` dopo perdita dei supporti, oppure breakdown confermato sotto `~8.80` e meglio ancora sotto `~7.70`
  - a favore: fondamentale `sopravvalutato`, struttura da blow-off, ampio spazio di mean reversion verso `~6.00-6.30`
- quale lato ha l asimmetria migliore:
  - `condizionalmente short dopo trigger`
  - `adesso nessuno`
- perche il lato opposto e inferiore:
  - il long fresco compra un asset gia esploso e ancora vicino al massimo del regime osservato
  - lo short fresco vende contro trend `1W / 1D` mentre il perp e gia in sconto e il carry penalizza il fade meccanico
- differenza tra `tesi corretta` e `trade con edge`:
  - la tesi fondamentale puo restare `sopravvalutato`
  - ma finche il mercato non perde livelli chiave, questa non diventa automaticamente uno short con edge
- se il fondamentale e `sopravvalutato`: perche lo short e preferibile oppure perche non lo e ancora
  - lo short diventerebbe il lato preferibile solo sotto breakdown confermato
  - non lo e ancora perche price action, funding e basis non mostrano capitolazione del lato rialzista
- se il fondamentale e `sottovalutato`: `n.a.`

## 9. Investment / HODL case
- espressione investment: `avoid`
- orizzonte dominante: `multi-year`
- timeframe usato per la tesi investment: `max disponibile (~4 mesi) + 3M / 1M finestra + report fondamentale + report di verifica`
- coerenza con la tesi fondamentale: `alta`
- cosa rende sensato il caso investment:
  - il business esiste
  - la venue quality e migliorata
  - il progetto ha una presenza di mercato reale
- cosa lo invalida:
  - storico troppo corto per parlare seriamente di `HODL di anni`
  - token rights deboli e value accrual poco dimostrato
  - valuation troppo avanti rispetto al business dichiarato
  - regime attuale da blow-off, non da base d investimento
- cosa migliorerebbe la tesi:
  - `6-12` mesi di base o consolidazione che sopravvive a un cambio di regime
  - reporting wallet / buyback / treasury
  - prova di utility live con impatto economico sul token
  - migliore trasparenza su vesting e distribuzione
- cosa la peggiorerebbe:
  - perdita della gamba finale sopra `~6.00`
  - ulteriore espansione parabolica senza miglioramento dell accrual
  - conferma di supply overhang / unlock pressure non assorbita

## 10. Spot / positional case
- espressione spot: `hold if already in`
- tipo di caso: `positional multi-week`
- timeframe usato per la tesi spot: `1W / 1D / 4H`
- coerenza con la tesi fondamentale: `media`
- cosa rende sensato il caso spot:
  - `1W` e `1D` restano bullish
  - funding negativo e perp in sconto riducono l edge dello short aggressivo
  - un holder entrato molto piu in basso puo ancora lasciare correre una size ridotta
- cosa lo invalida:
  - come `fresh spot` il prezzo e troppo esteso
  - il token resta strutturalmente sopravvalutato
  - la struttura operativa non offre ancora un punto di accumulo disciplinato
- cosa migliorerebbe la tesi:
  - base multi-day sopra `~7.70-8.00`
  - pullback ordinato con tenuta di `~6.00-6.30`
  - funding che resta non euforico mentre il prezzo costruisce supporti
- cosa la peggiorerebbe:
  - perdita di `~7.70-8.00`
  - perdita di `~6.00-6.30`
  - nuovo squeeze verticale senza consolidazione, che alza ancora il rischio di reversal

## 11. Swing long case
- stato: `non attivo adesso`
- trigger long: `pullback hold` in area `~8.80-9.00` con reclaim `1H` di `~9.60-9.70`, oppure acceptance sopra `~10.00` e poi `12.00`
- livello o zona di entrata: `su hold + reclaim`, non in mezzo al range rumoroso
- invalidazione: sotto `~8.80` per il trigger tattico; invalidazione piu seria sotto `~7.70`
- primi target: `~10.00`, `~11.00`, `12.00`
- timeframe dominante: `1H / 4H`
- condizione che trasformerebbe il long in no trade: reclaim senza follow-through o nuovo allargamento dello sconto del perp mentre il prezzo non fa nuovi massimi

## 12. Swing short case
- stato: `non attivo adesso`
- trigger short: `failed reclaim` della fascia `~9.60-10.00` dopo perdita dei supporti, oppure breakdown confermato sotto `~8.80`; il setup migliora molto sotto `~7.70`
- livello o zona di entrata: `su rejection` o `su breakdown`, non al centro del range
- invalidazione: recovery sopra `~10.00`; invalidazione maggiore sopra `12.00`
- primi target: `~9.00`, `~8.00`, `~6.00-6.30`
- timeframe dominante: `1H / 4H / 1D`
- condizione che trasformerebbe lo short in no trade: funding che resta fortemente negativo mentre il prezzo rifiuta di accelerare al ribasso e ricomprime rapidamente verso `~10.00`

## 12A. Probabilistic scenario map
- scenario `1`: `chop / digestione alta`
  - probabilita stimata: `35%`
  - trigger / condizione: tenuta grossolana di `~8.80-9.00` senza reclaim pulito sopra `~10.00` e senza breakdown sotto `~8.80`
  - path di prezzo atteso: range rumoroso tra parte alta `~9.8-10.0` e parte bassa `~8.8-9.0`
  - lato favorito: `nessuno`
  - migliore espressione: `no trade`
  - invalidazione dello scenario: uscita pulita sopra `~10.00` o sotto `~8.80`
- scenario `2`: `continuation bullish`
  - probabilita stimata: `30%`
  - trigger / condizione: acceptance sopra `~10.00` con compressione dello sconto perp e tenuta dei pullback
  - path di prezzo atteso: ritest di `~11.00`, poi `12.00`, poi possibile estensione
  - lato favorito: `long`
  - migliore espressione: `swing long`
  - invalidazione dello scenario: false breakout e ritorno veloce sotto `~9.60`
- scenario `3`: `reversion / breakdown bearish`
  - probabilita stimata: `25%`
  - trigger / condizione: perdita netta di `~8.80`, poi conferma sotto `~7.70`
  - path di prezzo atteso: test di `~8.00`, poi `~6.00-6.30`, con spazio ulteriore se il sentiment si rompe davvero
  - lato favorito: `short`
  - migliore espressione: `swing short`
  - invalidazione dello scenario: reclaim veloce sopra `~9.60-10.00`
- scenario `4`: `event extension / squeeze finale`
  - probabilita stimata: `10%`
  - trigger / condizione: accelerazione impulsiva sopra `12.00` con ulteriore espansione dei volumi spot
  - path di prezzo atteso: nuova gamba di euforia prima di una digestione piu violenta
  - lato favorito: `long`
  - migliore espressione: `swing long`
  - invalidazione dello scenario: mancato follow-through sopra `12.00`

Chiusura sezione
- scenario dominante: `chop / digestione alta 35%`
- scenario piu pericoloso contro la view: `event extension / squeeze finale 10%`
- lato con `EV` migliore adesso: `nessuno`
- lato prioritario da cercare finche il fondamentale resta questo: `short`

## 13. No-trade test
- il setup e troppo sporco? `si`
- il risk/reward e insufficiente? `si, sia per fresh long sia per fade short`
- la liquidita o il positioning peggiorano troppo l esecuzione? `la liquidita e abbastanza buona; il positioning toglie edge allo short e non regala long pulito`
- la view e piu teorica che praticabile? `si, se si forza un ingresso adesso`
- un evento ancora aperto rende il prezzo non affidabile come base operativa? `si`
- aspettare darebbe un setup migliore? `si`
- uno dei due lati ha davvero edge probabilistico netto dopo costi e carry? `no`

## 14. Decisione finale
- verdict fondamentale ereditato: `sopravvalutato`
- stato evento/regime: `event-driven`
- bias 1M / secular: `non disponibile`
- bias 1W: `bullish`
- bias 1D: `bullish`
- bias operativo: `neutral`
- lato prioritario da cercare: `short`
- lato con edge maggiore adesso: `nessuno`
- migliore espressione investment: `avoid`
- migliore espressione tattica: `no trade`
- scenario dominante con probabilita stimata: `chop / digestione alta 35%`
- timeframe dominante della tesi: `4H / 1D`
- orizzonte holding implicito: `swing multi-day`
- coerenza con la tesi fondamentale: `media`
- conviction: `media`
- eseguibilita: `media`
- invalidation della tesi:
  - `bullish invalidation` del `no trade`: acceptance sopra `~10.00` e poi `12.00`, con compressione dello sconto perp e funding meno difensivo
  - `bearish invalidation` della neutralita: perdita netta di `~8.80`, poi `~7.70`, e soprattutto `~6.00-6.30`
- se spot: `non accumulare fresco qui; se gia dentro da molto piu in basso ha senso solo hold di una size ridotta / de-riskata finche il daily non perde 7.70 e poi 6.00`
- se swing: `niente trade a mercato ora; aspettare o pullback hold + reclaim per long, oppure rejection / breakdown molto piu pulita per short`
- motivo principale del verdetto in massimo 3 frasi:
  - `RAVE` resta troppo debole come caso `investment / HODL di anni`: storico corto, token quality bassa e valuation molto avanti rispetto al suo waterfall.
  - Allo stesso tempo `1W` e `1D` non autorizzano uno short semplice, perche il chart resta fortissimo e il perp tratta ancora in sconto con funding negativo.
  - La conclusione disciplinata oggi non e proteggere il long o il short: il lato da cercare resta `short`, ma finche non si manifesta il trigger corretto la risposta giusta resta `no trade`.
