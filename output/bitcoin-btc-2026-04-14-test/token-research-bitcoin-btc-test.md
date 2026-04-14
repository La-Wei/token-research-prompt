# Token Research: `Bitcoin / BTC`

## Input usato
- `[NOME/TICKER]`: `Bitcoin / BTC`
- Data snapshot principale: `2026-04-14`
- Obiettivo del test: eseguire `prompt/token-research-prompt.md` distinguendo con rigore tra qualita del network Bitcoin, qualita del token `BTC`, market structure e pricing

## Materiale minimo per l analisi

### Fonti principali
- Fonti ufficiali protocollo:
  - https://bitcoin.org/en/bitcoin-paper.html
  - https://bitcoin.org/en/
  - https://developer.bitcoin.org/devguide/transactions.html
  - https://developer.bitcoin.org/
  - https://bitcoincore.org/
- Fonti primarie / market snapshot:
  - https://www.coinbase.com/price/bitcoin
  - https://api.kraken.com/0/public/Ticker?pair=XBTUSD
  - https://mempool.space/
  - https://mempool.space/mining/pool/foundryusa
  - https://mempool.space/mining/pool/antpool
  - https://mempool.space/mining/pool/spiderpool
  - https://www.coinglass.com/currencies/BTC/futures
- Fonti istituzionali / market structure / treasury demand:
  - https://coinshares.com/us/insights/research-data/fund-flows-13-04-26/
  - https://coinshares.com/insights/research-data/bitcoin-mining-report-q1-2026/
  - https://www.strategy.com/press/strategy-acquires-13927-btc-now-holds-780897-btc_04-13-2026

### Snapshot numerico essenziale
- `Coinbase` snapshot `2026-04-14`, crawl stesso giorno:
  - prezzo spot: `$74,193.02`
  - market cap: `$1.49T`
  - FDV: `$1.56T`
  - volume 24h: `$51.279B`
  - circulating supply: `20,015,553 BTC`
  - total supply: `20,015,553 BTC`
  - max supply: `21,000,000 BTC`
  - market cap / FDV: `~0.95`
  - dominance: `60.66%`
  - performance: `24h +4.96%`, `7d +8.17%`, `30d +4.65%`, `1y -10.57%`
  - ATH mostrato: `$126,210.50` il `2025-10-06`
- `Kraken REST API` snapshot `2026-04-14`, open diretto stesso giorno:
  - last trade: `$74,727.50`
  - ask: `$74,737.40`
  - bid: `$74,737.30`
  - 24h high: `$74,966.20`
  - 24h low: `$70,691.60`
  - 24h VWAP: `$73,154.85`
- `Supply math` derivata dallo schedule post-halving:
  - nuovo issuance annuale teorico: `164,250 BTC`
  - inflazione annuale teorica sulla circulating attuale: `~0.8206%`
  - percentuale gia emessa: `~95.31%`
- `Mempool.space` snapshot recente `2026-04-13/14`:
  - fee board osservata: `~1-3 sat/vB`
  - Foundry USA 1w block share: `28.41%`
  - AntPool 1w block share: `18.52%`
  - SpiderPool 1w block share: `7.24%`
  - top 2 pool share: `46.93%`
  - top 4 pool share osservabile con pool principali selezionati: `~67.43%`
  - Foundry 144-block reward totale: `451.64 BTC`
  - average fee per block su quel sample: `~0.0114 BTC`
  - fee share sul reward totale del sample: `~0.36%`
- `CoinGlass` snapshot `2026-04-14`, dashboard crawl stesso giorno:
  - futures volume 24h: `~$44.78B`
  - spot volume 24h: `~$3.02B`
  - open interest: `~$52.17B`
  - market cap mostrata: `~$1.42T`
- `CoinShares Fund Flows` pubblicato `2026-04-13`:
  - inflows settimanali digital asset products: `~$1.1B`
  - inflows settimanali Bitcoin: `~$871M`
  - quota di Bitcoin sugli inflows totali: `~79%`
  - inflows su prodotti short-Bitcoin: `~$20.2M`
- `CoinShares Bitcoin Mining Report Q1 2026`, pubblicato `2026-03-25`:
  - weighted average cash cost dei miner pubblici in `Q4 2025`: `~$79,995/BTC`
  - hashprice in inizio `Q1 2026`: `~$29-30 / PH / day`
  - hashrate al momento della pubblicazione: `~1,020 EH/s`
  - average fees per block in `Q4 2025`: `~0.018 BTC`
  - fee income `consistently below 1%` del total block reward nel periodo descritto
- `Strategy` 8-K `2026-04-13`:
  - BTC comprati tra `2026-04-06` e `2026-04-12`: `13,927 BTC`
  - aggregate purchase price: `~$1.00B`
  - average purchase price del periodo: `$71,902`
  - aggregate holdings as of `2026-04-12`: `780,897 BTC`
  - average purchase price storico holdings: `$75,577`
  - quota sulla circulating attuale: `~3.90%`

### Punti che restano opachi
- non ho una vista primaria unica e same-timestamp su `liquid circulating supply`, saldi exchange e beneficial ownership, perche ETF, custodian e cold storage aggregano milioni di utenti
- non ho una riconciliazione primaria perfetta nello stesso minuto tra `Coinbase`, `Kraken`, `CoinGlass` e altre dashboard sullo spot globale, quindi tratto le dashboard aggregate come contesto e non come anchor finale del prezzo
- non ho una vista completa e same-timestamp su funding, basis, borrow cost e short availability cross-venue; posso solo dire che il mercato derivati e molto profondo
- non ho una misura primaria pulita del vero settlement economico netto su Bitcoin che separi pagamenti finali, self-churn, consolidamenti UTXO e movimenti inter-custodian

---

# Output del prompt

## 0. Research mode e perimetro evidenze
- qualita delle fonti: `alta`
- copertura dati: `parziale-completa`
- modalita: `full diligence`
- motivo della scelta:
  - la meccanica di Bitcoin, il ruolo del token, il fee market e lo schedule di supply sono ricostruibili con fonti primarie e documentazione tecnica
  - market snapshot e market structure sono osservabili con venue spot primarie, API pubbliche e dashboard metodologiche credibili
  - restano buchi su float reale, beneficial ownership e microstructure cross-venue completa, ma non impediscono un giudizio strutturale serio su business, token e price placement
