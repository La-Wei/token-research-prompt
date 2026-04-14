# Token Research: `Bitcoin / BTC`

## Input usato
- `[NOME/TICKER]`: `Bitcoin / BTC`
- Data snapshot principale: `2026-04-14`
- Obiettivo del test: eseguire `prompt/token-research-prompt.md` distinguendo con rigore tra necessita reale del protocollo Bitcoin, qualita del token `BTC`, market structure e pricing

## Materiale minimo per l analisi

### Fonti principali
- Fonti ufficiali protocollo:
  - https://bitcoin.org/en/how-it-works
  - https://bitcoin.org/en/bitcoin-core/features/validation
  - https://developer.bitcoin.org/devguide/transactions.html
  - https://developer.bitcoin.org/devguide/block_chain.html
- Fonti di market e onchain data:
  - https://www.coinglass.com/currencies/BTC
  - https://www.coingecko.com/en/coins/bitcoin
  - https://mempool.space/
  - https://ycharts.com/indicators/bitcoin_transactions_per_day
  - https://ycharts.com/indicators/bitcoin_network_hash_rate
  - https://ycharts.com/indicators/bitcoin_miners_revenue_per_day
  - https://ycharts.com/indicators/bitcoin_total_transaction_fees_per_day
  - https://ycharts.com/indicators/bitcoin_average_transaction_fee
- Fonti su holder base, tesorerie e regime regolatorio:
  - https://www.coingecko.com/en/treasuries
  - https://www.strategy.com/press/strategy-acquires-13627-btc-and-now-holds-687410-btc_01-12-2026
  - https://www.strategy.com/press/strategy-acquires-4871-btc-and-now-holds-766970-btc_04-06-2026
  - https://www.strategy.com/press/strategy-acquires-13927-btc-now-holds-780897-btc_04-13-2026
  - https://www.strategy.com/purchases
  - https://www.sec.gov/newsroom/press-releases/2026-26-sec-cftc-announce-historic-memorandum-understanding-between-agencies
  - https://www.sec.gov/newsroom/press-releases/2026-30-sec-clarifies-application-federal-securities-laws-crypto-assets
  - https://www.whitehouse.gov/presidential-actions/2025/03/establishment-of-the-strategic-bitcoin-reserve-and-united-states-digital-asset-stockpile/

### Snapshot numerico essenziale
- `CoinGlass` snapshot `2026-04-10`:
  - prezzo spot: `~$72,373`
  - market cap: `~$1.44T`
  - futures volume 24h: `~$64.43B`
  - spot volume 24h: `~$5.14B`
  - open interest: `~$53.52B`
  - circulating supply: `20.01M BTC`
  - total supply: `20.01M BTC`
  - max supply: `21.00M BTC`
- `CoinGecko` page snippet consultata `2026-04-14`:
  - 24h range: `~$70,617 - $71,524`
  - 7d range: `~$67,947 - $73,538`
  - all-time high mostrato: `~$126,080` il `2025-10-06`
  - distanza dall ATH: `~43.8%`
- `YCharts / Blockchain.com` ultimi punti giornalieri accessibili:
  - transactions per day: `465,261` il `2026-04-06`
  - network hash rate: `884.23M TH/s` il `2026-04-06`
  - miners revenue per day: `~$34.09M` il `2026-04-09`
  - total transaction fees per day: `2.799 BTC` / `~$197,568` il `2026-03-11`
  - average transaction fee: `~$0.4916` il `2026-03-11`
- `mempool.space` snapshot vicino alla data report:
  - fee rate alto: `~1 sat/vB`
  - unconfirmed transactions: `~21,847`
  - average block time: `~10.6 minuti`
  - stima prossimo difficulty adjustment: `~-5.78%`
- `Strategy` fonti ufficiali:
  - holdings `2026-01-12`: `687,410 BTC`
  - holdings `2026-04-06`: `766,970 BTC`
  - holdings `2026-04-13`: `780,897 BTC`
  - incremento `2026-01-12 -> 2026-04-13`: `+93,487 BTC`

### Punti che restano opachi
- non ho una misura primaria unica del `liquid float` reale dopo ETF, custodian, treasury aziendali, coin dormienti e coin probabilmente perse
- non ho una beneficial ownership map pulita dietro i grandi indirizzi o dietro tutti i veicoli custodial
- non ho una misura unificata e same-timestamp di exchange reserves, ETF holdings e coin illiquide
- la valutazione di lungo periodo del security budget post-halving resta inferenziale: i dati correnti chiudono bene il presente, non dimostrano da soli la sostenibilita fee-only futura

---

# Output del prompt

## 0. Research mode e perimetro evidenze
- qualita delle fonti: `alta`
- copertura dati: `parziale`
- modalita: `full diligence`
- motivo della scelta:
  - la necessita di esistenza del protocollo, la meccanica monetaria, la cap a `21M` e la logica fee -> miner sono documentate da fonti ufficiali Bitcoin
  - supply, diluzione, assenza di treasury/opportunistic unlock e market structure macro sono osservabili con sufficiente rigore
  - holder base e float beneficiano di fonti buone ma non perfette, perche ETF, custodian e coin perse rendono la proprieta economica meno leggibile dell ownership onchain grezza
- copertura market structure: `robusta`
- blocchi osservabili con rigore sufficiente:
  - necessita di esistenza del prodotto
  - necessita del token
  - supply, cap monetaria e assenza di unlock discrezionali
  - qualita della liquidita spot e derivati
  - holder concentration per tesorerie pubbliche piu visibili
  - recenti sviluppi regolatori e di treasury demand
- blocchi ancora non chiudibili:
  - float veramente liquido
  - quota precisa di coin perse o economicamente non mobili
  - beneficial ownership dietro i grandi custodian
  - sostenibilita fee-only del security budget in un futuro molto piu lontano
- implicazione principale dei buchi dati:
  - il verdetto puo essere serio su business, token e pricing relativo, ma non deve fingere precisione sulla vera scarsita del float o su un valore intrinseco cash-flow based che Bitcoin non ha
- rischio principale di errore analitico:
  - trattare `BTC` troppo come un asset a fee capture e troppo poco come un bene monetario/riserva
- cap di confidenza:
  - `non oltre media`, perche Bitcoin resta un asset monetario il cui fair value dipende piu da adozione e premium che da cash flow dimostrabili
- confidenza preliminare: `media`

