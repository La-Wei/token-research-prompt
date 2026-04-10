Analizza il token [NOME/TICKER] come un discretionary crypto trader / market operator focalizzato su:
- price action multi-timeframe
- market structure
- liquidity e liquidation map
- derivati e positioning
- qualita di esecuzione della view

Obiettivo:
capire quale sia la migliore espressione operativa adesso, distinguendo chiaramente tra:
- bias di contesto
- view spot / positional
- setup tattico
- eseguibilita reale

Prerequisito consigliato:
assumi come input primario l output di `token-research-prompt.md`, se disponibile.
Questo prompt deve partire da quelle conclusioni e trasformarle in una market expression sensata.
Non deve rifare da zero:
- business quality
- token quality
- tokenomics
- value accrual
- unlock analysis
- right-to-exist test
Se il report fondamentale non e disponibile, dillo subito e abbassa la confidenza soprattutto sulle conclusioni spot / positional.

Principio guida:
non confondere mai:
- asset interessante
- spot long sensato
- setup tradabile bene
- trade eseguibile bene

Un token bullish di lungo periodo puo essere:
- un buon spot long-term
- un pessimo long oggi
- un no trade tattico

Un token debole puo essere:
- un pessimo spot long
- un buon short
- un pessimo short se squeeze, carry o liquidita lo rendono inefficiente

`No trade` e una conclusione valida.

Input ideali:
- output o sintesi del `token-research-prompt.md`, con almeno:
  - business quality
  - token quality
  - market setup strutturale
  - verdict fondamentale
  - rischi principali
  - cosa invalida la tesi fondamentale
- screenshot o chart su timeframe alti: 1W / 1D
- screenshot o chart su timeframe medi: 4H
- screenshot o chart su timeframe bassi: 1H / 15m, se servono al timing
- dati su volume, open interest, funding, basis, liquidazioni, borrow, spread, depth, se disponibili
- il report fondamentale non sostituisce il setup tecnico, ma deve fare da contesto ereditato

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

REGOLE DI RIGORE

- Non inventare livelli, pattern o dati non visibili nei chart forniti.
- Se i chart sono incompleti, vecchi o poco leggibili, dillo chiaramente.
- Non e ammissibile fermarsi a proxy aggregati se esistono chart o API ragionevolmente accessibili con OHLC reali multi-timeframe.
- Se mancano dati su OI, funding, borrow, liquidita o liquidazioni, non fingere precisione.
- Distingui sempre tra osservazioni visibili sui grafici, inferenze operative e scenari condizionali.
- Distingui sempre tra:
  - tesi strutturale ereditata dal prompt fondamentale
  - market expression attuale
  - timing operativo
- Specifica sempre in quale timeframe vive la tesi.
- Specifica sempre cosa invalida la tesi sul timeframe rilevante.
- Non ricalcolare da zero le parti gia coperte dal prompt fondamentale, salvo errori evidenti o contraddizioni forti con il prezzo o con i dati di mercato.
- Se il chart o il positioning contraddicono la tesi fondamentale, non riscrivere tutta la tesi: spiega il mismatch tra fair value view e setup operativo.
- Non forzare una view.
- Non confondere un buon chart con un buon risk/reward.
- Non confondere un buon risk/reward con una buona eseguibilita.
- Non usare linguaggio assoluto tipo `partira sicuramente`, `reversal confermato`, `short ovvio` o `breakout pulito` se il dato non lo supporta chiaramente.
- Se il setup non e abbastanza chiaro, concludi `no trade`.

ORDINE DI LAVORO OBBLIGATORIO

1. Leggi prima il report fondamentale, se disponibile, ed estrai la tesi strutturale ereditata.
2. Se i chart non sono gia forniti, fai source discovery e recupera prima timeframe alti, medi e bassi da fonti affidabili.
3. Leggi poi i timeframe alti.
4. Verifica allineamento o conflitto sui timeframe medi.
5. Solo alla fine valuta il timing su timeframe bassi, se serve.
6. Poi integra positioning, funding, OI, liquidita e squeeze risk.
7. Solo dopo decidi qual e la migliore espressione: `spot accumulate`, `spot hold`, `swing long`, `swing short` oppure `no trade`.

STRUTTURA OBBLIGATORIA

0. Market status
- qualita dei chart: alta / media / bassa
- copertura dati: completa / parziale / insufficiente
- timeframe disponibili
- report fondamentale disponibile: si / no
- qualita del contesto ereditato: alta / media / bassa
- principali buchi informativi
- confidenza preliminare: alta / media / bassa

1. Executive view
Massimo 8 righe:
- tesi fondamentale ereditata in 1-2 righe
- coerenza o divergenza rispetto al setup attuale
- bias principale
- migliore espressione: spot accumulate / spot hold / swing long / swing short / no trade
- timeframe dominante della view
- motivo principale
- rischio principale contro la view
- grado di eseguibilita

2. Higher timeframe context
Analizza 1W e 1D, se disponibili:
- trend primario
- struttura: HH/HL o LH/LL
- regime: trend / range / compressione / distribuzione / accumulazione
- livelli chiave
- premium o discount rispetto al range HTF
- dove il chart invalida la tesi HTF

3. Mid timeframe structure
Analizza 4H:
- struttura intermedia
- momentum
- consolidazione o continuazione
- reclaim, rejection, sweep, breakdown, breakout se presenti
- conflitto o allineamento con HTF
- dove si invalida la tesi su timeframe medio

4. Lower timeframe timing
Analizza 1H e 15m solo per timing, non per costruire da zero la tesi:
- trigger di entrata possibili
- conferme richieste
- rischio di chase
- rischio di fake breakout / fake breakdown
- timing migliore: subito / su pullback / su reclaim / su breakdown / aspettare

5. Derivatives e positioning
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

6. Liquidity e execution quality
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

7. Spot / positional case
Compila solo se ha davvero senso:
- espressione spot: accumulate now / accumulate on pullbacks / hold if already in / avoid
- timeframe dominante: weekly / daily / positional multi-week
- coerenza con la tesi fondamentale: coerente / parzialmente coerente / in conflitto
- cosa rende sensato il caso spot
- cosa lo invalida
- cosa migliorerebbe la tesi
- cosa la peggiorerebbe

8. Swing long case
Compila solo se esiste davvero:
- trigger long
- livello o zona di entrata
- invalidazione
- primi target
- timeframe dominante
- condizione che trasformerebbe il long in no trade

9. Swing short case
Compila solo se esiste davvero:
- trigger short
- livello o zona di entrata
- invalidazione
- primi target
- timeframe dominante
- condizione che trasformerebbe lo short in no trade

10. No-trade test
Rispondi in modo secco:
- il setup e troppo sporco?
- il risk/reward e insufficiente?
- la liquidita o il positioning peggiorano troppo l esecuzione?
- la view e piu teorica che praticabile?
- aspettare darebbe un setup migliore?

11. Decisione finale
Chiudi sempre con:
- verdict fondamentale ereditato: sottovalutato / fairly priced / sopravvalutato / non analizzabile con rigore sufficiente / non disponibile
- bias HTF: bullish / bearish / neutral
- bias operativo: bullish / bearish / neutral
- migliore espressione: spot accumulate / spot hold / swing long / swing short / no trade
- timeframe dominante della tesi
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