- copertura market structure: `robusta`
- blocchi osservabili con rigore sufficiente:
  - necessita di esistenza del protocollo
  - necessita del token per il prodotto
  - waterfall economico block subsidy / transaction fees / miner revenue
  - supply cap, supply residua e net supply direction
  - assenza di unlock classici, treasury onchain e fee switch
  - profondita di mercato spot e derivati
  - recenti sviluppi di domanda istituzionale e treasury accumulation
- blocchi ancora non chiudibili:
  - exchange float reale e percentuale esatta di supply disponibile al trading
  - beneficial ownership pulita tra ETF, custodian e utenti finali
  - basis e funding cross-venue nello stesso timestamp
  - misura pulita del settlement economico netto filtrando il rumore onchain
- implicazione principale dei buchi dati:
  - il verdetto deve poggiare su struttura monetaria, qualita della supply e pricing del `monetary premium`, non su una finta precisione del float o del funding
- rischio principale di errore analitico:
  - sottostimare quanto Bitcoin venga prezzato come `global reserve asset` e sovrastimare quanto il fee market attuale debba giustificarne il market cap
- confidenza preliminare: `media`

## 1. TL;DR iniziale
- Bitcoin non e un business da leggere come equity o protocol fee machine; e un asset monetario digitale con settlement permissionless e supply rigidamente limitata.
- Il progetto deve esistere davvero se il bisogno e `scarce collateral + bearer asset + non-sovereign settlement rail`; molto meno se il bisogno e pagare il caffe piu comodamente.
- `BTC` e necessario al prodotto: senza `BTC` non esistono il security budget, la scarsita monetaria e l unita economica del sistema.
- Il punto forte del token non e il cash flow diretto ma la pulizia della supply: niente treasury di protocollo, niente unlock VC, emissione residua bassa, hard cap reale.
- Il punto debole e che il direct accrual per l holder passivo e quasi nullo: le fees vanno ai miner, non agli holder, e oggi restano piccole rispetto al block reward.
- Il mercato probabilmente non sta sottovalutando questa realta: a `~$1.49T` di market cap Bitcoin e gia prezzato come il chiaro vincitore del monetary premium crypto.
- Il bull case serio e `reserve demand + corporate / ETF accumulation + survivorship premium`, non `fee growth redistribuita agli holder`.
- Giudizio preliminare: business/protocollo di qualita alta, token di qualita alta relativa, ma sullo snapshot `2026-04-14` `BTC` appare `fairly priced`, circa al centro del corridoio base piu coerente con la tesi.

## 2. Che cosa fa davvero il protocollo
Fatti verificabili:
- Il whitepaper di Bitcoin lo definisce un sistema di `peer-to-peer electronic cash`.
- Bitcoin.org descrive Bitcoin come denaro `open-source` che opera senza autorita centrale o banche e dice esplicitamente che nessuno possiede o controlla Bitcoin.
- La documentazione developer spiega che le transazioni spendono `UTXO`, che le fees sono pagate per byte in funzione della domanda di spazio nei blocchi e che la fee va al miner.
- Coinbase descrive Bitcoin come asset digitale decentralizzato per inviare, ricevere e conservare valore senza banche o autorita centrali.

Inferenze ragionevoli:
- Il problema reale che Bitcoin risolve non e `fare un altra payment app`; e offrire un bene digitale scarso, neutrale e non sovrano che puo essere detenuto e trasferito senza dipendere da un emittente.
- Il bisogno piu forte oggi non sembra il retail payments mass-market. Sembra piuttosto:
  - collateral neutrale
  - riserva di valore digitale
  - settlement internazionale resistente alla censura
  - benchmark monetario crypto
- Per l utente finale che vuole semplicemente pagare in fretta e con UX comoda, stablecoins, banche e fintech spesso restano migliori.
- Per chi invece vuole un asset bearer, con supply predefinita e senza rischio emittente, le alternative centralizzate non replicano il prodotto.
- Se togli `BTC`, il prodotto non resta quasi identico: spariscono la scarsita, il security budget minerario e il motivo economico per usare proprio quel ledger.
- Se Bitcoin sparisse domani, il bisogno reale che resterebbe scoperto sarebbe quello di un asset digitale globale, non emesso da nessuno, con regole monetarie credibili e liquidita globale.

Confronto esplicito con alternative realistiche
- soluzione centralizzata / API tradizionale:
  - banche, PayPal, broker custodial, gold ETF, stablecoin custodial
  - vantaggio Bitcoin: self-custody, neutralita, final settlement, hard cap credibile, nessun emittente
  - svantaggio Bitcoin: UX, recupero fondi, compliance integration, velocita percepita e costo medio lato utente finale
- open source non tokenizzato:
  - software di accounting, database distribuiti, ledger permissioned
  - vantaggio Bitcoin: un software open source senza asset nativo non crea di per se un bene scarso globale; crea solo un database condiviso
  - svantaggio Bitcoin: richiede un asset volatile e un security model costoso
- soluzione locale / self-hosted / offchain:
  - utile per un operatore singolo o un consorzio
  - ma non replica bene un asset monetario globale, liquido e settlement-final senza fiduciary issuer

Vantaggio di prodotto vs vantaggio di coordinamento
- vantaggio di prodotto:
  - scarsita credibile
  - resistenza alla censura
  - self-custody
  - settlement permissionless
- vantaggio di coordinamento / capitale:
  - deepest liquidity pool del settore
  - brand e legittimazione istituzionale
  - integrazione in ETF, corporate treasuries e desks globali
  - network effect su custodia, collateral acceptance e mercato derivati

Mini verdict atomico
- necessita di esistenza del prodotto: `alta`
- vantaggio vs soluzione centralizzata/API: `medio`
- vantaggio vs open source non tokenizzato o locale: `forte`
- necessita del token per il prodotto: `alta`
- il progetto e soprattutto: `coordination/capital layer + bene monetario digitale`