## 1. TL;DR iniziale
- Bitcoin risolve un bisogno reale: detenere e trasferire un asset digitale scarso, neutrale e non confiscabile con regole monetarie credibilmente dure.
- Il prodotto esiste davvero, ma non e il miglior sistema per pagamenti retail veloci o per UX; il suo vantaggio sta in riserva di valore, settlement e autocustodia.
- `BTC` e necessario al prodotto in modo totale: non e un token appeso sopra il protocollo; e il bene monetario del protocollo.
- La supply story e la piu pulita del settore: `21M` cap, `~95.3%` gia minati, nessun VC unlock, nessuna foundation treasury che puo diluire gli holder.
- Il problema e che non esiste revenue share holder-level: fees e subsidy vanno ai miner, quindi il bull case non e cash-flow, ma `monetary premium + balance-sheet demand + scarsita credibile`.
- Il mercato puo ancora sottoprezzare la pulizia della supply e l assorbimento da tesorerie/istituzioni, ma a `~$1.4T+` di market cap non sta ignorando Bitcoin.
- Giudizio preliminare: asset di qualita altissima e token di qualita altissima relativa, ma sullo snapshot attuale appare piu `fairly priced` che chiaramente cheap.

## 2. Che cosa fa davvero il protocollo
Fatti verificabili:
- `bitcoin.org` descrive Bitcoin come sistema che usa tecnologia peer-to-peer per operare senza banca centrale o intermediario centrale.
- `bitcoin.org` e la documentazione `Bitcoin Core Validation` chiariscono che i full node verificano blocchi e transazioni e proteggono le regole di consenso, incluso il limite finale di supply.
- `developer.bitcoin.org` spiega che le transaction fees vengono pagate ai miner e che il block reward combina subsidy e fees.
- L ordine esecutivo della Casa Bianca del `2025-03-06` definisce Bitcoin come asset con supply permanentemente capata a `21M` e lo collega esplicitamente alla narrativa `digital gold`.

Inferenze ragionevoli:
- Il problema reale che Bitcoin risolve non e `fare TPS migliori di Visa`. E offrire un bene digitale scarso, portabile e difficile da censurare o svalutare arbitrariamente.
- L utente finale che trae il massimo vantaggio da Bitcoin oggi non e necessariamente il consumatore retail che vuole pagare il caffe. E:
  - chi vuole savings asset non sovrano
  - chi vuole settlement neutrale
  - chi vuole self-custody
  - chi vuole collateral globale non emesso da una controparte aziendale
- Contro soluzioni centralizzate, Bitcoin perde su UX, velocita percepita, chargebacks e assistenza. Vince su neutralita, scarsita credibile, trasferibilita globale e assenza di controparte.
- Contro open source non tokenizzato o ledger permissioned, Bitcoin vince quando il punto e la neutralita monetaria condivisa tra parti che non si fidano l una dell altra. Se il problema e solo registrare dati in un consorzio, un database o un ledger permissioned resta piu efficiente.
- Se togli `BTC`, il prodotto non resta quasi identico: salta l unita monetaria, la fee market, il security budget e la logica stessa di scarsita del sistema.

Confronto esplicito con alternative realistiche
- soluzione centralizzata / API tradizionale:
  - banche commerciali, wire internazionali, PayPal, Revolut, stablecoin custodial e infrastrutture fintech
  - vantaggio Bitcoin: possesso nativo, final settlement neutrale, resistenza alla censura, nessun emittente
  - svantaggio Bitcoin: UX, compliance, recupero errori, velocita percepita e integrazione fiat restano spesso migliori lato centralizzato
- open source non tokenizzato:
  - database replicati, ledger permissioned, sistemi di settlement privati
  - vantaggio Bitcoin: bene monetario condiviso e non emesso da nessuno, verificabile globalmente
  - svantaggio Bitcoin: costi energetici e throughput basso rispetto a sistemi chiusi
- soluzione locale / self-hosted / offchain:
  - utile per registrare contabilita interna o coordinare un gruppo ristretto
  - ma non sostituisce un asset monetario neutrale che puo essere detenuto e verificato globalmente senza chiedere permesso

Vantaggio di prodotto vs vantaggio di coordinamento
- vantaggio di prodotto:
  - autocustodia
  - final settlement non dipendente da una singola impresa
  - politica monetaria semplice e credibilmente rigida
- vantaggio di coordinamento / capitale:
  - brand storico
  - liquidita globale
  - profondita derivati
  - status di asset benchmark del settore crypto

Mini verdict atomico
- necessita di esistenza del prodotto: `alta`
- vantaggio vs soluzione centralizzata/API: `medio`
- vantaggio vs open source non tokenizzato o locale: `forte`
- necessita del token per il prodotto: `alta`
- il progetto e soprattutto: `prodotto superiore + coordination layer monetario`

## 3. Business quality: qualita reale del protocollo
Fatti verificabili:
- `YCharts / Blockchain.com` mostra:
  - `465,261` transazioni/giorno il `2026-04-06`, `+66.5%` YoY
  - `884.23M TH/s` di hash rate medio il `2026-04-06`, `+0.96%` YoY
  - `~$34.09M` di miners revenue/giorno il `2026-04-09`, `+3.3%` YoY
  - `~$197,568` di total transaction fees/giorno il `2026-03-11`, `-59.8%` YoY
  - `~$0.4916` di average transaction fee il `2026-03-11`, `-62.3%` YoY
- `mempool.space` vicino alla data del report mostra mempool non congestionata:
  - fee alta `~1 sat/vB`
  - `~21.8k` transazioni non confermate
  - block time medio `~10.6 minuti`

Metric perimeter reconciliation
- `transactions per day` misura attivita onchain confermata, non valore economico trasferito.
- `hash rate` misura security spend/competition dei miner, non domanda finale degli utenti.
- `miners revenue` misura il budget economico pagato ai miner, ma include soprattutto nuova emissione e non equivale a `protocol revenue retained`.
- `transaction fees per day` misura cosa gli utenti pagano per spazio di blocco; non misura il valore monetario complessivo di Bitcoin come bene di riserva.

Inferenze ragionevoli:
- La business quality di Bitcoin resta `alta`, ma per motivi diversi dai protocolli app-driven:
  - potenza del brand monetario
  - robustezza della security layer
  - profondita di liquidita e collateral use
  - accettazione istituzionale crescente
