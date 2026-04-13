# Test Prompt: `token-trade-prompt.md`

## Input usato
- `[NOME/TICKER]`: `Hyperliquid / HYPE`
- Report fondamentale usato:
  - `token-research-hyperliquid-hype-test.md`
  - `token-research-hyperliquid-hype-verification.md`
- Data snapshot principale: `2026-04-10`
- Fonti market snapshot:
  - Hyperliquid API ufficiale: `candleSnapshot` su `@107` per `15m / 1h / 4h / 1d / 1w`
  - Hyperliquid API ufficiale: `l2Book` su `@107`
  - Bybit API pubblica: `HYPEUSDT` ticker, funding, open interest, orderbook, 1h kline
  - CoinGecko: cross-check prezzo, venue, multi-venue depth, token volume
  - DefiLlama: holders revenue, perp volume, DEX volume, protocol open interest

---

# Output del prompt

## 0. Market status
- qualita dei chart: `media`
- copertura dati: `parziale`
- timeframe disponibili: `15m / 1h / 4h / 1d / 1w` da `Hyperliquid API ufficiale`; `1h` cross-check da `Bybit`
- report fondamentale disponibile: `si`
- qualita del contesto ereditato: `alta`
- principali buchi informativi: `liquidation map`, `borrow/short availability`, `basis utile`, `holder concentration aggiornata`, `OI token-specific cross-venue completo`
- confidenza preliminare: `media`

## 1. Executive view
La tesi fondamentale ereditata e semplice: `business quality alta`, `token quality alta`, `verdict fondamentale fairly priced`, con rischio principale nella supply discipline e nella dipendenza dai volumi.
Il setup attuale e coerente con quella tesi: i timeframe reali mostrano continuazione rialzista da `4h` a `1h`, con compressione di breve sotto i massimi locali.
Bias principale: `HTF costruttivo, MTF e LTF in continuazione ma gia vicini alla parte alta del range`.
Migliore espressione: `swing long`.
Timeframe dominante della view: `4h / 1h`.
Motivo principale: i candles ufficiali di Hyperliquid mostrano una struttura in progressione `HH/HL`, funding perp lieve e non eccessivo, esecuzione buona.
Rischio principale contro la view: breakout failure sopra `~42.26` e ritorno sotto `~41.68-41.74`, che trasformerebbe il long in chase sbagliato.
Grado di eseguibilita: `medio`.

## 2. Higher timeframe context
Osservazioni visibili:
- `1W` Hyperliquid API, ultime settimane complete:
  - `36.019 -> 38.816` sui close settimanali piu recenti completi
  - settimana corrente live: `open 38.792`, `high 42.263`, `low 38.184`, `last ~42.114`
- `1D` Hyperliquid API, ultime giornate complete:
  - close recenti: `36.296 -> 38.638 -> 38.816 -> 39.477`
  - giornata corrente live: `high 42.263`, `low 39.44`, `last ~42.106`
- ATH storico disponibile: `$59.30`.

Inferenze operative:
- Il weekly non ha ancora confermato breakout strutturale in close, ma sta chiaramente facendo un reclaim della parte alta del range delle ultime settimane.
- Il daily e in espansione e sta trattando sopra i close recenti; la forza e reale, ma il breakout daily e ancora live e non va trattato come close confermato.
- Il contesto HTF quindi e `bullish`, ma non in discount: stiamo comprando forza, non debolezza.

Livelli chiave visibili:
- supporto HTF attuale: `~38.18` (low della settimana corrente)
- supporto daily piu vicino: `~39.44`
- resistenza / high live immediato: `~42.26`
- resistenza HTF successiva visibile: `~43.76` (vecchio high weekly)
- riferimento estremo: `ATH 59.30`

Premium o discount rispetto al range HTF:
- rispetto al range settimanale attuale, HYPE tratta in `premium`, non in discount.

Invalidazione della lettura HTF:
- la lettura HTF perde forza se il reclaim fallisce e il prezzo torna sotto `~38.18` su base daily.