## 3. Business quality: qualita reale del protocollo
Fatti verificabili:
- `Coinbase` snapshot `2026-04-14` mostra Bitcoin come asset `#1` per popolarita con market cap `~$1.49T`, dominance `60.66%` e volume 24h `~$51.28B`.
- `CoinShares` nel report del `2026-04-13` mostra `~$1.1B` di inflows settimanali nei prodotti crypto e `~$871M` solo su Bitcoin.
- `Strategy` ha comunicato l `2026-04-13` holdings pari a `780,897 BTC`, quindi una singola corporate treasury controlla circa il `3.9%` della circulating osservata da Coinbase.
- `CoinShares Bitcoin Mining Report Q1 2026` dice che l hashrate era `~1,020 EH/s` al momento della pubblicazione, nonostante hashprice molto compresso.
- `Mempool.space` mostra fee board ancora bassa e pool mining con share elevate per i primi operatori, segno di una rete economicamente viva ma con qualche concentrazione infrastrutturale.

Metric perimeter reconciliation
- `market cap` misura il valore monetario che il mercato assegna al bene, non i ricavi del protocollo.
- `ETF / ETP inflows` misurano domanda di investimento intermediata, non uso nativo del layer base.
- `hashrate` misura spesa competitiva per la sicurezza, non domanda finale da utenti paganti.
- `transaction fees` misurano domanda per blockspace, non tokenholder revenue.
- `corporate treasury holdings` misurano adozione come riserva di bilancio, non necessariamente uso come mezzo di pagamento.

Inferenze ragionevoli:
- La business quality di Bitcoin e `alta` se lo si legge per quello che e davvero:
  - bene monetario digitale
  - collateral neutrale
  - settlement network con forte survivorship premium
- La domanda che conta oggi e soprattutto domanda di riserva, collaterale e allocazione di bilancio, piu che domanda di consumo retail quotidiano.
- Questo non e un difetto cosmetico; e la forma reale del product-market fit di Bitcoin nel 2026.
- Il mercato tende spesso a raccontare Bitcoin come `payments network`. I numeri disponibili suggeriscono piu chiaramente `monetary network`.
- La crescita non e comprata con emissioni di token insider o incentive programs; e in gran parte domanda organica di mercato, istituzionale e macro.
- Il lato debole e che una parte materiale della domanda resta comunque regime-dependent:
  - macro liquidity
  - ETF / product flows
  - treasury allocation decisions
  - leva sul mercato derivati

Speculazioni:
- Se l adozione come `treasury reserve asset` o `macro collateral` accelera, la business quality puo migliorare ancora senza bisogno di fee market esplosivo.
- Se invece i flussi restano prevalentemente speculativi e il fee market non cresce mai in modo strutturale, Bitcoin puo restare un asset monetario forte ma con narrativa `payments / settlement` meno convincente del brand.

## 4. Unit economics e qualita dei ricavi
Fatti verificabili:
- La documentazione `developer.bitcoin.org` spiega che le transaction fees dipendono dalla byte size della transazione e dalla domanda di blockspace e che la fee e assegnata al miner.
- La pagina FAQ di Coinbase dice che il miner riceve block reward in nuovo `BTC` insieme alle transaction fees.
- `Mempool.space`, sul sample recente a 144 blocchi per Foundry USA, mostra:
  - total reward: `451.64 BTC`
  - average reward per block: `~3.1364 BTC`
  - average fee per block: `~0.0114 BTC`
  - fee share del reward totale del sample: `~0.36%`
- `CoinShares` nel mining report `Q1 2026` dice che le fees erano `consistently below 1%` del total block reward nel periodo analizzato e cita average fees per block `~0.018 BTC` in `Q4 2025`.
- Lo schedule attuale implica `164,250 BTC` di nuova issuance teorica annua, cioe `~0.82%` di inflazione sulla circulating odierna.

Flow of value waterfall
- `gross user fees`:
  - transaction fees pagate in `BTC` dagli utenti per ottenere blockspace
- `protocol revenue retained`:
  - `nessuna`
  - Bitcoin non trattiene fees in treasury, non brucia fees, non redistribuisce fees a holder passivi
- `miner revenue`:
  - block subsidy in nuovo `BTC`
  - transaction fees in `BTC`
- `tokenholder revenue`:
  - non esiste revenue share diretta per chi detiene passivamente `BTC`
  - l holder beneficia solo in forma indiretta se la domanda di `BTC` come bene monetario cresce
- `staking rewards budget`:
  - `non applicabile`

Buyback quality test
- buyback: `non applicabile`
- fonte: nessun programma di buyback nativo
- percentuale esatta: `0`
- base di calcolo: `nessuna`
- natura: `inesistente`
- destinazione finale di eventuali riacquisti: `non applicabile`
- effetto su supply: `non applicabile`

Stress test sulla monetizzazione diretta del token
- uso il fee sample recente di `~0.0114 BTC` per blocco come riferimento prudente:
  - annualizzazione fee minerarie implicite: `~599 BTC/anno`
  - al prezzo Coinbase snapshot, equivalgono a circa `~$44M/anno`
- contro un market cap di `~$1.49T`, anche trattando in modo errato queste fees come `holder revenue`, il rendimento implicito sarebbe circa `0.003%`
- ma questo esercizio e gia troppo favorevole all holder, perche quelle fees non vanno agli holder passivi: vanno ai miner

Inferenze ragionevoli:
- Il direct accrual per l holder passivo di `BTC` e `quasi nullo`.
- Bitcoin non va comprato come quasi-equity del fee market. Quel frame porta a concludere che l asset e absurdamente caro, ma e il frame sbagliato.
- Il vero economic engine del token e il `monetary premium`, non il pass-through dei ricavi.
- Esiste pero una tensione strutturale di lungo periodo:
  - oggi la security budget dipende ancora soprattutto dall issuance
  - nel lunghissimo periodo il sistema dovra contare molto di piu sulle fees o su un prezzo molto piu alto del `BTC`

Speculazioni:
- Se nuove forme di domanda di blockspace alzano le fees in modo strutturale, il profilo di sicurezza di lungo periodo migliora.
- Anche in quel caso, pero, il beneficio per gli holder resterebbe indiretto: migliore security narrative, non cash flow diretto.

## 5. Token: come cattura valore davvero
Fatti verificabili:
- `BTC` e necessario per:
  - pagare fees sul layer base
  - ricevere block reward come miner
  - fungere da unita economica nativa del network
- Il protocollo non prevede:
  - fee switch
  - burn
  - buyback
  - staking nativo PoS
  - governance token separato
  - treasury di protocollo
- `Bitcoin.org` e `Coinbase` insistono entrambi sui tratti di scarsita, decentralizzazione e assenza di emittente centrale.
- Il massimo teorico di supply resta `21,000,000 BTC`.