- La crescita recente sembra piu coerente con `monetary network adoption` che con `fee explosion`:
  - piu transazioni rispetto a un anno fa
  - hash rate vicino ai massimi strutturali
  - fee medie e fees totali oggi non in regime euforico
- Quindi il business non appare cosmetico, ma neppure nel suo stato migliore come monetizzatore di block space.

Speculazioni:
- Se Bitcoin continua a rafforzarsi come bene di treasury, collateral e riserva sovrana, la business quality puo migliorare senza che le fees onchain esplodano.
- Se invece il mercato pretende che la tesi si giustifichi con fees e revenue-like metrics, Bitcoin sembrera sempre troppo caro rispetto a cio che in realta sta monetizzando: fiducia monetaria, non cash flow.

## 4. Unit economics e qualita dei ricavi
Fatti verificabili:
- `developer.bitcoin.org` chiarisce che le transaction fees sono date ai miner.
- `developer.bitcoin.org` chiarisce che `transaction fees + block subsidy = block reward`.
- `YCharts / Blockchain.com` indica:
  - `~$34.09M` di miners revenue/giorno il `2026-04-09`
  - `~$197,568` di total transaction fees/giorno il `2026-03-11`
- Con subsidy corrente di `3.125 BTC` per blocco e circa `144` blocchi/giorno, la nuova issuance run-rate e circa `450 BTC/giorno`.

Flow of value waterfall
- `gross user fees`:
  - fees pagate dagli utenti per entrare nei blocchi
  - ultimo punto accessibile: `2.799 BTC` / `~$197,568` al giorno il `2026-03-11`
- `protocol revenue retained`:
  - `nessuna`
  - Bitcoin non ha treasury di protocollo che trattenga parte delle fees per gli holder
- `miner revenue`:
  - block subsidy
  - transaction fees
  - ultimo punto accessibile: `~$34.09M` al giorno il `2026-04-09`
- `tokenholder revenue`:
  - `nessuna` per il passive holder di `BTC`
  - l holder beneficia solo se cresce la domanda per l asset o se si comprime l offerta disponibile
- `buyback budget / burn budget / staking rewards budget`:
  - `non applicabile`

Stress test sulla monetizzazione economica
- Se annualizzo le fees osservate il `2026-03-11`, ottengo circa `~$72.1M` annui.
- Contro market cap `~$1.44T - $1.49T`, questo implica un multiplo `market cap / annualized user fees` di circa `20,000x`.
- Anche il `miners revenue` annualizzato (`~$12.44B`) non e un anchor corretto per gli holder:
  - va ai miner, non agli holder passivi
  - include soprattutto emissione e non ricavi trattenuti dal protocollo
- Le fees del `2026-03-11` sono solo `~0.58%` del miners revenue del `2026-04-09` su base giornaliera comparabile: il security budget attuale resta principalmente subsidy-led.

Buyback quality test
- buyback: `non applicabile`
- fonte: nessun buyback nativo
- percentuale esatta: `0`
- base di calcolo: `nessuna`
- natura: `inesistente`
- destinazione finale dei token ricomprati: `non applicabile`
- effetto su supply: `non applicabile`

Inferenze ragionevoli:
- Bitcoin non monetizza come quasi-equity e non va letto cosi.
- La qualita del business non sta nella quota di fees che arriva all holder; sta nella credibilita del bene monetario e nella sua capacita di attrarre capitale di bilancio.
- Il vero nodo economico di lungo termine non e `mancano buyback`. E:
  - il fee market restera abbastanza forte negli anni per sostenere la security quando la subsidy scendera ancora?

## 5. Token: come cattura valore davvero
Fatti verificabili:
- `BTC` e l asset nativo del protocollo.
- La supply totale e hard-capped a `21M` secondo le fonti ufficiali e la documentazione di validazione di Bitcoin Core.
- Le fees sono pagate in `BTC` e i miner sono remunerati in `BTC`.
- Non esistono staking, governance yield, revenue share, fee switch o burn permanenti a beneficio degli holder passivi.

Inferenze ragionevoli:
- `BTC` cattura valore soprattutto in modo `indiretto ma nativo`:
  - e il bene monetario che gli utenti vogliono detenere
  - e l asset che viene accumulato da tesorerie e investitori
  - e il collateral benchmark del sistema crypto
- La cattura non passa attraverso `cash flow to holder`.
- Questo rende `BTC` molto diverso da tanti token con utility vaga:
  - non distribuisce ricavi
  - ma coincide direttamente con il prodotto monetario che il mercato vuole possedere

Claim audit
- claim: `BTC ha supply fissa a 21M`
  - evidenza migliore disponibile:
    - `Bitcoin Core Validation`
    - documentazione ufficiale
    - ordine esecutivo della Casa Bianca del `2025-03-06`
  - cosa dimostra davvero:
    - il limite massimo e parte delle regole di consenso
  - cosa non dimostra:
    - non dimostra da solo che il prezzo attuale sia basso
  - giudizio finale: `supportata`

- claim: `BTC e deflattivo`
  - evidenza a favore:
    - la remaining supply e solo `~4.69%` del massimo
    - il run-rate annuo corrente di nuova emissione e basso
  - evidenza contraria:
    - la supply continua comunque a crescere fino ai prossimi halving e oltre
  - cosa dimostra davvero:
    - inflazione monetaria molto bassa e prevedibile
  - cosa non dimostra:
    - non dimostra deflazione nominale oggi
  - giudizio finale: `non dimostrata`

- claim: `la domanda da treasury/istituzioni stringe davvero il float`
  - evidenza migliore disponibile:
    - `Strategy` passa da `687,410 BTC` il `2026-01-12` a `780,897 BTC` il `2026-04-13`
    - `CoinGecko Treasuries` mostra che Strategy resta la maggiore treasury visibile e che i governi USA e Cina restano holder rilevanti
  - cosa dimostra davvero:
    - una quota materiale di supply viene assorbita in bilanci che non sono market-making inventory di breve
  - cosa non dimostra:
    - non dimostra il float liquido esatto o una scarsita immediata per ogni fase di mercato
  - giudizio finale: `parzialmente supportata`

## 6. Supply, unlock e dilution analysis
Fatti verificabili:
- `CoinGlass` snapshot `2026-04-10`:
  - circulating supply `20.01M BTC`
  - total supply `20.01M BTC`
  - max supply `21.00M BTC`