## 3. Mid timeframe structure
Osservazioni visibili:
- `4H` Hyperliquid API, ultime chiusure complete:
  - `38.843 -> 39.581 -> 40.071 -> 39.477 -> 40.173 -> 40.06 -> 41.161 -> 41.722`
  - candle live attuale: `high 42.253`, `last ~42.111`
- Il pivot piu importante del recente leg up e il passaggio da `~40.06` a `~41.16`, poi `~41.72`.

Inferenze operative:
- La struttura `4H` e costruttiva: c e una sequenza di higher lows e higher highs con momentum in accelerazione.
- Il mercato ha gia reclaimato l area `~40.0-40.4` e ora sta comprimendo sotto `~42.26`.
- Il `4H` e allineato con l HTF: non mostra distribuzione, mostra continuazione.

Invalidazione della tesi timeframe medio:
- per il bias bullish, la prima invalidazione utile e perdere `~41.04` su base `4H`
- la rottura piu seria della struttura media sarebbe una perdita di `~39.44`

## 4. Lower timeframe timing
Osservazioni visibili:
- `1H` Hyperliquid API, ultime chiusure complete:
  - `40.06 -> 40.427 -> 40.983 -> 40.935 -> 41.161 -> 41.195 -> 41.529 -> 42.061 -> 41.722 -> 42.121`
- `15m` Hyperliquid API, ultime candele:
  - range locale visibile `~41.686 - 42.263`
- `1H` Bybit perp cross-check:
  - ripresa da `~41.095` a `~42.052`
  - pullback intermedio a `~41.69`
  - massimo recente `~42.30`

Inferenze operative:
- Il `1H` conferma trend e non conflitto: il pullback e stato assorbito, non ha rotto struttura.
- Il `15m` mostra compressione sotto i massimi locali. Questo e un contesto da continuation trade, non da short facile.
- Il rischio di chase resta reale se si entra nel mezzo del micro-range.

Timing migliore:
- `su pullback` verso `~41.68-41.74` se assorbito bene
- `su reclaim/acceptance` sopra `~42.26-42.30`
- `non subito a mercato` nel mezzo del range corto

## 5. Derivatives e positioning
Fatti verificabili:
- Bybit `HYPEUSDT` ticker:
  - `lastPrice 42.039`
  - `indexPrice 42.083`
  - `markPrice 42.052`
  - `fundingRate 0.00003532`
  - `openInterest 5,465,922.28 HYPE`
  - `turnover24h ~$167.95M`
- A mark price attuale, l OI Bybit equivale a circa `~$230M` notional.
- CoinGecko token volume `24h ~$280.6M`.
- DefiLlama protocol OI `~$7B+` resta dato di ecosistema, non proxy pulito del perp HYPE.

Inferenze operative:
- Funding positivo ma molto contenuto: segnala bias long leggero, non euforia evidente.
- Mark e index sono quasi allineati: non c e dislocazione evidente da perp overheated.
- Il positioning quindi `supporta moderatamente` il long, ma non lo rende crowded in modo chiaro.

Limiti residui:
- basis storica poco utile qui
- mancano liquidation clusters token-specific affidabili
- mancano borrow cost e short availability completi

Conclusione operativa:
- i derivati non contraddicono il long
- il carry non penalizza in modo materiale la view long tattica
- non vedo un contesto da short squeeze estremo, ma nemmeno un crowded long da evitare a priori

## 6. Liquidity e execution quality
Fatti verificabili:
- Hyperliquid `l2Book` ufficiale su `@107`:
  - spread immediato `~0.001`
  - top 20 bids `~$171.6k`
  - top 20 asks `~$177.1k`
- Bybit perp book:
  - best bid / ask `42.039 / 42.040`
  - top 10 bids `~$23.0k`
  - top 10 asks `~$9.4k`
- CoinGecko multi-venue spot:
  - Hyperliquid `HYPE/USDC`: volume `~$44.2M`
  - spread molto stretto anche su Gate / OKX / Bybit / Coinbase
  - depth `+/-2%` buona sulle principali venue CEX