Inferenze ragionevoli:
- `BTC` cattura valore in modo `indiretto ma reale`:
  - se aumenta la domanda per possedere, collateralizzare o usare Bitcoin come reserve asset, il valore si riflette nel prezzo del token perche il token e l asset
- Questa cattura di valore non assomiglia a revenue share e non va scambiata per yield.
- In Bitcoin il legame business -> token e diverso da quasi tutto il resto del settore:
  - non passa da fee redistribution
  - non passa da governance rents
  - passa dalla domanda diretta per il bene monetario stesso
- Questo rende il token qualitativamente migliore di molti alt token, ma non lo rende automaticamente `cheap`.

Claim audit inline
- claim: `Bitcoin e gia deflattivo`
  - evidenza migliore: supply cap a `21M`, ma issuance residua annua ancora `~164,250 BTC`
  - cosa dimostra davvero: scarsita terminale e bassa inflazione, non deflazione attuale
  - giudizio: `parzialmente supportata`
- claim: `il token cattura revenue`
  - evidenza migliore: developer docs e Coinbase dicono che fees e subsidy vanno ai miner
  - cosa dimostra davvero: il token e necessario, ma non incassa revenue passiva
  - giudizio: `non dimostrata`

Speculazioni:
- Se Bitcoin consolida il ruolo di collateral globale e treasury reserve, il premium di scarsita puo espandersi anche senza forte crescita delle fees.
- Se invece il mercato smette di premiarlo come bene monetario superiore, il token resta tecnicamente valido ma la rerating story si indebolisce parecchio.

## 6. Supply, unlock e dilution analysis
Fatti verificabili:
- `Coinbase` snapshot `2026-04-14`:
  - circulating supply: `20,015,553 BTC`
  - total supply: `20,015,553 BTC`
  - max supply: `21,000,000 BTC`
  - FDV: `~$1.56T`
- La quota gia emessa e `~95.31%`.
- La nuova issuance teorica annuale post-halving e `164,250 BTC`, cioe circa `0.82%` della circulating attuale.
- Non esiste uno schedule di unlock tipo:
  - team vesting
  - VC cliff
  - foundation emissions
  - ecosystem grants onchain
- `Coinbase` segnala anche che il max supply non puo essere aumentato senza consensus change.

Float vs supply
- `total supply` e `circulating supply` coincidono quasi interamente nel senso protocol-level
- `liquid circulating supply` e piu bassa della circulating nominale perche una porzione di coin e:
  - dormiente
  - persa
  - in cold storage di lungo termine
  - intrappolata in wrapper / custody aggregation
- `exchange float` reale non e chiudibile con rigore sufficiente dai dati disponibili oggi

Inferenze ragionevoli:
- La qualita della supply di Bitcoin e una delle piu pulite dell intero settore.
- La scarsita non e narrativa di marketing:
  - il cap esiste davvero
  - la dilution residua e bassa
  - non esistono unlock opportunistici classici
- Questo non significa `supply netta in calo`: la supply netta e ancora in aumento, solo molto lentamente.
- La sell pressure strutturale non arriva da unlock. Arriva soprattutto da:
  - miner sales
  - treasury rebalancing
  - prese di profitto di holder storici

Sell pressure potenziale nei prossimi `3 / 6 / 12 mesi`
- `3 mesi`:
  - dominata da miner economics, ETF flows e corporate treasury decisions
- `6 mesi`:
  - dominata da regime macro, leva derivati e comportamento dei grandi veicoli intermediati
- `12 mesi`:
  - dominata da narrativa monetaria e da eventuale espansione del buyer base istituzionale

Speculazioni:
- Se la domanda marginale da prodotti quotati e treasury buyers resta superiore all issuance piu alle vendite dei miner, il prezzo puo restare supportato anche senza mania retail.
- Se gli acquirenti strutturali rallentano, l assenza di unlock non basta da sola a difendere il prezzo.

## 7. Treasury e capital allocation
Fatti verificabili:
- Bitcoin non ha una treasury di protocollo.
- Non esiste una foundation che riceva automaticamente fees o nuova supply per mandato di governance.
- Non esiste un buyback budget protocol-defined.

Inferenze ragionevoli:
- Questo elimina una grande fonte di agency risk comune negli alt token:
  - niente foundation che vende token per spese
  - niente grants treasury che puo tornare a mercato
  - niente emissioni discrezionali
- Il rovescio della medaglia e che Bitcoin non possiede neppure un capitale centralizzato da usare per:
  - marketing
  - grants
  - partnership
  - buyback difensivi
- La `capital allocation` che conta quindi sta fuori dal protocollo:
  - capex dei miner
  - politiche di treasury delle corporate holders
  - decisioni dei gestori di prodotti quotati

Rischi di secondo ordine
- concentrazione di soft power in:
  - core dev piu influenti
  - grandi pool minerari
  - grandi custodian / ETF wrapper
- ma questa non e la stessa cosa di una treasury centralizzata che puo dumpare supply nativa

## 7A. Token accrual e net supply verdict
- il token riceve valore economico: `indiretto`
- il driver principale del bull case e: `mix`, con prevalenza di `business growth come bene monetario + scarsita narrativa reale`
- i buyback sono materialmente rilevanti sul market cap attuale: `no`
- i buyback superano la pressione da unlock / emissioni: `no`
- i token riacquistati spariscono davvero: `no`
- la supply netta appare: `in aumento`, ma lentamente
- il legame business -> token e: `medio`
- mini verdict finale della sezione: `bullish per il token`, ma per motivi di scarsita e necessita monetaria, non per direct cash flow

## 8. Posizionamento competitivo
Competitor diretti
- `oro`:
  - vantaggio Bitcoin: trasferibilita digitale, custody programmabile, settlement 24/7, divisibilita estrema
  - vantaggio oro: volatilita piu bassa, track record storico millenario, minore rischio tecnologico
- `fiat e titoli di stato` come riserva liquida:
  - vantaggio Bitcoin: non-sovereign, supply finita, self-custody
  - svantaggio Bitcoin: nessun cash yield intrinseco, drawdown profondi, alta sensibilita al regime macro
- `Ethereum / altri crypto reserve assets`:
  - vantaggio Bitcoin: maggiore semplicita, minore governance surface, brand piu forte, supply story piu pulita
  - svantaggio Bitcoin: meno programmabilita, meno fee-generating utility, meno app-layer capture