- Questo implica che circa `95.3%` del massimo supply e gia stato emesso.
- Restano circa `984,460 BTC` da minare.
- Con subsidy corrente di `3.125 BTC` per blocco, la nuova issuance run-rate e circa `164,250 BTC` annui, pari a circa `0.82%` della supply attuale.

Float vs supply
- total supply: `~20.01M BTC`
- circulating supply: `~20.01M BTC`
- liquid circulating supply:
  - inferiore alla circolante nominale
  - una parte e in treasury aziendali o governative
  - una parte e presumibilmente persa o dormiente
  - una parte e in custodia ETF / exchange / custody rails
- exchange float:
  - non chiudibile con precisione in questo report
- treasury-held / protocol-controlled:
  - protocol-controlled treasury: `assente`
  - treasury aziendali e governative: `materiali`, ma esterne al protocollo

Source reconciliation evidence log
- dato: `spot price / market cap`
  - fonte 1: `CoinGlass` `2026-04-10`
  - tipo di fonte: `dashboard terza`
  - definizione usata: market snapshot live
  - grado di verificabilita: `probabilmente corretto ma timestamp-specific`
  - implicazione analitica: uso `CoinGlass` per un market snapshot coerente
- dato: `BTC price`
  - fonte 2: `YCharts` `2026-04-06`
  - tipo di fonte: `dashboard terza`
  - definizione usata: `price as of midnight UTC`
  - grado di verificabilita: `probabilmente corretto ma con perimetro EOD`
  - implicazione analitica: utile per serie storica, non per confronti tick-level con `CoinGlass`
- dato: `Strategy holdings`
  - fonte 3: `CoinGecko Treasuries`
  - tipo di fonte: `dashboard terza`
  - definizione usata: holdings treasury tracciate
  - grado di verificabilita: `probabilmente corretto ma soggetto a lag`
  - implicazione analitica: buono per panorama holder base, non per l ultima variazione settimanale
- dato: `Strategy holdings`
  - fonte 4: `Strategy` `8-K` del `2026-04-13`
  - tipo di fonte: `fonte primaria ufficiale`
  - definizione usata: holdings societarie dichiarate
  - grado di verificabilita: `molto alto`
  - implicazione analitica: prevale sul dato dashboard quando valuto l ultima concentrazione nota

Net supply change
- unlock cliff tradizionali: `assenti`
- emissioni: `presenti`, ma basse e deterministiche
- treasury releases del protocollo: `assenti`
- insider allocation unlock: `assenti`
- burn permanente: `assente`

Inferenze ragionevoli:
- Il rischio dilution di Bitcoin non e `opportunistico`; e `meccanico, noto e in discesa`.
- La supply netta resta in aumento fino al prossimo halving e oltre, ma in misura bassa e altamente prevedibile.
- Il vero supporto della supply story non e la narrativa di burn. E:
  - nessun team unlock
  - nessun foundation overhang
  - nessun tokenomics discretionary reset

## 7. Treasury e capital allocation
Fatti verificabili:
- Bitcoin protocol non ha treasury nativa.
- Non esiste foundation che raccolga una quota standard delle fees.
- L allocazione del capitale dentro il sistema avviene soprattutto via:
  - miner economics
  - holder behavior
  - treasury aziendali/governative esterne al protocollo

Inferenze ragionevoli:
- Il classico rischio `foundation sells into strength` qui e quasi assente a livello di protocollo.
- Il blocco da monitorare non e la treasury del protocollo, ma la concentrazione di bilancio esterna:
  - aziende come `Strategy`
  - governi
  - custodian / ETF
  - miner balance sheets
- Questo riduce i rischi di dilution discrezionale ma introduce rischi di concentrazione e di flussi forzati da soggetti molto grandi.

## 7A. Token accrual e net supply verdict
- il token riceve valore economico: `indiretto`
- il driver principale del bull case e: `scarsita credibile + reserve demand + institutional/sovereign adoption`
- i buyback sono materialmente rilevanti sul market cap attuale: `no`
- i buyback superano la pressione da unlock / emissioni: `no`
- i token riacquistati spariscono davvero: `non applicabile`
- la supply netta appare: `in aumento`
- il legame business -> token e: `forte`
- mini verdict finale della sezione: `bullish per il token`

Chiusura esplicita delle 5 domande chiave
- Il token riceve valore economico diretto, indiretto o quasi nullo?
  - `indiretto`, perche non riceve cash flow ma coincide con il bene monetario che il mercato vuole detenere
- I buyback sono abbastanza grandi da contare sul market cap attuale?
  - `no`, perche non esistono
- I buyback superano o no la pressione da unlock/emissioni?
  - `no`
- I token riacquistati spariscono davvero o possono tornare sul mercato?
  - `non applicabile`
- Il bull case dipende da business growth, buyback mechanics o narrativa di scarsita?
  - `business growth monetario + scarsita credibile + demand da bilancio`, non buyback

## 8. Posizionamento competitivo
Competitor diretti
- oro fisico e oro finanziarizzato
- `ETH` e altri crypto assets usati come collateral macro
- asset rifugio e hard-money trades

Competitor indiretti
- dollaro cash e Treasury bills
- stablecoin USD per il lato settlement digitale
- depositi bancari e money market funds per il lato `parking` del capitale

Competitor adiacenti
- sistemi di pagamento tradizionali
- network di settlement permissioned
- asset tokenizzati custodial

Fatti verificabili:
- Bitcoin resta l asset benchmark del settore per market cap, liquidita e riconoscibilita.
- La Casa Bianca nel `2025` ha gia formalizzato una lettura di Bitcoin come bene strategico scarso, distinguendolo implicitamente dal resto del settore.
- Le fonti regolatorie `SEC/CFTC` del `2026-03-11` e `2026-03-17` mostrano un contesto USA piu leggibile per i crypto asset in generale.

Inferenze ragionevoli:
- Il vantaggio vero di Bitcoin non e battere stablecoin o Visa sui pagamenti. E vincere la gara per diventare il bene monetario crypto piu credibile e il collaterale non-sovrano piu desiderabile.
- Contro l oro, Bitcoin vince su portabilita, divisibilita e settlement nativo; perde su volatilita, storia e accettazione legacy.
- Contro `ETH`, Bitcoin vince su semplicita della tesi monetaria e pulizia della supply; perde su produttivita onchain e opzionalita applicativa.
- Il mercato gia gli riconosce un premio enorme. Quindi il vantaggio competitivo esiste, ma molta parte del suo brand moat e gia prezzata.