Inferenze operative:
- La liquidita spot e reale. Questo non e un token microcap difficile da eseguire.
- Per size piccole e medie la view e eseguibile bene.
- Per size piu aggressive, il token resta eseguibile ma va trattato come mercato multi-venue e non solo come single-book su Hyperliquid spot.
- Ci sono livelli magnete evidenti: `41.68-41.74` come supporto intraday e `42.26-42.30` come trigger di breakout.

Giudizio di esecuzione:
- la view e `eseguibile bene`
- il timing richiede disciplina, ma non e piu il collo di bottiglia principale come nel file precedente

## 7. Spot / positional case
- espressione spot: `hold if already in / accumulate on pullbacks`
- timeframe dominante: `positional multi-week`
- coerenza con la tesi fondamentale: `coerente`
- cosa rende sensato il caso spot:
  - il contesto fondamentale resta buono
  - il token ha liquidita sufficiente e value accrual reale
  - i timeframe reali confermano che il trend di medio non si e deteriorato
- cosa lo invalida:
  - perdita netta di momentum con ritorno sotto `~38.18`
  - deterioramento di volumi/revenue o supply discipline
- cosa migliorerebbe la tesi:
  - pullback ordinato che difende `~39.4-40.0`
  - close daily sopra `~42.26`, poi attacco a `~43.76`
- cosa la peggiorerebbe:
  - comprare forza cieca mentre il token resta `fairly priced` e gia in premium di breve

## 8. Swing long case
- trigger long:
  - `breakout long` solo su acceptance `15m/1h` sopra `~42.26-42.30`
  - `pullback long` solo se la zona `~41.68-41.74` tiene e il prezzo torna sopra `~42.0`
- livello o zona di entrata:
  - breakout: `sopra 42.30 dopo conferma`
  - pullback: `41.68-41.74` con tenuta visibile
- invalidazione:
  - tattica: fallimento del breakout e perdita di `~41.68`
  - strutturale: perdita di `~41.04` su `4H`
- primi target:
  - per il pullback long: ritorno a `~42.26`
  - per il breakout long: `~43.76` come primo target HTF visibile
- timeframe dominante: `4h / 1h`
- condizione che trasformerebbe il long in no trade:
  - prezzo in mezzo al range `41.8-42.2` senza trigger
  - rifiuto ripetuto sopra `42.26` con chiusure `1H` di nuovo sotto `41.68`

## 9. Swing short case
Non compilato.
Motivo: la struttura `4H/1H` e rialzista, il funding non e abbastanza tirato per cercare uno short tattico con edge evidente, e il mercato non mostra ancora segni chiari di exhaustion.

## 10. No-trade test
- il setup e troppo sporco? `no`
- il risk/reward e insufficiente? `solo se si compra a mercato nel mezzo del range`
- la liquidita o il positioning peggiorano troppo l esecuzione? `no`
- la view e piu teorica che praticabile? `no`
- aspettare darebbe un setup migliore? `si, ma dentro una view long, non per forza in no-trade`

## 11. Decisione finale
- verdict fondamentale ereditato: `fairly priced`
- bias HTF: `bullish`
- bias operativo: `bullish`
- migliore espressione: `swing long`
- timeframe dominante della tesi: `4h / 1h`
- coerenza con la tesi fondamentale: `alta`
- conviction: `media`
- eseguibilita: `media`
- invalidation della tesi: `fallimento del breakout sopra 42.26-42.30 e perdita di 41.68; invalidazione piu seria su 4H sotto 41.04`
- se spot: `hold if already in; meglio accumulare su pullback piuttosto che inseguire`
- se swing: `long solo su acceptance sopra 42.26-42.30 o su pullback che difende 41.68-41.74; primo target visibile 43.76`
- motivo principale del verdetto: `Con i candles ufficiali di Hyperliquid il quadro non e piu un proxy: da 4h a 15m HYPE mostra continuazione rialzista con compressione sotto i massimi locali. Il funding perp e positivo ma lieve, quindi non vedo crowding tale da invalidare il long. La view giusta non e comprare a caso, ma esprimere un swing long disciplinato su trigger reali.`
