# Test Prompt: `token-trade-prompt.md`

## Input usato
- `[NOME/TICKER]`: `Bittensor / TAO`
- Report fondamentale usato:
  - `token-research-bittensor-tao-test.md`
  - `token-research-bittensor-tao-verification.md`
- Data snapshot principale: `2026-04-10`
- Fonti market snapshot:
  - `Binance Spot API`: `klines` su `TAOUSDT` per `15m / 1h / 4h / 1d / 1w`
  - `Binance Spot API`: `bookTicker` e `depth`
  - `Binance Futures API`: `premiumIndex`, `openInterest`, `openInterestHist`, `fundingRate`, `depth`
  - `CoinGlass`: cross-check all-exchange su prezzo, volumi, OI e liquidazioni
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
- principali buchi informativi: `liquidation map precisa`, `basis storica`, `borrow / short availability`, `depth cross-venue completa`, `funding history cross-exchange`
- confidenza preliminare: `media`

## 1. Recent event e regime shock audit
Ultimi `90d`
- evento: rally AI e rerating del network
- data: marzo 2026
- fonte: `The Block`, model card `Covenant-72B`, report fondamentale / verifica
- stato: `confermato`
- cosa e confermato: TAO ha quasi raddoppiato in marzo mentre il mercato ha iniziato a prezzare il progresso del network e la credibilita del distributed training
- cosa resta allegation o non chiuso: quanto di quel rally fosse giustificato da business proof vs semplice narrative expansion
- market reaction osservata: rally molto forte nel mese, culminato poi nell estensione verso `~377.8` high spot su Binance
- impatto su business / token / market structure / fiducia: `token + narrativa + fiducia`
- l evento e chiuso o ancora aperto?: `parzialmente chiuso`
- il setup corrente sembra tecnico o event-driven?: `il rally precedente era in parte narrative-driven`

Ultimi `30d`
- evento: `Covenant-72B` come prova tecnica forte
- data: `2026-03-09 / 2026-03-10`
- fonte: `Hugging Face model card`
- stato: `confermato`
- cosa e confermato: modello `72B`, `1.1T` token di training, `20+` participant compute, benchmark `MMLU 67.11`
- cosa resta allegation o non chiuso: che il successo tecnico si traduca in monetizzazione esterna e accrual piu pulito per TAO
- market reaction osservata: forte rerating nel mese, ma non isolabile con rigore da sola sul chart
- impatto su business / token / market structure / fiducia: `business + token + narrativa`
- l evento e chiuso o ancora aperto?: `chiuso come fatto tecnico, aperto come implicazione economica`
- il setup corrente sembra tecnico o event-driven?: `il suo effetto e stato in gran parte assorbito nel rally di marzo`

- evento: `BIP-023` emission rebalance
- data: `2026-03-22`
- fonte: `vote-bittensor.xyz`
- stato: `in evoluzione`
- cosa e confermato: proposta di cambiare lo split da `41 / 41 / 18` a `38 / 44 / 18`
- cosa resta allegation o non chiuso: stato finale / implementazione effettiva, dato che la pagina mostra metadati temporali non perfettamente coerenti
- market reaction osservata: non isolabile in modo pulito dal resto del move
- impatto su business / token / market structure / fiducia: `token + governance`
- l evento e chiuso o ancora aperto?: `ancora aperto`
- il setup corrente sembra tecnico o event-driven?: `contribuisce al regime policy-driven, ma non spiega da solo il move`

Ultimi `7d`
- evento: uscita di `Covenant AI` e shock di governance
- data: `2026-04-09`
- fonte: `The Block`, report di verifica
- stato: `confermato come evento, contestato nel merito di parte delle accuse`
- cosa e confermato: team importante del network lascia Bittensor e accusa il progetto di `decentralization theatre`
- cosa resta allegation o non chiuso: sospensione unilaterale delle emissions e piena natura dei poteri effettivi del founder / triumvirate
- market reaction osservata: su `CoinGlass` `TAO ~$268.49`, `-19.78%` 24h, `futures vol ~$3.79B`, `spot vol ~$592.22M`, `OI ~$461.97M`, `liq 24h ~$12.03M`; su Binance spot il dump porta il prezzo fino a `~248.9`
- impatto su business / token / market structure / fiducia: `fiducia + market structure + token`
- l evento e chiuso o ancora aperto?: `ancora aperto`
- il setup corrente sembra tecnico o event-driven?: `nettamente event-driven`

