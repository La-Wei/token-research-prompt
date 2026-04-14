# Verification Audit: `Bitcoin / BTC`

## Data di verifica
- Data di verifica: `2026-04-14`
- Report verificato: `output/bitcoin-btc-2026-04-14-test/token-research-bitcoin-btc-test.md`
- Prompt base di riferimento: `prompt/token-research-prompt.md`

## Esito sintetico
- esito generale: `largamente confermato`
- scelta metodologica del report originale: `coerente`
- classificazione metodologica confermata: `full diligence`
- errori materiali trovati: `1`
- punti da aggiornare: `2`
- verdetto finale originale: `fairly priced`
- valutazione della verifica sul verdetto finale: `difendibile e non da ribaltare`

## Verifica del perimetro metodologico
- Il report originale usa davvero fonti primarie o metodologicamente forti per i blocchi che contano:
  - `bitcoin.org` e `developer.bitcoin.org` per natura del protocollo, token necessity e fee waterfall
  - `Coinbase` e `Kraken API` per il controllo same-day del prezzo
  - `mempool.space` per fee market e mining concentration
  - `Strategy 8-K` e `CoinShares` per flussi recenti, miner economics e treasury demand
- La scelta `full diligence` era coerente:
  - waterfall, supply, treasury e verdict di token accrual sono chiudibili con rigore sufficiente
  - i buchi residui su float reale, beneficial ownership e microstructure cross-venue non obbligano a passare a `opacity-compressed`
- La separazione tra `business quality`, `token quality` e `market setup` e rispettata in modo sostanziale.
- Il controllo obbligatorio su `spot price` e `market cap` passa:
  - `Coinbase` crawl same-day mostra `BTC $74,193.02`, market cap `~$1.49T`, circulating `20,015,553 BTC`
  - `Kraken REST API` same-day mostra last trade `BTC $74,727.50`
  - la differenza spot tra i due anchor e `~0.72%`, quindi non materiale
  - il market cap implicito da `Coinbase price x circulating supply` e `~$1.485T`, coerente con il `~$1.49T` riportato
- Non emerge un errore materiale di mixing tra `tick live`, `EOD` e `range` sul blocco spot finale: il report ha usato uno snapshot same-day con cross-check primario.

## Fonti usate per la verifica
- https://bitcoin.org/en/
- https://bitcoin.org/en/bitcoin-paper.html
- https://developer.bitcoin.org/devguide/transactions.html
- https://www.coinbase.com/price/bitcoin
- https://api.kraken.com/0/public/Ticker?pair=XBTUSD
- https://www.coinglass.com/currencies/BTC/futures
- https://mempool.space/
- https://mempool.space/mining
- https://bitcoincore.org/en/blog/
- https://bitcoincore.org/en/2026/01/05/wallet-migration-bug/
- https://coinshares.com/fr/insights/research-data/fund-flows-13-04-26/
- https://coinshares.com/insights/research-data/bitcoin-mining-report-q1-2026/
- https://www.strategy.com/press/strategy-acquires-13927-btc-now-holds-780897-btc_04-13-2026
- https://assets.contentstack.io/v3/assets/bltf8d808d9b8cebd37/blt3d42b5dfaeefd97a/69dc6fdaa22d2281611ded4f/form-8-k_04-13-2026.pdf

## Eventi recenti verificati
- `2026-04-13` `CoinShares Digital Asset Fund Flows`
  - confermato: inflows settimanali `~$1.1B`, con Bitcoin a `~$871M` e short-Bitcoin a `~$20.2M`
  - implicazione: conferma che Bitcoin ha continuato ad assorbire la quota principale dei flussi istituzionali della settimana
- `2026-04-13` `Strategy 8-K`
  - confermato: `13,927 BTC` acquistati per `~$1.00B`, holdings totali a `780,897 BTC`, average purchase price del periodo `~$71,902`
  - implicazione: conferma il tema di concentrazione crescente in treasury vehicles e corporate demand
- `2026-03-25` `CoinShares Bitcoin Mining Report Q1 2026`
  - confermato: weighted average cash cost `~$79,995/BTC` in `Q4 2025`, hashprice `~$29-30 / PH / day` in `Q1 2026`, fee income `consistently below 1%` del total block reward nel periodo descritto
  - implicazione: conferma che il fee market oggi non sostituisce il subsidy nel security budget