## 9. Moat, rischio copia e dipendenze esterne
Fatti verificabili:
- Le regole monetarie e di validazione sono semplici e fortemente radicate nella cultura del protocollo.
- La rete mantiene hash rate molto elevato e liquidita globale profonda.
- Esistono gia molte copie tecniche di Bitcoin, ma nessuna ha replicato il suo status monetario.

Inferenze ragionevoli:
- Il moat di Bitcoin non e `codice non copiabile`; e `Schelling point monetario + Lindy + liquidita + brand + distribuzione del possesso`.
- Il rischio copia del prodotto tecnico e alto. Il rischio copia del premium monetario e basso.
- Le dipendenze esterne da monitorare restano reali:
  - produzione ASIC
  - energia
  - grandi custodian
  - ETF
  - governi
  - grandi tesorerie aziendali
- Quindi il business/protocollo e robusto, ma non e immune da centralizzazioni periferiche.

## 10. Market structure del token
Fatti verificabili:
- `CoinGlass` `2026-04-10`:
  - futures volume 24h `~$64.43B`
  - spot volume 24h `~$5.14B`
  - open interest `~$53.52B`
  - market cap `~$1.44T`
- `CoinGecko` `2026-04-14`:
  - 24h range `~$70.6k - $71.5k`
  - 7d range `~$67.9k - $73.5k`
  - BTC resta `~43.8%` sotto ATH
- `mempool.space` mostra fee basse e nessuna congestione estrema nella finestra osservata.

Inferenze ragionevoli:
- `BTC` non ha market structure da alt squeezabile: la liquidita e globale e profonda.
- Il prezzo e sostenuto da domanda reale di bilancio e da una struttura derivati molto grande.
- Proprio per questo la market structure non e `fragile`, ma puo essere molto violenta:
  - OI enorme
  - leva alta
  - liquidazioni capaci di accelerare squeeze e flush
- Il lato piu interessante non e la scarsita artificiale, ma il possibile irrigidimento del float liquido quando grandi holder strutturali accumulano.

Limiti informativi dichiarati
- non ho una misura unica di exchange balances
- non ho il beneficial ownership breakdown dietro gli ETF
- non ho borrow cost e short availability completi cross-venue
- quindi la confidenza sul micro-blocco `float tradabile effettivo` resta `media`

## 11. Holder base e allineamento
Fatti verificabili:
- `Strategy` dichiara ufficialmente `780,897 BTC` al `2026-04-13`.
- `Strategy` era a `687,410 BTC` il `2026-01-12`: incremento di `+93,487 BTC` in circa tre mesi.
- `CoinGecko Treasuries` mostra che Strategy resta il maggiore holder corporate visibile e che `United States` e `China` restano holder governativi di rilievo.

Inferenze ragionevoli:
- La holder base di Bitcoin e fra le piu profonde del settore:
  - retail self-custody
  - ETF/custodian
  - treasury aziendali
  - governi
  - miner
  - fondi macro / crypto
- L allineamento medio e piu lungo termine rispetto alla maggior parte dei token, ma non perfetto:
  - i miner sono seller strutturali
  - le tesorerie possono diventare seller forzati
  - i governi possono liquidare o riallocare
- Il rischio di concentrazione non e nel protocollo. E nei grandi veicoli di detenzione.

## CT-12. Recent event evidence log
- `ultimi 7d`
  - ricerca sulle fonti ufficiali e migliori fonti disponibili:
    - non ho trovato exploit core-protocol, halt o rotture di consenso sufficientemente materiali da cambiare la tesi

- `2026-04-13`
  - fonte: `Strategy 8-K`
  - tipo di fonte: `fonte primaria ufficiale`
  - stato: `confermato`
  - cosa e successo davvero:
    - Strategy ha acquistato `13,927 BTC`
    - holdings totali dichiarate: `780,897 BTC`
  - cosa e solo narrativa:
    - non dimostra da sola che il prezzo debba salire linearmente
  - market reaction osservata:
    - `CoinGecko` mostra BTC ancora in un range `~$70.6k - $71.5k` il `2026-04-14`, quindi nessun price discovery esplosivo immediato nel dato che ho
  - impatto principale: `market structure / fiducia / narrativa di scarsita`
  - stato finale: `in evoluzione`

- `2026-04-06`
  - fonte: `Strategy 8-K`
  - tipo di fonte: `fonte primaria ufficiale`
  - stato: `confermato`
  - cosa e successo davvero:
    - Strategy ha acquistato `4,871 BTC`
    - holdings totali dichiarate: `766,970 BTC`
  - cosa e solo narrativa:
    - non prova da sola un nuovo equilibrio di lungo periodo del prezzo
  - market reaction osservata:
    - il contesto di prezzo successivo resta costruttivo ma non isolabile come effetto singolo
  - impatto principale: `market structure / fiducia`
  - stato finale: `in evoluzione`

- `2026-03-17`
  - fonte: `SEC`
  - tipo di fonte: `fonte primaria ufficiale`
  - stato: `confermato`
  - cosa e successo davvero:
    - la `SEC`, congiuntamente con la `CFTC`, ha pubblicato un interpretive release che chiarisce il trattamento di varie categorie di crypto assets
    - il testo afferma che la maggior parte dei crypto assets non e di per se una security
  - cosa e solo narrativa:
    - non dimostra da sola piu flussi su BTC
  - market reaction osservata:
    - il contesto di marzo-aprile resta ordinato; non ho un repricing isolabile attribuibile solo al documento
  - impatto principale: `fiducia / market structure / regolatorio`
  - stato finale: `in evoluzione`

- `2026-03-11`
  - fonte: `SEC / CFTC` press release
  - tipo di fonte: `fonte primaria ufficiale`
  - stato: `confermato`
  - cosa e successo davvero:
    - le due agenzie hanno annunciato un `Memorandum of Understanding`
    - il testo parla di armonizzazione, chiarezza definitoria e framework piu adatto ai crypto assets
  - cosa e solo narrativa:
    - non e di per se approvazione di nuovi prodotti o garanzia di flussi
  - market reaction osservata:
    - nessun singolo spike thesis-changing isolabile, ma il segnale di regime regolatorio e costruttivo
  - impatto principale: `fiducia / market structure`
  - stato finale: `in evoluzione`