- evento: risposta di `Jacob Steeves`
- data: `2026-04-10`
- fonte: `The Block`
- stato: `confermato`
- cosa e confermato: Steeves nega di poter sospendere le emissions
- cosa resta allegation o non chiuso: il grado reale di controllo politico / sociale sulla rete
- market reaction osservata: nessuna normalizzazione piena; il prezzo rimbalza dal panic low ma resta molto sotto le aree di breakdown
- impatto su business / token / market structure / fiducia: `fiducia`
- l evento e chiuso o ancora aperto?: `ancora aperto`
- il setup corrente sembra tecnico o event-driven?: `event-driven in digestione tecnica`

Mini verdict
- `evento materiale ancora aperto`
- impatto principale: `fiducia / market structure`
- stato: `in evoluzione`

## 2. Executive view
La tesi fondamentale ereditata e `fairly priced`, con `market setup fragile` e governance discount reale.
Il setup attuale non contraddice quella tesi: il chart non mostra sottovalutazione evidente, mostra piuttosto un mercato che sta ancora digerendo uno shock di fiducia.
Bias principale: `neutral con rischio di ulteriore downside se i livelli di panic low cedono`.
Migliore espressione: `no trade`.
Timeframe dominante della view: `1d / 4h`.
Motivo principale: breakdown daily gia avvenuto, evento ancora aperto, funding ormai negativo e OI in bleed, quindi l edge sia sul long sia sullo short e mediocre nel punto attuale.
Rischio principale contro la view: un reclaim rapido sopra `~274` e poi `~283-293` che trasformi il post-shock in bear trap.
Grado di eseguibilita: `medio`.

## 3. Higher timeframe context
Osservazioni visibili
- `1W` Binance:
  - settimana precedente completa: `open ~315.5`, `high ~335.3`, `low ~292.6`, `close ~310.2`
  - settimana corrente live: `open ~310.2`, `high ~351.1`, `low ~248.9`, `last ~261.4-261.6`
- `1D` Binance, ultime giornate chiave:
  - `2026-04-05`: `close ~312.9`
  - `2026-04-06`: `close ~335.4`
  - `2026-04-07`: `close ~325.1`
  - `2026-04-08`: `close ~305.1`
  - `2026-04-09`: `low ~248.9`, `close ~261.4`
  - `2026-04-10` live: rebound parziale ma nessun reclaim serio delle aree rotte

Inferenze operative
- Il weekly non e ancora una struttura di crollo totale di lungo periodo, ma il candle in corso e chiaramente un `failed continuation` / `outside reversal` molto sporco.
- Il daily ha gia rotto la zona di supporto `~292.6-305`, che prima faceva da area di accettazione del rally.
- Quindi il regime HTF non e piu `trend pulito`. E piu corretto leggerlo come `breakdown da event shock dentro un contesto ancora sopra i minimi di marzo`.

Livelli chiave HTF
- supporto estremo visibile: `~248.9`
- supporto intermedio: `~257-260`
- prima resistenza utile: `~273.8-274.3`
- resistenza piu importante: `~283-293`
- supply / invalidation piu forte del breakdown: `~305-310`
- supply alta: `~335-351`

Premium o discount rispetto al range HTF
- TAO tratta in `discount` rispetto al top del rally, ma non in `discount pulito`: il prezzo e scontato perche il mercato ha introdotto un governance discount, non per semplice mean reversion meccanica.

Invalidazione della lettura HTF
- la lettura prudente / neutrale-bearish perde forza con `reclaim daily` sopra `~283-293`
- un ritorno sopra `~305-310` trasformerebbe il post-shock in bear trap molto piu seria

## 4. Mid timeframe structure
Osservazioni visibili
- `4H` Binance:
  - dump fino a `~248.9`
  - rimbalzo fino a `~274.3`
  - poi nuova rotazione down con ultime aree battute tra `~259` e `~269`
- le ultime `4H` non mostrano ancora una sequenza pulita di `HH/HL`; mostrano piuttosto un range sporco post-shock con lower highs locali

