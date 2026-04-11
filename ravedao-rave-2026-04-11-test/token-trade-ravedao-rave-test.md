# Test Prompt: `token-trade-prompt.md`

## Input usato
- `[NOME/TICKER]`: `RaveDAO / RAVE`
- Report fondamentale usato:
  - `token-research-ravedao-rave-test.md`
  - `token-research-ravedao-rave-verification.md`
- Data snapshot principale: `2026-04-11`
- Timestamp mercato usato:
  - `2026-04-10 23:05 UTC`
  - `2026-04-11 01:05 Europe/Rome`
- Fonti market snapshot:
  - `Kraken Spot API`: `OHLC` su `RAVEUSD` per `15m / 1h / 4h / 1d / 1w`
  - `Kraken Spot API`: `Ticker`, `Depth`
  - `Coinbase Exchange API`: `product`, `ticker`, `book`
  - `Binance Futures API`: `exchangeInfo`, `premiumIndex`, `openInterest`, `openInterestHist`, `fundingRate`, `depth`, `klines`
  - report fondamentale e report di verifica come contesto ereditato prevalente

---

# Output del prompt

## 0. Market status
- qualita dei chart: `alta`
- copertura dati: `parziale`
- timeframe disponibili: `1w / 1d / 4h / 1h / 15m`
- report fondamentale disponibile: `si`
- report di verifica disponibile: `si`
- qualita del contesto ereditato: `alta`
- principali buchi informativi: `liquidation map precisa cross-exchange`, `borrow / short availability`, `basis storica completa`, `book depth cross-venue completa oltre i primi livelli`, `dati funding / OI all-exchange consolidati con fonte primaria unica`
- confidenza preliminare: `media`

## 1. Recent event e regime shock audit
Ultimi `90d`
- evento: `Coinbase roadmap -> Coinbase access`
- data: `2026-02-04` roadmap, `2026-02-11` access / availability
- fonte: `Coinbase Markets`, `Coinbase product page`, report di verifica
- stato: `confermato`
- cosa e confermato: `RAVE` e stato aggiunto alla roadmap e poi reso disponibile sull ecosistema Coinbase
- cosa resta allegation o non chiuso: quanto dell attuale rerating dipenda ancora da questo catalyst e quanto sia puro reflexive follow-through
- market reaction osservata: miglioramento di accesso, liquidita e legittimazione di venue; il move attuale pero e molto piu grande del solo catalyst iniziale
- impatto su business / token / market structure / fiducia: `token + market structure`
- l evento e chiuso o ancora aperto?: `chiuso come fatto, aperto come effetto sul pricing`
- il setup corrente sembra tecnico o event-driven?: `originato da evento, poi trasformato in squeeze tecnico`

Ultimi `30d`
- evento: nessun announcement primario materialmente thesis-changing trovato nelle fonti ufficiali consultate
- data: `nessuna data singola dominante`
- fonte: `RaveDAO site`, `PLVR`, report di verifica
- stato: `confermato`
- cosa e confermato: non emergono exploit, halt, dispute di governance, parameter changes o shock regolatori materiali nelle fonti primarie consultate
- cosa resta allegation o non chiuso: il motivo preciso dell accelerazione estrema del prezzo nelle ultime sedute
- market reaction osservata: da `Kraken 1D`, il token passa da area `~0.249-0.315` a `~1.58+` in pochi giorni, con due daily impulsive consecutive e volume enorme
- impatto su business / token / market structure / fiducia: `market structure + token`
- l evento e chiuso o ancora aperto?: `ancora aperto come regime di prezzo`
- il setup corrente sembra tecnico o event-driven?: `overshoot da euforia / repricing di market structure`

Ultimi `7d`
- evento: breakout verticale e nuovo `ATH`
- data: `2026-04-09 / 2026-04-10`
- fonte: `Kraken Spot API`, `CoinGecko`, `Binance Futures API`
- stato: `confermato`
- cosa e confermato: su `Kraken 1D` il token chiude `2026-04-09` a `~1.0005` dopo high `~1.0967`, poi il `2026-04-10` estende fino a `~1.747` high e tratta `~1.58-1.59` nello snapshot live
- cosa resta allegation o non chiuso: se il move stia ancora pulendo supply illiquida oppure se sia gia entrato in fase distributiva
- market reaction osservata: `Kraken` spot `~1.5819`, `Coinbase` spot `~1.583`, `Binance` perp mark `~1.5637`; volumi molto alti su spot e perp; funding Binance passato da fortemente positivo a negativo e poi quasi flat
- impatto su business / token / market structure / fiducia: `market structure + token`
- l evento e chiuso o ancora aperto?: `ancora aperto`
- il setup corrente sembra tecnico o event-driven?: `nettamente event-driven / squeeze-driven`