- `2026-01-12 -> 2026-04-13`
  - fonte: `Strategy` `8-K` + `Strategy purchases`
  - tipo di fonte: `fonte primaria ufficiale`
  - stato: `confermato`
  - cosa e successo davvero:
    - Strategy e passata da `687,410 BTC` a `780,897 BTC`
    - incremento netto: `+93,487 BTC`
  - cosa e solo narrativa:
    - non dimostra che tutto il capitale corporate seguira lo stesso percorso
  - market reaction osservata:
    - float tightening credibile, ma move di prezzo non attribuibile solo a questa sequenza
  - impatto principale: `market structure / holder concentration`
  - stato finale: `aperto`

## CT-13. Narrative break e trust shock test
- Non vedo un `thesis-changing structural break` recente su Bitcoin.
- Non vedo un trust shock materiale su sicurezza del protocollo o integrita del consenso.
- Vedo invece due nodi strutturali reali:
  - concentrazione crescente in grandi balance-sheet holders
  - dipendenza del bull case piu da reserve demand che da economics di fee market
- Classificazione del regime:
  - non `drama di breve`
  - non `thesis-changing structural break`
  - piu correttamente `nessun trust shock materiale, ma persiste un rischio reale di concentrazione / custodial dependency / value-anchoring ambiguity`

## 12. Thesis-change synthesis
Sviluppo 1
- data: `2026-04-13`
- sviluppo o evento: `nuova accelerazione della domanda da treasury corporate`
- cosa e confermato:
  - Strategy ha portato le proprie holdings a `780,897 BTC`
  - la sequenza `2026-01-12 -> 2026-04-13` mostra `+93,487 BTC` accumulati
- cosa resta allegation o non dimostrato:
  - che questa traiettoria sia imitata rapidamente da un ampio set di corporate treasuries
- market reaction osservata:
  - nessun blow-off immediato; il prezzo resta ben sotto ATH
- cosa cambia davvero:
  - rende piu credibile il bull case `float tightening by balance sheets`
  - aumenta il rischio di concentrazione
- quanto sembra gia prezzato: `parzialmente`
- orizzonte dell impatto residuo: `settimane / trimestri`

Sviluppo 2
- data: `2026-03-11` e `2026-03-17`
- sviluppo o evento: `regime regolatorio USA nettamente piu leggibile`
- cosa e confermato:
  - `SEC` e `CFTC` hanno formalizzato maggiore armonizzazione
  - la `SEC` ha pubblicato una lettura piu chiara del perimetro securities/non-securities
- cosa resta allegation o non dimostrato:
  - che cio si traduca in tempi brevi in domanda marginale molto piu alta su `BTC`
- market reaction osservata:
  - nessun repricing singolo pulito, ma miglioramento del backdrop istituzionale
- cosa cambia davvero:
  - riduce uno dei principali sconti di rischio storici del settore
  - favorisce Bitcoin come asset istituzionalizzabile
- quanto sembra gia prezzato: `parzialmente`
- orizzonte dell impatto residuo: `trimestri`

Sviluppo 3
- data: `2026-03-11` e `2026-04-14`
- sviluppo o evento: `il regime operativo attuale non mostra fee stress o euphoric onchain demand`
- cosa e confermato:
  - fees giornaliere e fee medie restano basse rispetto all anno precedente
  - mempool e fee rates recenti non mostrano congestione estrema
- cosa resta allegation o non dimostrato:
  - che il fee market debole oggi implichi automaticamente un problema imminente di sicurezza
- market reaction osservata:
  - il prezzo regge comunque in area `~$70k`
- cosa cambia davvero:
  - chiarisce che il bull case corrente e `reserve-demand-led`, non `fee-led`
- quanto sembra gia prezzato: `poco`
- orizzonte dell impatto residuo: `trimestri`

Mini verdict
- `evento materiale e ancora aperto`
- impatto principale: `market structure / fiducia`
- stato: `in evoluzione`
- grado di pricing percepito: `parzialmente`
- orizzonte dominante: `trimestri`

## 13. Catalizzatori
Gia noti
- prosecuzione di acquisti da parte di `Strategy` e di altre treasury pubbliche
  - impatto potenziale: `medio-alto`
  - probabilita: `media`
  - timing: `settimane / mesi`
  - gia prezzato?: `parzialmente`
- contesto regolatorio USA piu leggibile dopo i documenti `SEC/CFTC` di marzo
  - impatto potenziale: `medio`
  - probabilita: `alta`
  - timing: `mesi`
  - gia prezzato?: `parzialmente`

Probabili
- ulteriore adozione di `BTC` come treasury reserve da nuove aziende o veicoli quotati
  - impatto potenziale: `alto`
  - probabilita: `media`
  - timing: `mesi`
  - gia prezzato?: `non completamente`
- continuita della narrativa `digital gold` in un contesto macro di debasement e sfiducia verso debito sovrano
  - impatto potenziale: `alto`
  - probabilita: `media`
  - timing: `trimestri`
  - gia prezzato?: `molto, ma non totalmente`

Opzionali
- ripresa di un fee market piu robusto via maggiore uso settlement o onchain activity episodica
  - impatto potenziale: `medio`
  - probabilita: `bassa-media`
  - timing: `incerto`
  - gia prezzato?: `poco`
- espansione del ruolo di `BTC` come collateral formale in piu prodotti finanziari
  - impatto potenziale: `medio-alto`
  - probabilita: `media`
  - timing: `trimestri`
  - gia prezzato?: `parzialmente`

Puramente speculativi
- ulteriore corsa sovrana al `Bitcoin reserve` oltre i casi gia visibili
  - impatto potenziale: `molto alto`
  - probabilita: `bassa`
  - timing: `imprevedibile`
  - gia prezzato?: `poco`

## 14. Bull case
Bull case realistico
- milestone operative necessarie:
  - proseguimento dell accumulo da bilanci corporate / ETF / advisor
  - nessun trust shock regolatorio o di custodia
  - narrativa `digital gold` che resta intatta
- metriche che devono migliorare:
  - crescita holdings treasury visibili
  - tenuta di liquidita e volumi
  - nessun deterioramento materiale della hash security
- rerating plausibile:
  - ritorno verso ATH `~$126k`
  - market cap coerente `~$2.5T`
- origine del rialzo:
  - soprattutto `multiple expansion / monetary premium`
  - in misura minore `business growth monetario`