Inferenze operative
- Il `4H` non e ancora un long trend resettato. E una struttura di digestione dopo una dislocazione violenta.
- Il massimo di reazione `~273.8-274.3` e il livello tecnico piu importante del breve: finche non viene recuperato, il rimbalzo resta solo reattivo.
- Il range di lavoro del `4H` adesso e grosso modo `~249-274`, con pivot intermedio `~259-261`.

Conflitto o allineamento con HTF
- `4H` e allineato con la prudenza HTF: nessun segnale di inversione strutturale ancora confermato

Invalidazione della tesi timeframe medio
- per la lettura prudente: `4H acceptance` sopra `~274`
- per la lettura bearish: perdita pulita di `~257` e poi di `~248.9`

## 5. Lower timeframe timing
Osservazioni visibili
- `1H` Binance:
  - rimbalzo fino a `~273.8`
  - poi lower highs successivi e ritorno verso `~261-265`
- `15m` Binance:
  - micro struttura sporca
  - ultimo sell leg da `~265.9` verso `~261.4`
  - nessun reclaim netto nel micro

Inferenze operative
- Il `1H` non autorizza chase long qui.
- Il `15m` non offre neanche uno short pulito a mercato, perche il dump e gia avvenuto e la leva si sta scaricando.
- Il timing migliore adesso e `aspettare`.

Trigger possibili
- long solo `su reclaim` di `~268.5-274` con conferma `1H`
- long piu serio solo sopra `~283`
- short solo `su failed reclaim` verso `~268-274` oppure `su breakdown` sotto `~257 / 248.9`, non nel mezzo

Rischio di chase
- alto sul long se si compra in mezzo senza reclaim
- medio-alto sullo short se si vende dopo un funding gia negativo e dopo flush importante

Timing migliore
- `aspettare`

## 6. Derivatives e positioning
Fatti verificabili
- `CoinGlass` all-exchange snapshot:
  - prezzo `~$268.49`
  - futures volume `~$3.79B`
  - spot volume `~$592.22M`
  - OI `~$461.97M`
  - liquidazioni 24h `~$12.03M`
- `Binance Futures` live:
  - mark `~261.44`
  - index `~261.58`
  - funding live `~-0.0378%`
  - OI `351,405 TAO`, circa `~$91.9M` notional
- funding recenti su Binance:
  - le ultime letture sono virate decisamente negative fino a `~-0.0857%` e `~-0.0656%`
- `openInterestHist` Binance ultime ~2 ore:
  - OI in token `-2.08%`
  - OI notional `-3.68%`

Inferenze operative
- Il positioning dice che il long crowding iniziale e stato gia colpito e che ora il mercato sta iniziando a prezzare anche short crowding tattico.
- Mark e index sono quasi allineati, quindi non c e una dislocazione perp estrema che regali edge ovvio.
- Funding negativo e OI in calo significano che lo short non ha piu il profilo pulito del primo impulso del breakdown.

Conclusione operativa
- il positioning non supporta un long immediato
- ma non supporta neanche uno short inseguito a mercato
- questo e uno dei motivi principali per cui la conclusione giusta resta `no trade`

## 7. Liquidity e execution quality
Fatti verificabili
- `Binance Spot`:
  - best bid / ask `261.4 / 261.5`
  - spread `~0.038%`
  - top 20 bid depth `~$534k`
  - top 20 ask depth `~$516k`
  - wall evidente lato ask attorno a `262`
  - bids piu densi attorno a `260.0` e `259.8`
- `Binance Futures`:
  - best bid / ask `261.22 / 261.23`
  - spread `~0.0038%`
  - top 20 bid depth `~$67.1k`
  - top 20 ask depth `~$72.4k`

Inferenze operative
- La view e eseguibile bene per size piccole e medie.
- Non siamo in un mercato illiquido; il problema non e la possibilita di esecuzione, ma la qualita dell edge.
- In regime di shock, pero, la liquidita osservata a libro non elimina il rischio di gap e slippage se escono nuovi headline.

Livelli magnete / zone di liquidita
- `260 / 259.8` lato bid spot
- `262` lato ask spot
- `257` e `248.9` come magneti downside
- `274` e `283+` come zone di reclaim che cambiano davvero il tono