Competitor indiretti
- stablecoins per pagamenti
- ETF e broker per esposizione finanziaria comoda
- real estate, commodities, macro hedges come contenitori di capital preservation

Competitor adiacenti
- other proof-of-work assets
- synthetic bitcoin exposure via public equities, miners, treasury companies

Inferenze ragionevoli:
- Il vantaggio competitivo piu forte di Bitcoin non e tecnico in senso puro; e `social liquidity + policy credibility + institutional acceptance`.
- Questo moat e reale e difficile da copiare, anche se il codice in astratto e copiabile.
- Il mercato pero gli riconosce gia un premio molto ampio:
  - non e un winner sottoradar
  - e gia trattato come il benchmark dell intero settore

Mini take competitivo
- vantaggi veri:
  - brand monetario
  - liquidita
  - supply credibility
  - regulatory legibility relativa
- vantaggi temporanei:
  - parte della dominance in fasi di risk-off crypto
- vantaggi di narrativa:
  - lettura semplicistica `digital gold inevitabile`
- vantaggi finti:
  - idea che fee market attuale da solo giustifichi il market cap

## 9. Moat, rischio copia e dipendenze esterne
Fatti verificabili:
- Il software e open source.
- Bitcoin opera senza owner centrale, ma l ecosistema dipende ancora da:
  - miner
  - ASIC manufacturers
  - energia
  - custodian
  - exchange
  - veicoli regolamentati
- `Mempool.space` mostra che una quota materiale dei blocchi resta concentrata in pochi pool.

Inferenze ragionevoli:
- Il prodotto e facilmente copiabile nel codice, ma molto difficile da copiare nel `moat sociale`.
- I veri moat sono:
  - profondita di capitale
  - liquidita
  - Lindy effect
  - accettazione come collateral
  - clarity narrativa come asset semplice
- Le dipendenze esterne contano eccome:
  - supply chain ASIC
  - energy economics
  - canali di custodia
  - gateway regolamentati
- Bitcoin e quindi robusto, ma non invulnerabile. Il suo moat e piu `coordination moat` che `software moat`.

## 10. Market structure del token
Fatti verificabili:
- `Coinbase` `2026-04-14`:
  - spot price: `$74,193.02`
  - market cap: `~$1.49T`
  - 24h volume: `~$51.28B`
- `Kraken API` stesso giorno:
  - last trade: `$74,727.50`
  - 24h high / low: `$74,966.20 / $70,691.60`
- `CoinGlass` snapshot `2026-04-14`:
  - futures volume 24h: `~$44.78B`
  - spot volume 24h: `~$3.02B`
  - open interest: `~$52.17B`
- `Mempool.space` mostra che top 2 pool sono `~46.93%` della block share osservata e il top 4 e `~67.43%` sul set selezionato.
- `Strategy` detiene `780,897 BTC`, cioe `~3.90%` della circulating osservata.

Inferenze ragionevoli:
- `BTC` e profondamente liquido e non ha la fragilita tipica di alt con float minuscolo.
- Non e pero immune da reflexivity:
  - il mercato derivati e gigantesco
  - open interest molto alto puo amplificare squeeze e liquidation cascades
- Il prezzo e sostenuto da domanda reale e istituzionale molto piu che da scarsita artificiale insider-made.
- Non c e classico `listing catalyst` o `delisting risk` come per gli alt, ma esiste un rischio diverso:
  - concentrazione crescente in wrapper e custodian
  - concentrazione di mining pools
  - concentrazione in pochi holder strategici

Limiti informativi
- non ho funding, basis, borrow e short availability cross-venue nello stesso timestamp
- non ho exchange float preciso
- non ho una mappa completa degli ETF beneficial owners

Giudizio strutturale della sezione
- liquidita spot reale: `alta`
- qualita delle venue: `alta`
- rischio dump da insider unlock: `basso`
- rischio reflexivity da derivati: `medio`
- fragilita da concentrazione infrastrutturale / custody: `media`

## 11. Holder base e allineamento
Fatti verificabili:
- `Coinbase` descrive Satoshi come possibile miner iniziale di `~1M BTC`, holdings mai mosse secondo la narrativa piu diffusa riportata dalla pagina.
- `Strategy` controlla `780,897 BTC` a `2026-04-12`.
- `CoinShares` registra `~$871M` di inflows settimanali su prodotti Bitcoin nella settimana chiusa al `2026-04-13`.
- Bitcoin non ha team allocation, foundation vesting o insider unlock schedule nativi comparabili agli alt token.

Inferenze ragionevoli:
- L holder base di Bitcoin e ampia ma barbell:
  - early holders e coin dormienti
  - ETF / custodian / allocatori istituzionali
  - corporate treasury
  - trader macro e crypto-native
- L allineamento strutturale e migliore della media crypto perche mancano i classici rent seekers da tokenomics.
- Cresce pero un altro tipo di concentrazione:
  - veicoli quotati
  - custodian
  - grandi corporate holders
- I maggiori holder sono piu spesso `strategici` o `dormienti` che `mercenari`, ma questo non elimina il rischio di concentrazione economica.

## CT-12. Recent event evidence log
- `2026-04-13`
  - fonte: `CoinShares Fund Flows`
  - stato: `confermato`
  - cosa e successo davvero: prodotti digital asset hanno registrato `~$1.1B` di inflows settimanali; Bitcoin ha assorbito `~$871M`, cioe circa il `79%` del totale
  - cosa e solo narrativa: che questo implichi da solo una nuova gamba strutturale di bull market
  - market reaction osservata: `Coinbase` mostra `BTC` `+8.17%` su 7 giorni e volume 24h `~$51.28B`
  - impatto: `market structure / fiducia`
  - stato dell impatto: `aperto ma non thesis-changing da solo`
- `2026-04-13`
  - fonte: `Strategy 8-K`
  - stato: `confermato`
  - cosa e successo davvero: Strategy ha acquistato `13,927 BTC` per `~$1.00B` e ha portato le holdings a `780,897 BTC`
  - cosa e solo narrativa: che ogni acquisto corporate implichi scarsita terminale immediata
  - market reaction osservata: coerente con narrativa di domanda treasury; non ho causalita isolabile tick-by-tick
  - impatto: `market structure / narrativa / fiducia`
  - stato dell impatto: `aperto`