Mini verdict
- `evento materiale ancora aperto`
- impatto principale: `market structure / token`
- stato: `in evoluzione`

## 2. Executive view
La tesi fondamentale ereditata e `sopravvalutato`, con token quality `bassa` e forte dipendenza da narrativa / float scarcity piu che da value accrual.
Il setup tecnico di breve non conferma quella tesi nel timing: il chart e ancora forte, ma troppo esteso per un long pulito e ancora troppo instabile per uno short elegante.
Bias principale: `neutral`.
Migliore espressione: `no trade`.
Timeframe dominante della view: `4h / 1d`.
Motivo principale: trend ancora rialzista ma in pieno regime verticale post-squeeze, con risk/reward mediocre sia sul chase long sia sul fade short.
Rischio principale contro la view: breakout con acceptance sopra `~1.67` e poi `~1.75` che prolunga la reflexivity.
Grado di eseguibilita: `medio`.

## 3. Higher timeframe context
Osservazioni visibili
- `1W` Kraken:
  - settimana precedente completa: `open ~0.2362`, `high ~0.3395`, `low ~0.2252`, `close ~0.3150`
  - settimana corrente live: `open ~0.3162`, `high ~1.7470`, `low ~0.2987`, `last ~1.5911`
- `1D` Kraken, ultime giornate chiave:
  - `2026-04-05`: `open ~0.2528`, `high ~0.2567`, `low ~0.2446`, `close ~0.2481`
  - `2026-04-06`: `open ~0.2492`, `high ~0.2839`, `low ~0.2490`, `close ~0.2678`
  - `2026-04-07`: `open ~0.2684`, `high ~0.3395`, `low ~0.2672`, `close ~0.3150`
  - `2026-04-08`: `open ~0.3162`, `high ~1.0967`, `low ~0.2987`, `close ~1.0005`
  - `2026-04-09`: `open ~0.9986`, `high ~1.7470`, `low ~0.9148`, `last/live ~1.5819`

Inferenze operative
- Il weekly non e solo bullish: e in `price discovery verticale`, quindi il trend primario e forte ma la leggibilita del risk/reward e bassa.
- Il daily non mostra ancora una reversal structure. Mostra una `blow-off expansion` con close ancora altissime dentro il range.
- Il regime HTF corretto non e `healthy trend lineare`; e `breakout estremo ancora non digerito`.

Livelli chiave HTF
- supporto estremo / base del breakout: `~0.91-1.00`
- supporto intermedio molto importante: `~1.20-1.27`
- supporto di controllo piu vicino: `~1.39-1.47`
- supporto micro-chiave corrente: `~1.53-1.55`
- prima resistenza utile: `~1.63-1.67`
- resistenza / ATH: `~1.747`

Premium o discount rispetto al range HTF
- `RAVE` tratta in `forte premium` rispetto al range che il mercato aveva accettato fino a pochi giorni fa.
- Non c e nessun discount HTF leggibile; c e solo una compressione del rischio di continuation contro il rischio di mean reversion violenta.

Invalidazione della lettura HTF
- la lettura `trend fortissimo ma poco inseguibile` perde forza solo con:
  - `acceptance` sopra `~1.67`
  - breakout e tenuta sopra `~1.747`
- la struttura HTF si deteriora seriamente con:
  - perdita di `~1.39-1.47`
  - rischio maggiore sotto `~1.20`

## 4. Mid timeframe structure
Osservazioni visibili
- `4H` Kraken ultime strutture:
  - `0.9986 -> 1.2279 -> close ~1.0064`
  - `1.0070 -> 1.1911 -> close ~1.1121`
  - `1.1053 -> 1.3423 -> close ~1.2699`
  - `1.2683 -> 1.7470 -> close ~1.4733`
  - `1.4619 -> 1.6259 -> close ~1.5709`
  - candle live: `open ~1.5624`, `high ~1.6679`, `low ~1.5300`, `last ~1.5819`
- Non c e ancora `LH/LL` chiaro sul `4H`.
- C e pero una perdita di momentum evidente rispetto alla parte piu parabolica del move.

Inferenze operative
- Il `4H` e in consolidazione alta dopo un impulso estremo, non in breakdown confermato.
- La fascia `~1.53-1.55` e il pivot tattico piu importante del breve.
- La fascia `~1.63-1.67` e la prima area di supply che decide se il mercato resta in continuation o entra in una base piu lunga.

Conflitto o allineamento con HTF
- `4H` ancora allineato con la forza HTF, ma con momentum meno pulito.
- Quindi il contesto dice `trend up`, mentre l esecuzione dice `non inseguire in mezzo al range alto`.

Invalidazione della tesi timeframe medio
- per la lettura prudente / neutrale: reclaim e acceptance sopra `~1.67`
- per la lettura piu bearish tattica: serve perdita pulita di `~1.53`, poi conferma sotto `~1.39-1.47`