Giudizio di esecuzione
- la view e `eseguibile`, ma il setup resta `teoricamente tradabile meglio di quanto sia attualmente profittevole`

## 8. Spot / positional case
- espressione spot: `avoid`
- timeframe dominante: `daily / positional multi-week`
- coerenza con la tesi fondamentale: `alta`
- cosa rende sensato il caso spot:
  - la tesi fondamentale non e collassata del tutto
  - TAO resta un asset-base con una certa sostanza strutturale
  - il prezzo e molto sotto i massimi recenti
- cosa lo invalida:
  - il fatto che il shock di governance sia ancora aperto e non pienamente metabolizzato
  - la mancata riconquista di `~274` e soprattutto `~283-293`
- cosa migliorerebbe la tesi:
  - chiarimenti di governance
  - tenuta sopra `~248.9` e reclaim della fascia `~283-293`
- cosa la peggiorerebbe:
  - nuovi attriti con subnet chiave
  - rottura netta di `~248.9`

## 9. Swing long case
Non attivo adesso.

Watchlist long condizionale
- trigger long: `reclaim 1H` sopra `~274` e preferibilmente acceptance daily sopra `~283`
- livello o zona di entrata: `su reclaim`, non in mezzo al range attuale
- invalidazione: ritorno sotto `~267` per il trigger tattico; piu seria sotto `~259`
- primi target: `~283`, poi `~293-305`
- timeframe dominante: `1H / 4H / 1D`
- condizione che trasformerebbe il long in no trade: reclaim senza follow-through oppure nuovo deterioramento headlines

## 10. Swing short case
Non attivo adesso come trade a mercato.

Watchlist short condizionale
- trigger short: `failed reclaim` della fascia `~268-274` oppure breakdown pulito sotto `~257`, con rischio molto piu serio sotto `~248.9`
- livello o zona di entrata: `su rejection`, non su flush gia esteso
- invalidazione: recovery sopra `~274`; invalidazione piu seria sopra `~283`
- primi target: `~257`, `~248.9`, poi eventualmente `~235-220`
- timeframe dominante: `1H / 4H`
- condizione che trasformerebbe lo short in no trade: funding ancora piu negativo, OI che continua a scaricarsi e prezzo che smette di accelerare verso il basso

## 11. No-trade test
- il setup e troppo sporco? `si`
- il risk/reward e insufficiente? `si, nel punto attuale`
- la liquidita o il positioning peggiorano troppo l esecuzione? `la liquidita no, il positioning toglie edge allo short inseguito`
- la view e piu teorica che praticabile? `si, se forzo un ingresso adesso`
- un evento ancora aperto rende il prezzo non affidabile come base operativa? `si`
- aspettare darebbe un setup migliore? `si`

## 12. Decisione finale
- verdict fondamentale ereditato: `fairly priced`
- stato evento/regime: `structural-break risk`
- bias HTF: `neutral`
- bias operativo: `neutral`
- migliore espressione: `no trade`
- timeframe dominante della tesi: `1d / 4h`
- coerenza con la tesi fondamentale: `alta`
- conviction: `media`
- eseguibilita: `media`
- invalidation della tesi:
  - `bullish invalidation` del no-trade: reclaim sopra `~274` e soprattutto `~283-293`
  - `bearish invalidation` della neutralita: perdita netta di `~257` e poi `~248.9`
- se spot: `avoid fresh spot here; al massimo hold solo se gia dentro con size lunga e tolleranza alta alla volatilita`
- se swing: `n.a. adesso; aspettare o un reclaim credibile o una rejection molto piu pulita`
- motivo principale del verdetto in massimo 3 frasi:
  - TAO oggi non offre un edge chiaro: il breakdown daily e gia successo, ma il funding ormai negativo e l OI in bleed rendono anche lo short molto meno elegante da inseguire.
  - Il mercato resta dominato da un governance shock ancora aperto, quindi il prezzo attuale e piu `event-driven` che tecnicamente pulito.
  - La scelta corretta non e prevedere il prossimo headline, ma aspettare che il mercato scelga tra `reclaim sopra 274/283` o nuova accelerazione sotto `257/248.9`.