- `2026-03-25`
  - fonte: `CoinShares Bitcoin Mining Report Q1 2026`
  - stato: `confermato`
  - cosa e successo davvero: report descrive hashprice `~$29-30/PH/day`, average cash cost `~$79,995/BTC` in `Q4 2025` per i miner pubblici e fee income sotto l `1%` del reward totale nel periodo
  - cosa e solo narrativa: che questo significhi rottura imminente della sicurezza del network
  - market reaction osservata: pressione sul mining sector piu che structural break su `BTC`
  - impatto: `business / security budget / narrativa`
  - stato dell impatto: `aperto ma gestibile`
- `2026-01-05` e `2026-01-10`
  - fonte: `Bitcoin Core`
  - stato: `confermato e chiuso`
  - cosa e successo davvero: Bitcoin Core ha pubblicato un avviso su un `wallet migration bug` in `30.0` e `30.1`, poi `30.2` e stata rilasciata il `2026-01-10`
  - cosa e solo narrativa: che si sia trattato di rottura del consenso Bitcoin
  - market reaction osservata: nessun evidence log serio di thesis break sul token; evento piu di software maintenance e trust optics
  - impatto: `fiducia / software operational risk`
  - stato dell impatto: `chiuso`

## CT-13. Narrative break e trust shock test
- `wallet migration bug` di gennaio:
  - classificazione: `problema di optics o comunicazione`
  - motivo: serio per chi usa quelle versioni wallet, ma non e stato un consensus failure
- concentrazione dei mining pools:
  - classificazione: `rischio reale di centralizzazione`
  - motivo: top 2 pool quasi al `47%` e top 4 oltre il `67%` sul sample selezionato meritano attenzione strutturale
- concentrazione in wrapper / ETF / treasury companies:
  - classificazione: `rischio reale di controparte / partner concentration`
  - motivo: non rompe Bitcoin, ma allontana parte della detenzione dalla purezza `self-custody` della narrativa
- verdict del test:
  - nessun `thesis-changing structural break` recente trovato
  - esistono pero vulnerabilita croniche su concentrazione mineraria e intermediated ownership che non vanno trattate come rumore

## 12. Thesis-change synthesis
Sviluppi che cambiano davvero la lettura
- `2026-04-13` `CoinShares fund flows`:
  - confermato: forte rimbalzo di flussi nei prodotti digital asset con Bitcoin al centro
  - market reaction osservata: prezzo e volume in recupero settimanale
  - cosa cambia: rafforza la lettura di Bitcoin come destinatario principale del capitale istituzionale quando il mercato torna costruttivo
  - quanto sembra gia prezzato: `parzialmente`
  - orizzonte residuo: `settimane`
- `2026-04-13` `Strategy 8-K`:
  - confermato: ulteriore corporate accumulation su scala materiale
  - cosa cambia: aumenta la tesi di `treasuryization` del supply base, ma aumenta anche la concentrazione
  - quanto sembra gia prezzato: `parzialmente`
  - orizzonte residuo: `trimestri`
- `2026-03-25` `CoinShares mining report`:
  - confermato: fee market ancora troppo piccolo per sostituire davvero il subsidy oggi
  - cosa cambia: ricorda che il bull case di Bitcoin non puo poggiare sul fee cash flow; deve poggiare sul monetary premium
  - quanto sembra gia prezzato: `molto`
  - orizzonte residuo: `trimestri`

Mini verdict
- evento materiale ma transitorio
- impatto principale: `market structure`
- stato: `in evoluzione`
- grado di pricing percepito: `parzialmente`
- orizzonte dominante: `settimane / trimestri`

## 13. Catalizzatori
Gia noti
- prosecuzione degli inflows nei prodotti spot / ETP
  - impatto potenziale: `alto`
  - probabilita: `media`
  - timing: `settimane`
  - pricing: `parzialmente prezzato`
- ulteriori acquisti da corporate treasury gia attive
  - impatto potenziale: `medio`
  - probabilita: `media`
  - timing: `settimane / trimestri`
  - pricing: `parzialmente prezzato`

Probabili
- regime macro piu accomodante e calo del costo opportunita del non-yielding collateral
  - impatto potenziale: `alto`
  - probabilita: `media`
  - timing: `trimestri`
  - pricing: `non pienamente prezzato`
- prosecuzione della dominance rotation verso `BTC` nei periodi di market stress o selective risk-on
  - impatto potenziale: `medio`
  - probabilita: `media-alta`
  - timing: `settimane`
  - pricing: `parzialmente prezzato`

Opzionali
- miglioramento materiale del fee market onchain
  - impatto potenziale: `medio`
  - probabilita: `bassa-media`
  - timing: `trimestri`
  - pricing: `poco prezzato`
- ampliamento della base di collateral acceptance tradizionale
  - impatto potenziale: `alto`
  - probabilita: `bassa-media`
  - timing: `trimestri`
  - pricing: `poco prezzato`

Puramente speculativi
- adozione sovrana o quasi-sovrana piu aggressiva del previsto
  - impatto potenziale: `molto alto`
  - probabilita: `bassa`
  - timing: `trimestri`
  - pricing: `non prezzato`

## 14. Bull case
Bull case realistico
- Bitcoin resta il principale destinatario del capitale istituzionale crypto
- l issuance residua bassa continua a essere assorbita da ETF, treasury companies e long-term allocators
- il prezzo puo tornare nell area `~$100k`, cioe market cap `~$2.00T`
- gran parte del rialzo verrebbe da espansione del monetary premium, non da crescita delle fees

Bull case forte
- la domanda treasury si amplia oltre i nomi gia noti
- il regime macro diventa piu favorevole agli asset scarsi non sovrani
- ritorno all ATH `~$126.2k` diventa plausibile, cioe market cap `~$2.53T`
- il rerating sarebbe trainato soprattutto da narrativa monetaria convalidata dai flussi

Bull case estremo
- Bitcoin viene trattato sempre piu come reserve asset globale piu che come semplice crypto beta
- nuove ondate di corporate / sovereign accumulation riducono il float percepito
- uno scenario `~$150k` implica market cap `~$3.00T`
- qui il grosso del rialzo verrebbe da multiple expansion del premium monetario, non da unit economics