## 5. Lower timeframe timing
Osservazioni visibili
- `1H` Kraken / Binance:
  - massimo recente `~1.6679`
  - poi sequenza di close non disastrosa ma senza follow-through pulito
  - ultime ore tra `~1.53` e `~1.63`
- `15m` Kraken / Binance:
  - sell leg `~1.62 -> ~1.54`
  - rimbalzo `~1.54 -> ~1.59-1.60`
  - nessun trend micro pulito; piuttosto un `range rumoroso post-squeeze`

Inferenze operative
- Il `1H` non autorizza chase long a mercato qui.
- Il `15m` non autorizza nemmeno short aggressivo in mezzo, perche lo squeeze non e chiaramente collassato.
- Il timing migliore resta `aspettare`.

Trigger possibili
- long solo:
  - `su pullback hold` di `~1.53-1.55` con reclaim `~1.60-1.63`
  - oppure `su breakout` con acceptance sopra `~1.67 / 1.75`
- short solo:
  - `su failed reclaim` di `~1.63-1.67`
  - oppure `su breakdown` confermato sotto `~1.53`, con setup molto migliore sotto `~1.39`

Rischio di chase
- alto sul long se si compra in mezzo dopo due daily verticali
- alto sullo short se si vende senza breakdown in un asset che ha appena fatto price discovery

Timing migliore
- `aspettare`

## 6. Derivatives e positioning
Fatti verificabili
- `Binance Futures`:
  - status `TRADING`
  - contratto `PERPETUAL`
  - onboarding `2025-12-14 15:30 UTC`
- snapshot live `Binance premiumIndex`:
  - mark `~1.563654`
  - index `~1.563694`
  - estimated settle `~1.578410`
  - funding live `~+0.005%`
  - next funding `2026-04-11 00:00 UTC`
- `Binance OI` live:
  - `29,331,411` contratti
  - circa `~$45.9M` notionals usando il mark live
- `openInterestHist` Binance ultime ~55 minuti:
  - da `28.80M` a `29.35M` contratti, circa `+1.9%`
  - notional da `~$46.28M` a `~$46.03M`, quindi grossomodo `flat / leggermente down`
- funding history recente Binance:
  - `2026-04-08`: positivo fino a `~+0.1325%`
  - poi compressione
  - `2026-04-10 00:00 UTC`: `~-0.1925%`
  - `2026-04-10 08:00 UTC`: `~-0.0133%`
  - funding live ora quasi neutro / lievemente positivo

Inferenze operative
- Il long crowding piu aggressivo e gia stato in parte scaricato: funding non e piu euforico.
- Allo stesso tempo non c e ancora una lettura da short crowding estremo che regali uno squeeze long ovvio.
- Il perp non e fortemente disallineato dal suo index; quindi non c e edge evidente da basis dislocata.
- L OI in contratti sta risalendo un po mentre il prezzo consolida: segnale di ricarica leva, ma non ancora di crowding brutale.

Conclusione operativa
- il positioning non supporta un long immediato a mercato
- ma non supporta neanche uno short inseguito in assenza di breakdown
- questo e uno dei motivi principali per cui la conclusione corretta resta `no trade`

## 7. Liquidity e execution quality
Fatti verificabili
- `Kraken Spot`:
  - last `~1.5819`
  - bid / ask ticker `~1.5796 / 1.5820`
  - spread `~0.15%`
  - top 20 bid depth `~$49.8k`
  - top 20 ask depth `~$29.5k`
  - top 100 bid depth `~$286.9k`
  - top 100 ask depth `~$116.9k`
- `Coinbase Spot`:
  - last `~1.5830`
  - bid / ask `~1.5804 / 1.5821`
  - spread `~0.11%`
  - top 20 bid depth `~$3.2k`
  - top 20 ask depth `~$3.8k`
  - top 100 bid depth `~$82.2k`
  - top 100 ask depth `~$47.8k`
- `Binance Perp`:
  - mark `~1.5637`
  - best bid / ask `~1.56566 / 1.56588`
  - spread `~0.014%`
  - top 20 bid depth `~$2.8k`
  - top 20 ask depth `~$2.0k`

Inferenze operative
- La liquidita spot e sufficiente per size piccole e medie, soprattutto usando `Kraken + Coinbase`.
- La liquidita perp su Binance e ottima per spread, ma il top-book osservato non e profondissimo: serve disciplina sull execution se la volatilita accelera.
- Il mercato e tradabile, ma non e un mega-cap profondissimo; quindi gli spike possono restare violenti.

Livelli magnete / zone di liquidita
- `1.55` lato bid di controllo
- `1.53` come breakdown micro che cambia il tono
- `1.63-1.67` come fascia di decisione lato ask
- `1.747` come magnete di breakout / liquidity grab
- `1.39-1.47` come primo cluster serio di mean reversion