Bull case forte
- milestone operative necessarie:
  - continua adozione di BTC come treasury reserve anche oltre Strategy
  - regime USA ancora piu pro-crypto
  - conferma di BTC come asset rifugio digitale in macro incerta
- metriche che devono migliorare:
  - nuove treasury disclosure
  - volumi spot e OI che crescono senza stress di funding eccessivo
  - hash rate stabile o in crescita
- rerating plausibile:
  - area `~$150k - $175k`
  - market cap `~$3.0T - $3.5T`
- origine del rialzo:
  - quasi tutta `premium expansion`
  - solo marginalmente `fee economics`

Bull case estremo
- milestone operative necessarie:
  - ondata sovrana o quasi-sovrana
  - perdita di fiducia molto forte nelle valute fiat o nei bond lunghi
  - BTC trattato piu come riserva globale che come beta tech
- metriche che devono migliorare:
  - flussi di bilancio molto piu larghi
  - riduzione del float liquido
  - assenza di stress regolatorio
- rerating plausibile:
  - area `~$200k - $250k`
  - market cap `~$4.0T - $5.0T`
- origine del rialzo:
  - quasi interamente `monetary premium / narrativa di scarsita credibile`

## 15. Bear case
- Il bear case piu serio non e `Bitcoin smette di funzionare`. E `Bitcoin continua a funzionare ma il premium monetario si comprime`.
- Cosa rompe la tesi:
  - fallimento della narrativa `reserve asset`
  - ripresa forte dei real yields
  - ritorno del mercato a trattare BTC come semplice beta speculativo
- Execution risk:
  - non tanto nel protocollo quanto nel perimetro infrastrutturale:
    - custodia
    - ETF rails
    - financing structures delle corporate treasuries
- Regulatory risk:
  - meno drammatico che per altri token, ma ancora reale sul lato custody, accounting, tax e leverage
- Security budget risk:
  - fees troppo basse rispetto al peso del market cap restano un nodo strutturale di lungo periodo
- Liquidity risk:
  - OI molto elevato puo produrre flush violenti anche senza cambiare la tesi di fondo
- Concentrazione:
  - grandi holder aziendali o governativi possono diventare seller o overhang narrativi
- Rischio che il business vada bene ma il token no:
  - possibile se Bitcoin resta un network sicuro e rispettato ma senza nuova espansione del monetary premium
  - in quel caso la price action puo restare laterale o sotto ATH a lungo

## 16. Valuation thinking
Fatti verificabili:
- `CoinGlass` `2026-04-10`:
  - market cap `~$1.44T`
  - spot `~$72.4k`
  - circulating supply `20.01M`
- `CoinGecko` `2026-04-14`:
  - BTC resta `~43.8%` sotto l ATH del `2025-10-06`
- `YCharts / Blockchain.com`:
  - annualized user fees sul dato `2026-03-11`: `~$72.1M`
  - annualized miners revenue sul dato `2026-04-09`: `~$12.44B`

Metric perimeter reconciliation
- `market cap / annual fees` non e un multiplo economico naturale per Bitcoin, perche le fees vanno ai miner, non agli holder.
- `market cap / miners revenue` e ancora meno pulito, perche il miners revenue include in larga parte nuova emissione.
- `FDV` e quasi coincidente con `market cap` su scala pratica, perche solo `~4.69%` del supply massimo resta da minare.

Inferenze ragionevoli:
- Bitcoin non e cheap se lo tratti come asset senza cash flow e con market cap gia oltre `~$1.4T`.
- Bitcoin non e neppure chiaramente caro se lo tratti come bene monetario scarso ancora molto lontano dal dominio dell oro o di altri store-of-value globali.
- Il punto onesto e:
  - l asset e di qualita altissima
  - il mercato lo sa gia
  - il pricing non grida `mispricing evidente`
- Quindi i multipli tradizionali aiutano soprattutto a ricordare cosa Bitcoin `non e`:
  - non e equity
  - non e un protocollo a fee distribution
  - non e un alt token da rerating sulla sola riduzione di emissioni

## 17. Price map e scenario map
Scenario 1: ritorno all ATH
- prezzo implicito: `~$126,080`
- market cap implicito: `~$2.52T`
- FDV implicita: `~$2.65T` circa se uso max supply teorica
- assunzioni implicite:
  - ritorno del mercato a prezzare il massimo premium recente
  - continuita della domanda da bilancio
- probabilita qualitativa: `media`

Scenario 2: rerating moderato ma senza euforia
- prezzo implicito: `~$90,000`
- market cap implicito: `~$1.80T`
- FDV implicita: `~$1.89T`
- assunzioni implicite:
  - backdrop macro costruttivo
  - continua adozione treasury / istituzionale
  - nessun protocol shock
- probabilita qualitativa: `medio-alta`

Scenario 3: strong rerating
- prezzo implicito: `~$150,000`
- market cap implicito: `~$3.00T`
- FDV implicita: `~$3.15T`
- assunzioni implicite:
  - forte espansione del premium monetario
  - nuova ondata di capitali di lungo periodo
- probabilita qualitativa: `medio-bassa`

Scenario 4: derating a multipli mediocri
- prezzo implicito: `~$60,000`
- market cap implicito: `~$1.20T`
- FDV implicita: `~$1.26T`
- assunzioni implicite:
  - macro risk-off
  - rallentamento della domanda da treasury
  - compressione del premium
- probabilita qualitativa: `media`

Scenario 5: il business cresce ma il token non segue
- prezzo implicito: `~$70,000 - $80,000`
- market cap implicito: `~$1.40T - $1.60T`
- FDV implicita: `~$1.47T - $1.68T`
- assunzioni implicite:
  - hash rate e transazioni restano solide
  - ma la domanda da bilancio non accelera
  - il mercato tratta BTC come asset maturo
- probabilita qualitativa: `media`

Scenario 6: il token pompa solo per narrativa
- prezzo implicito: `~$110,000`
- market cap implicito: `~$2.20T`
- FDV implicita: `~$2.31T`
- assunzioni implicite:
  - leva, momentum e scarsita narrativa battono la crescita del fee market
  - nessun miglioramento strutturale paragonabile nelle economics del protocollo
- probabilita qualitativa: `medio-bassa`

## 18. Mispricing test
- cosa sta sottovalutando il mercato?
  - la pulizia estrema della supply e l assenza quasi totale di dilution discrezionale
  - la potenza del balance-sheet demand nel comprimere il float marginale