## 15. Bear case
- il fee market resta cronicamente piccolo e rafforza la critica che il security budget dipenda troppo a lungo dall issuance
- il mercato smette di pagare il `monetary premium` e torna a trattare Bitcoin come puro macro beta ad alta volatilita
- ETF / ETP flows si girano, corporate treasury buyers rallentano e i miner restano sotto pressione
- la concentrazione in pochi pool, custodian e wrapper peggiora la qualita della decentralizzazione percepita
- stablecoins e canali centralizzati continuano a vincere quasi tutto il caso d uso pagamenti
- il prodotto puo continuare a esistere e a funzionare, ma il token puo comunque scendere molto se il premium di scarsita si comprime

## 16. Valuation thinking
Fatti verificabili:
- market cap attuale anchor `Coinbase`: `~$1.49T`
- FDV anchor `Coinbase`: `~$1.56T`
- ATH `Coinbase`: `$126,210.50`, che implicherebbe market cap `~$2.53T` sulla circulating attuale
- fee flow recente osservabile via mempool sample implica ordini di grandezza minuscoli rispetto al market cap

Perche il frame equity-style fallisce
- `price-to-fees` o `price-to-holder-revenue` su Bitcoin portano a numeri assurdi non perche il mercato sia sicuramente folle, ma perche l asset non e equity e gli holder non incassano fees
- il mercato paga:
  - survivability
  - liquidita
  - policy credibility
  - reserve optionality
  - collateral status

Lettura disciplinata del prezzo
- Se leggo Bitcoin come `payment rail monetizzata dalle fees`, appare estremamente caro.
- Se lo leggo come `digital reserve asset` con il moat monetario piu forte del settore, il prezzo attuale appare molto piu ragionevole.
- Il mercato sta gia pagando una quota larga del winner premium:
  - Bitcoin ha il market cap piu alto del settore di gran lunga
  - ha dominance elevata
  - assorbe la quota principale dei flussi istituzionali quando il rischio torna
- Quello che non sembra ancora completamente prezzato e uno scenario di vera `seconda gamba` del reserve adoption curve.

Inferenze ragionevoli:
- `BTC` non e cheap su base `cash flow`.
- `BTC` puo ancora essere ragionevolmente prezzato su base `monetary premium`.
- Il prezzo attuale sembra incorporare:
  - business / asset quality alta
  - supply quality molto alta
  - prosecuzione di adozione istituzionale ragionevole
- Non sembra invece incorporare pienamente un esito molto piu aggressivo tipo `global reserve breakout`.

## 17. Price map e scenario map
Scenario `bear / macro derating`
- prezzo: `~$45k`
- market cap: `~$0.90T`
- FDV: `~$0.95T`
- assunzioni implicite:
  - risk-off macro
  - outflows o rallentamento deciso dei buyer strutturali
  - nessuna thesis break tecnica, ma compressione del premium monetario
- probabilita qualitativa: `bassa-media`

Scenario `base case lower bound`
- prezzo: `~$60k`
- market cap: `~$1.20T`
- FDV: `~$1.26T`
- assunzioni implicite:
  - Bitcoin resta asset dominante ma i flussi non accelerano
  - fee market resta piccolo
  - il mercato tratta `BTC` come quality asset ma senza rerating
- probabilita qualitativa: `media`

Scenario `base case mid`
- prezzo: `~$75k`
- market cap: `~$1.50T`
- FDV: `~$1.58T`
- assunzioni implicite:
  - continuazione della tesi centrale attuale
  - adozione istituzionale presente ma non esplosiva
  - nessun structural break su security / regolazione / custody
- probabilita qualitativa: `alta`

Scenario `base case upper bound`
- prezzo: `~$85k`
- market cap: `~$1.70T`
- FDV: `~$1.79T`
- assunzioni implicite:
  - flussi strutturali ancora buoni
  - market setup positivo ma non euforico
  - il premium monetario si espande moderatamente
- probabilita qualitativa: `media`

Scenario `rerating forte ma non estremo`
- prezzo: `~$100k`
- market cap: `~$2.00T`
- FDV: `~$2.10T`
- assunzioni implicite:
  - maggiore corporate / ETF absorption
  - BTC trattato piu apertamente come reserve collateral istituzionale
- probabilita qualitativa: `media-bassa`

Scenario `ritorno all ATH`
- prezzo: `$126,210.50`
- market cap: `~$2.53T`
- FDV: `~$2.65T`
- assunzioni implicite:
  - nuova fase di rerating pieno del monetary premium
  - domanda marginale molto forte
- probabilita qualitativa: `bassa-media`

Scenario `narrative overshoot`
- prezzo: `~$150k`
- market cap: `~$3.00T`
- FDV: `~$3.15T`
- assunzioni implicite:
  - il mercato prezza una parte materiale del bull case estremo
  - la narrativa corre piu veloce del fee market o dell uso onchain
- probabilita qualitativa: `bassa`

Price placement
- `spot anchor` usato per il placement:
  - principale: `Coinbase`, crawl `2026-04-14`, `$74,193.02`
  - cross-check: `Kraken REST API`, open `2026-04-14`, last trade `$74,727.50`
- prezzo attuale / market cap attuale:
  - prezzo: `~$74.2k`
  - market cap: `~$1.49T`
- corridoio `base case` ragionevole:
  - lower bound: `~$60k`
  - mid: `~$75k`
  - upper bound: `~$85k`
- dove cade il prezzo attuale rispetto a quel corridoio:
  - `circa al centro`
- se il prezzo sta gia prezzando:
  - `solo il base case`

## 17A. Verdict calibration bridge
- base case centrale usato davvero:
  - Bitcoin resta il principale bene monetario crypto, continua ad assorbire flussi istituzionali ragionevoli, ma non ottiene ancora una vera accelerazione da adozione sovrana o fee market trasformativo
- corridoio coerente con quel base case:
  - `~$60k - $85k`, con centro `~$75k`
- distanza del prezzo attuale dal corridoio:
  - non materialmente distante
- stato della tesi al prezzo corrente:
  - `intatta`, ma non abbastanza poco prezzata da giustificare un verdetto di sottovalutazione strutturale

Classificazione obbligatoria del verdetto
- verdict: `fairly priced`

## 18. Mispricing test
- cosa sta sottovalutando il mercato?
  - quanto la supply quality di Bitcoin sia ancora nettamente superiore alla quasi totalita del settore crypto
- cosa sta sopravvalutando il mercato?
  - quando cade nel framing `fees = fondamentali` oppure, all opposto, quando assume che la sola narrativa di scarsita garantisca rerating infinito