- `2026-01-05` `Bitcoin Core wallet migration bug`
  - confermato: Bitcoin Core ha dichiarato che in `30.0` e `30.1`, in circostanze rare, un fallimento della migrazione wallet poteva cancellare i file nella wallet directory
  - implicazione: evento reale di software risk / optics, ma non consensus break
- `2026-01-10` e successivi post `Bitcoin Core blog`
  - confermato: `30.2` rilasciata; blog 2026 mostra anche `29.3` e `28.4` come maintenance releases
  - implicazione: l evento di gennaio risulta chiuso lato release management
- ultimi `30d / 90d` su fonti ufficiali controllate:
  - non risultano confermati su fonti primarie un `protocol halt`, un exploit di consenso, una governance dispute materiale, un founder exit o un cambio di tokenomics / emissione che imponga un cambio di verdict sul token

## Confermato
- `Che cosa fa davvero il protocollo`
  - confermato: `bitcoin.org` descrive Bitcoin come rete P2P senza autorita centrale e dice che nessuno possiede o controlla Bitcoin
  - confermato: il whitepaper e effettivamente `Bitcoin: A Peer-to-Peer Electronic Cash System`
- `Waterfall economico`
  - confermato: `developer.bitcoin.org` dice che le transaction fees dipendono dalla byte size, dalla domanda di blockspace e vanno al miner
  - confermato: `Coinbase` dice che il miner riceve block reward in nuovo `BTC` insieme alle transaction fees
  - confermato: non esistono fee burn, buyback, treasury revenue per holder passivi o staking rewards nativi
- `Supply / token quality`
  - confermato: `Coinbase` riporta max supply `21,000,000 BTC`
  - confermato: il calcolo di issuance annuale teorica `164,250 BTC` e inflazione `~0.8206%` sulla circulating snapshot e corretto
  - confermato: non esiste un unlock schedule tipo VC/team/foundation comparabile agli alt token
- `Spot anchor / market cap`
  - confermato: `Coinbase` same-day mostra `BTC $74,193.02`, market cap `~$1.49T`, circulating `20,015,553 BTC`
  - confermato: `Kraken API` same-day mostra `BTC $74,727.50`
  - confermato: la differenza e piccola e non cambia il verdict
- `Mempool / mining structure`
  - confermato: `mempool.space` mining dashboard same-day mostra reward 144 blocchi `451.64 BTC`, average fees per block `0.0114 BTC`
  - confermato: dashboard same-day mostra `Foundry USA 28.41%`, `AntPool 18.52%`, `F2Pool 10.93%`, `ViaBTC 9.57%`, `SpiderPool 7.70%`
  - confermato: top 2 `46.93%`, top 4 `67.43%`
- `Flussi e domanda recente`
  - confermato: `CoinShares` `2026-04-13` e `Strategy 8-K` `2026-04-13` supportano la tesi di forte domanda intermediata / treasury demand
- `Scelta metodologica`
  - confermato: `full diligence` resta la classificazione giusta

## Da correggere o aggiornare
- `CoinGlass snapshot live`
  - da correggere o aggiornare: il blocco `CoinGlass` del report originale non e riproducibile sul direct open corrente della pagina stessa
  - report originale: futures volume `~$44.78B`, spot volume `~$3.02B`, open interest `~$52.17B`, market cap `~$1.42T`
  - verifica corrente sul direct open `2026-04-14`: `BTC $74,336.2`, futures volume `~$82.07B`, spot volume `~$7.75B`, market cap `~$1.49T`, open interest `~$57.03B`
  - giudizio: questo e l unico errore materiale del file originale, non perche il senso del market setup sia sbagliato, ma perche le metriche live di CoinGlass sono state catturate in un punto che oggi non torna e andavano timestampate ancora piu esplicitamente o refreshate in verifica
- `Coinbase FDV / Diluted Valuation`
  - da aggiornare nel source reconciliation: la pagina Coinbase e internamente incoerente nel widget top-card
  - il widget mostra `FDV $1.56T` ma anche `Diluted Valuation $1.49T`, mentre il testo `Recent trends` dice `fully diluted valuation $1.56T`
  - giudizio: il report ha scelto il numero economicamente piu coerente, `price x 21M = ~1.558T`, ma andava segnalata l incoerenza della fonte nello stesso punto del report e non solo a valle

## Parzialmente confermato, ma non chiuso con rigore pieno
- `Bitcoin come soprattutto monetary network piu che payments network`
  - parzialmente confermato: l inferenza e forte e ben supportata da struttura di domanda, flussi e narrativa istituzionale
  - non e chiudibile con rigore pieno perche manca una misura primaria pulita del settlement economico netto che separi pagamenti finali da self-churn / consolidamenti / custodian moves