- cosa sta sopravvalutando il mercato?
  - in alcune letture, che la semplice scarsita basti sempre per un rerating lineare
  - in altre, che Bitcoin debba essere valutato come asset a fee yield per essere investibile
- qual e la variabile piu importante che quasi tutti stanno ignorando?
  - la velocita con cui capitale di bilancio e capitale custodial assorbono supply rispetto all emissione residua e ai seller strutturali
- dove sta il vero edge dell analisi?
  - nel separare `qualita del token` da `token accrual cash-flow based`: Bitcoin e eccellente come asset, ma non perche distribuisce ricavi
- cosa sto rischiando di capire male io come analista?
  - potrei sottostimare quanto rapidamente il mercato possa reratare un bene monetario quando l adozione da tesorerie supera una certa soglia
- qual e il vantaggio concreto che regge la tesi anche fuori dalla narrativa crypto, se esiste?
  - possedere e trasferire un asset scarso, digitale e non emesso da una controparte

## 18A. Strongest countercase
- La lettura piu forte contro il mio `fairly priced` e che sto trattando la domanda da tesorerie come lineare quando sta diventando strutturalmente riflessiva.
- Se `BTC` e davvero entrato nella fase `reserve asset on corporate and sovereign balance sheets`, la comparazione con vecchi cicli fee-led e troppo conservativa.
- L assunzione del mio framework che potrebbe essere troppo severa e voler vedere troppo ancoraggio economico in un asset che il mercato compra come bene monetario, non come equity.
- Il singolo sviluppo che nei prossimi `90d` renderebbe questa analisi troppo prudente sarebbe una nuova accelerazione visibile di corporate o sovereign accumulation.

## 18B. Claim audit residuale
Claim 1
- claim: `BTC ha la supply story piu pulita del settore`
- evidenza migliore disponibile:
  - cap `21M`
  - `~95.3%` gia emessi
  - nessun team unlock o foundation overhang
- cosa dimostra davvero:
  - dilution discrezionale quasi assente
- giudizio: `supportata`
- implicazione sulla confidenza o sul verdict:
  - supporta la qualita alta del token, ma non basta da sola per dire `sottovalutato`

Claim 2
- claim: `la domanda da treasury sta stringendo il float`
- evidenza migliore disponibile:
  - `Strategy` passa da `687,410 BTC` a `780,897 BTC` in tre mesi circa
- cosa dimostra davvero:
  - una parte rilevante di supply viene assorbita da holder strutturali
- giudizio: `parzialmente supportata`
- implicazione sulla confidenza o sul verdict:
  - aumenta l appeal strutturale del token, ma il float liquido esatto resta non chiuso

Claim 3
- claim: `il fee market attuale non ancora giustifica la valutazione se letto come cash flow`
- evidenza migliore disponibile:
  - fees giornaliere `~$197.6k`
  - fee media `~$0.49`
  - market cap `~$1.44T+`
- cosa dimostra davvero:
  - non c e anchor cash-flow holder-level sufficiente per leggere `BTC` come quasi-equity
- giudizio: `supportata`
- implicazione sulla confidenza o sul verdict:
  - spinge verso `fairly priced` invece che verso `cheap by default`

## 19. Residual source divergences
- `spot price / market cap`
  - fonti in conflitto: `CoinGlass`, `YCharts`, `CoinGecko`
  - differenza di definizione o perimetro:
    - `CoinGlass` e live-ish market snapshot
    - `YCharts` usa prezzo giornaliero `midnight UTC`
    - `CoinGecko` nel materiale consultato offre ranges e ATH piu che un tick unificato
  - possibile motivo della divergenza:
    - timestamp diversi e fonti dati diverse
  - implicazione analitica:
    - uso le dashboard per cio che fanno meglio e non miscelo tick e EOD come se fossero lo stesso dato

- `treasury holdings`
  - fonti in conflitto: `CoinGecko Treasuries` vs `Strategy 8-K`
  - differenza di definizione o perimetro:
    - la dashboard puo laggare
    - l `8-K` e la disclosure primaria piu recente
  - possibile motivo della divergenza:
    - ritardo di aggiornamento dashboard
  - implicazione analitica:
    - prevale sempre la disclosure primaria quando giudico la concentrazione piu recente

## 20. Checklist finale di investimento
- 3 motivi forti per essere bullish
  - `BTC` ha la supply structure piu credibile e meno diluitiva del settore
  - il prodotto monetario risolve un bisogno reale di riserva e settlement neutrale
  - la domanda da balance sheet resta un driver strutturale non banale
- 3 motivi forti per essere cauti
  - nessun holder cash flow diretto
  - market cap gia enorme, quindi il mercato conosce bene la qualita dell asset
  - concentrazione crescente in grandi holder e custodian
- 3 segnali che confermerebbero la tesi
  - nuove treasury disclosure materiali
  - tenuta o crescita dell hash rate senza shock di sicurezza
  - permanenza di un regime regolatorio USA piu leggibile e meno ostile
- 3 segnali che invaliderebbero la tesi
  - rallentamento netto o inversione dei grandi compratori strutturali
  - trust shock serio su custodia / ETF rails / governance sociale
  - compressione forte del premium monetario senza nuova domanda di lungo periodo
- 3 metriche da monitorare nei prossimi 90 giorni
  - holdings ufficiali delle maggiori tesorerie pubbliche
  - open interest e struttura della leva sui derivati
  - fee market e miners revenue per capire se il regime resta solo scarcity-led

## 21. Conclusione netta
- research mode: `full diligence`
- business quality: `alta`
- necessita di esistenza del prodotto: `alta`
- necessita del token per il prodotto: `alta`
- token quality: `alta`
- token accrual verdict: `medio`
- market setup: `favorevole`
- regime eventi recente: `evento materiale ma transitorio`
- verdict: `fairly priced`
- divergenze residue di fonti: `basse`
- confidenza del giudizio: `media`
- orizzonte temporale implicito: `medio-lungo`
- motivo principale del giudizio:
  - Bitcoin resta il miglior asset monetario crypto per scarsita, liquidita, assenza di unlock discrezionali e profondita del holder base.
  - Pero il mercato gia riconosce molta di questa qualita e non esiste una gamba cash-flow holder-level che renda ovvia la sottovalutazione.
  - Il vero upside residuo dipende da ulteriore reserve adoption e compressione del float, non da fee capture o tokenomics da yield.