- qual e la variabile piu importante che quasi tutti stanno ignorando?
  - che il nodo decisivo non e il fee yield odierno ma la persistenza del `monetary premium`
- dove sta il vero edge dell analisi?
  - separare con disciplina `asset monetario` da `protocol equity`
- cosa sto rischiando di capire male io come analista?
  - di essere troppo severo se la curva di adozione da reserve asset accelera piu rapidamente del previsto
- qual e il vantaggio concreto che regge la tesi anche fuori dalla narrativa crypto, se esiste?
  - un bene digitale scarso, auto-custodibile e non emesso da nessuno, trasferibile globalmente senza permesso

## 18A. Strongest countercase
- La lettura piu forte contro un verdict `fairly priced` e che il corridoio base e troppo conservativo: se il mercato sta davvero entrando in una fase di `treasury adoption`, `BTC` potrebbe meritare un base corridor piu vicino a `~$80k-110k`.
- La mia assunzione piu discutibile e trattare il reserve premium come crescita lenta e lineare.
- Il singolo sviluppo che nei prossimi `90d` farebbe apparire questa analisi troppo prudente sarebbe una prosecuzione di inflows su scala `~$1B+` settimanale accompagnata da nuovi acquirenti corporate o quasi-sovrani materialmente rilevanti.

## 18B. Claim audit residuale
- claim:
  - `Le fees oggi non sostituiscono materialmente il subsidy`
  - evidenza migliore disponibile: `Mempool.space` sample recente con fee share `~0.36%` e `CoinShares` Q1 2026 con fees sotto l `1%` del total block reward
  - cosa dimostra davvero: il security budget attuale dipende ancora soprattutto dalla nuova issuance
  - giudizio: `supportata`
  - implicazione: abbassa la solidita del frame `Bitcoin come fee machine`, non necessariamente quella del frame `Bitcoin come bene monetario`
- claim:
  - `Il token accrual di BTC e indiretto, non cash-flow`
  - evidenza migliore disponibile: developer docs e Coinbase dicono che fees e block reward vanno ai miner; non esistono burn, buyback o revenue share
  - cosa dimostra davvero: l holder passivo non incassa ricavi nativi del protocollo
  - giudizio: `supportata`
  - implicazione: il verdetto di prezzo va costruito su premium monetario e supply quality, non su `P/E` travestiti
- claim:
  - `La supply quality di Bitcoin resta eccezionale`
  - evidenza migliore disponibile: circulating `20,015,553`, max `21,000,000`, nessun unlock insider, nessuna treasury protocol-level
  - cosa dimostra davvero: scarsita reale e agency risk tokenomics molto bassa
  - giudizio: `supportata`
  - implicazione: sostiene la tesi che `BTC` meriti un premio strutturale rispetto al resto del settore

## 19. Residual source divergences
- metrica o dato:
  - `spot price`
  - fonti in conflitto: `Coinbase $74,193.02`, `Kraken API $74,727.50`, `CoinGlass` dashboard `~$71.65k`
  - differenza di definizione o perimetro: venue spot live vs dashboard aggregata / crawl lag
  - possibile motivo della divergenza: timestamp diversi e ritardo delle dashboard
  - implicazione analitica: per il verdict uso `Coinbase` come anchor principale e `Kraken API` come cross-check; non uso `CoinGlass` come verita spot finale
- metrica o dato:
  - `circulating supply`
  - fonti in conflitto: `Coinbase 20,015,553 BTC` vs `CoinGlass ~19.86M BTC`
  - differenza di definizione o perimetro: arrotondamenti / lag / metodologia dashboard
  - possibile motivo della divergenza: crawl timing e differente politica di rounding
  - implicazione analitica: la differenza non cambia il verdict, ma conferma che per i major il prezzo finale va ancorato a fonti piu primarie e riconciliate

## 20. Checklist finale di investimento
- 3 motivi forti per essere bullish
  - supply estremamente pulita, con hard cap reale e assenza di unlock / treasury overhang
  - moat di liquidita, brand e collateral acceptance ancora dominante
  - domanda istituzionale e treasury demand restano le piu credibili del settore
- 3 motivi forti per essere cauti
  - il direct accrual per holder passivi e quasi nullo
  - il fee market resta troppo piccolo per raccontare Bitcoin come cash-flow asset
  - concentrazione in pool, custodian e grandi holder cresce e puo pesare sulla narrativa di decentralizzazione
- 3 segnali che confermerebbero la tesi
  - prosecuzione degli inflows nei prodotti Bitcoin
  - ulteriori acquisti corporate / institutional materialmente rilevanti
  - tenuta o crescita del premium monetario senza dipendere da euforia generalizzata sugli alt
- 3 segnali che invaliderebbero la tesi
  - outflows persistenti e forti dai canali intermediati con derating del premium monetario
  - peggioramento serio della concentrazione o incidente che colpisca la fiducia nella decentralizzazione operativa
  - deterioramento del buyer base strutturale tale da lasciare i miner come seller dominanti senza nuovi assorbitori
- 3 metriche da monitorare nei prossimi 90 giorni
  - flussi settimanali su prodotti Bitcoin
  - quota fees / reward totale e condizioni del fee market
  - open interest derivati e segni di leva eccessiva rispetto alla domanda spot

## 21. Conclusione netta
- research mode: `full diligence`
- business quality: `alta`
- necessita di esistenza del prodotto: `alta`
- necessita del token per il prodotto: `alta`
- token quality: `alta`
- token accrual verdict: `medio`
- market setup: `neutro`
- regime eventi recente: `evento materiale ma transitorio`
- verdict: `fairly priced`
- divergenze residue di fonti: `basse`
- confidenza del giudizio: `media`
- orizzonte temporale implicito: `medio-lungo`
- motivo principale del giudizio:
  - Bitcoin merita un premio strutturale per qualita della supply, clarity monetaria e domanda istituzionale, ma quel premio e gia in gran parte riflesso in un market cap `~$1.49T`.
  - Il token e forte come bene monetario, non come fee-generating asset; per questo il bull case serio resta `monetary premium expansion`, non `holder cash flow`.
  - Sullo snapshot `2026-04-14`, il prezzo sembra prezzare bene il base case e non lascia un margine abbastanza ampio per chiamarlo `sottovalutato`.