- `Holder base e beneficial ownership`
  - parzialmente confermato: la concentrazione economica in ETF, custodian, treasury vehicles e grandi long-term holders e plausibile e coerente con i dati
  - non e chiudibile con rigore pieno senza una vista primaria completa su exchange float, ETF beneficial owners e custodian segregation
- `Market reaction causale agli eventi`
  - parzialmente confermato: prezzo e volumi settimanali si sono mossi in direzione coerente con inflows e Strategy buy
  - non e chiudibile con rigore pieno la causalita tick-by-tick di ciascun evento
- `Token accrual verdict = medio`
  - parzialmente confermato: e difendibile se si intende `indirect monetary premium capture`
  - non e una categoria puramente fattuale; con un frame piu stretto da holder cash flow si potrebbe chiamarlo `debole`

## Source reconciliation residua
- `Spot price`
  - `Coinbase` `BTC $74,193.02`
  - `Kraken API` `BTC $74,727.50`
  - divergenza: `~0.72%`
  - implicazione: non materiale; il controllo same-day passa
- `Market cap`
  - `Coinbase` market cap `~$1.49T`
  - `CoinGlass` current direct open market cap `~$1.49T`
  - implicazione: il report originale era corretto a non usare CoinGlass come verita spot finale
- `FDV`
  - `Coinbase` ha inconsistenza interna nel widget, mentre il calcolo economico `price x 21M` porta a `~$1.558T`
  - implicazione: meglio derivare il numero esplicitamente o usare una dashboard aggregata solo come cross-check
- `Mining concentration`
  - `mempool.space` usa finestre mobili di `24h / 1w / hashrate history`
  - implicazione: share dei pool possono cambiare in pochi giorni; i numeri del report originale erano validi per lo snapshot citato, ma vanno letti come finestra mobile, non come quota strutturale statica
- `CoinGlass derivatives metrics`
  - dashboard fortemente live e sensibile al timestamp
  - implicazione: utile per market structure, non adatta a diventare ancora finale non timestampato con precisione

## Valutazione del giudizio finale
- `business quality: alta`
  - valutazione verifica: `confermabile`
  - motivo: per Bitcoin la business quality va letta come qualita del bene monetario e del coordination layer, non come fee business da equity
- `necessita di esistenza del prodotto: alta`
  - valutazione verifica: `confermabile`
  - motivo: le fonti ufficiali e la struttura stessa del protocollo supportano la tesi di asset neutrale, bearer e non-sovereign
- `necessita del token per il prodotto: alta`
  - valutazione verifica: `confermabile`
  - motivo: senza `BTC` non esistono security budget, scarsita monetaria e unita economica del sistema
- `token quality: alta`
  - valutazione verifica: `confermabile`
  - motivo: hard cap reale, issuance residua bassa, assenza di unlock opportunistici e assenza di treasury overhang protocol-level
- `token accrual verdict: medio`
  - valutazione verifica: `difendibile`
  - motivo: medio solo nel senso di accrual indiretto da monetary premium; non nel senso di cash flow holder-level
- `market setup: neutro`
  - valutazione verifica: `confermabile`
  - motivo: liquidita alta e domanda strutturale presente, ma leva derivati elevata e market cap gia enorme limitano l asimmetria
- `verdict: fairly priced`
  - valutazione verifica: `confermabile`
  - motivo: la verifica non ha trovato errori tali da spostare il placement fuori dal corridoio base centrale usato dal report

## Sintesi finale
- Il report fondamentale su `Bitcoin / BTC` supera la verifica metodologica e fattuale sulla quasi totalita dei punti che contano davvero: product necessity, token necessity, waterfall, assenza di buyback/burn, supply cap, low residual issuance, eventi recenti e final verdict.
- L unico punto da correggere in modo netto e il blocco `CoinGlass` live: i numeri correnti della pagina non coincidono con quelli del report originale e vanno refreshati o marcati meglio come snapshot dinamico.
- Il resto dei buchi residui riguarda soprattutto cio che il report aveva gia dichiarato come opaco:
  - beneficial ownership
  - liquid float reale
  - causality perfetta degli eventi sui prezzi
  - market microstructure cross-venue completa
- Non emerge alcuna evidenza che obblighi a riclassificare il report da `full diligence` a `opacity-compressed`.
- Non emerge alcuna evidenza che obblighi a cambiare il giudizio finale da `fairly priced`.