Giudizio di esecuzione
- la view e `eseguibile`, ma con attrito reale se si forza size o chase
- l edge oggi e peggiore della qualita tecnica del mercato

## 8. Spot / positional case
- espressione spot: `avoid`
- timeframe dominante: `daily / positional multi-week`
- coerenza con la tesi fondamentale: `alta`
- cosa rende sensato il caso spot:
  - il business non e una shell vuota
  - il weekly e ancora fortemente bullish
  - l accesso exchange e migliorato davvero negli ultimi mesi
- cosa lo invalida:
  - il token resta fundamentalmente sopravvalutato rispetto al suo waterfall
  - il prezzo e troppo esteso rispetto al range accettato solo pochi giorni fa
  - il rischio di unlock overhang nel medio resta intatto
- cosa migliorerebbe la tesi:
  - consolidazione lunga senza perdere `~1.20-1.27`
  - pullback ordinato e tenuta di `~1.39-1.47`
  - prova seria di token utility monetizzabile o buyback auditabile
- cosa la peggiorerebbe:
  - perdita di `~1.39` e soprattutto `~1.20`
  - nuova euforia senza consolidazione, che alzerebbe ancora di piu il rischio di reversal

## 9. Swing long case
Non attivo adesso.

Watchlist long condizionale
- trigger long: `pullback hold` su `~1.53-1.55` con reclaim `1H` di `~1.60-1.63`, oppure breakout con acceptance sopra `~1.67` e poi `~1.75`
- livello o zona di entrata: `su hold + reclaim`, non in mezzo al range
- invalidazione: sotto `~1.53` per il trigger tattico; invalidazione piu seria sotto `~1.39`
- primi target: `~1.67`, poi `~1.747`, poi eventuale estensione in price discovery
- timeframe dominante: `1H / 4H`
- condizione che trasformerebbe il long in no trade: reclaim senza follow-through oppure funding che torna molto positivo mentre il prezzo smette di fare progressi

## 10. Swing short case
Non attivo adesso come trade a mercato.

Watchlist short condizionale
- trigger short: `failed reclaim` della fascia `~1.63-1.67` oppure breakdown confermato sotto `~1.53`; il setup diventa molto piu interessante sotto `~1.39`
- livello o zona di entrata: `su rejection` o `su breakdown`, non nel mezzo del range attuale
- invalidazione: recovery sopra `~1.67`; invalidazione piu seria sopra `~1.75`
- primi target: `~1.53`, `~1.39-1.47`, poi `~1.20-1.27`
- timeframe dominante: `1H / 4H / 1D`
- condizione che trasformerebbe lo short in no trade: funding che torna neutro/negativo con OI che si scarica mentre il prezzo non accelera al ribasso

## 11. No-trade test
- il setup e troppo sporco? `si`
- il risk/reward e insufficiente? `si, nel punto attuale`
- la liquidita o il positioning peggiorano troppo l esecuzione? `la liquidita no, il positioning non regala edge chiaro`
- la view e piu teorica che praticabile? `si, se forzo un ingresso adesso`
- un evento ancora aperto rende il prezzo non affidabile come base operativa? `si, il squeeze / repricing e ancora aperto`
- aspettare darebbe un setup migliore? `si`

## 12. Decisione finale
- verdict fondamentale ereditato: `sopravvalutato`
- stato evento/regime: `event-driven`
- bias HTF: `bullish`
- bias operativo: `neutral`
- migliore espressione: `no trade`
- timeframe dominante della tesi: `4h / 1d`
- coerenza con la tesi fondamentale: `media`
- conviction: `media`
- eseguibilita: `media`
- invalidation della tesi:
  - `bullish invalidation` del no-trade: acceptance sopra `~1.67` e breakout / tenuta sopra `~1.747`
  - `bearish invalidation` della neutralita: perdita netta di `~1.53` e soprattutto `~1.39`
- se spot: `avoid fresh spot here; al massimo hold parziale solo se gia dentro con grossi cushion e disciplina`
- se swing: `n.a. adesso; aspettare o un pullback hold + reclaim o una rejection / breakdown molto piu pulita`
- motivo principale del verdetto in massimo 3 frasi:
  - `RAVE` ha un chart ancora forte ma troppo esteso rispetto al suo profilo fondamentale e al suo range accettato fino a pochi giorni fa.
  - Il positioning non e piu abbastanza sbilanciato da rendere ovvio ne il long di continuation ne lo short di mean reversion.
  - In questo punto il mercato e tradabile solo teoricamente: il capitale si difende meglio aspettando o `acceptance sopra 1.67/1.75` o una rottura vera sotto `1.53/1.39`.
