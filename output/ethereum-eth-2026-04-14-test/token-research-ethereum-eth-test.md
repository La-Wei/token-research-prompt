# Token Research: `Ethereum / ETH`

## Input usato
- `[NOME/TICKER]`: `Ethereum / ETH`
- Data snapshot principale: `2026-04-14`
- Obiettivo del test: eseguire `prompt/token-research-prompt.md` distinguendo con rigore tra business reale di Ethereum, qualita del token `ETH`, market structure e pricing

## Materiale minimo per l analisi

### Fonti principali
- Fonti ufficiali protocollo:
  - https://ethereum.org/developers/docs/gas/
  - https://ethereum.org/developers/docs/intro-to-ether
  - https://ethereum.org/staking/
  - https://eips.ethereum.org/EIPS/eip-1559
- Fonti ufficiali Ethereum Foundation / roadmap / treasury:
  - https://blog.ethereum.org/2026/02/23/commitment-to-defi
  - https://blog.ethereum.org/2026/02/24/staking
  - https://blog.ethereum.org/2026/03/13/ef-mandate
  - https://blog.ethereum.org/2026/03/23/l1-l2-ethereum
- Fonti metodologiche e market data:
  - https://www.coingecko.com/en/coins/ethereum
  - https://defillama.com/chain/Ethereum
  - https://www.coinglass.com/currencies/ETH/overview
  - https://ultrasound.money/?timeFrame=since_merge

### Snapshot numerico essenziale
- `CoinGecko` snapshot `2026-04-14`:
  - prezzo spot: `~$2,362.95`
  - market cap: `~$285.21B`
  - FDV: `~$285.21B`
  - volume 24h: `~$24.97B`
  - circulating supply: `120,690,991 ETH`
  - total supply: `120,690,991 ETH`
  - max supply: `none / non hard capped`
  - market cap / FDV: `1.0`
  - 24h range: `~$2,178.19 - $2,380.34`
  - 7d range: `~$2,071.41 - $2,371.86`
  - performance: `24h +8.0%`, `7d +12.1%`, `14d +14.4%`, `30d +12.6%`, `1y +45.1%`
  - ATH mostrato: `~$4,946.05` il `2025-08-24`
- `DeFiLlama` snapshot `2026-04-14`:
  - TVL DeFi: `~$55.82B`
  - stablecoins market cap: `~$166.08B`
  - chain fees 24h: `~$400,357`
  - chain revenue 24h: `~$78,087`
  - app revenue 24h: `~$1.61M`
  - app fees 24h: `~$8.06M`
  - DEX volume 24h: `~$1.57B`
  - perps volume 24h: `~$1.50B`
  - active addresses 24h: `~725,111`
  - transactions 24h: `~2.54M`
- `ethereum.org staking` snapshot `2026-04-14`:
  - total ETH staked: `38,884,937 ETH`
  - total validators: `923,215`
  - current APR: `2.7%`
- `CoinGlass` snapshot `2026-04-14`:
  - futures volume 24h: `~$42.04B`
  - spot volume 24h: `~$3.25B`
  - open interest: `~$25.06B`
- `Ultra Sound Money` snapshot `2026-04-14`:
  - current supply mostrata: `~121,614,129.84 ETH`
  - 7d annualized supply growth: `~+0.00%`

### Punti che restano opachi
- non ho una riconciliazione primaria perfetta, nello stesso timestamp, tra `CoinGecko`, `Ultra Sound Money` e altre dashboard sulla supply esatta
- non ho una scomposizione pulita, live e primaria di quanto delle fees 24h correnti sia `base fee` burned vs `priority fee` vs altre componenti di execution ordering
- non ho una mappa completa del `liquid float` reale, dei saldi sugli exchange e della beneficial ownership, perche `ETH` e asset nativo e gli indirizzi custodian / staking pool aggregano molti utenti
- non ho una vista unica e primaria su funding, basis, borrow cost e short availability cross-venue nello stesso istante

---

# Output del prompt

## 0. Research mode e perimetro evidenze
- qualita delle fonti: `alta`
- copertura dati: `parziale-completa`
- modalita: `full diligence`
- motivo della scelta:
  - meccanica di fee, burn, staking, issuance e uso del token sono documentati con fonti ufficiali
  - dimensione del business, market cap e market structure sono osservabili con dashboard metodologiche robuste
  - restano alcuni buchi su liquid float, beneficial ownership e riconciliazione perfetta di supply / fee perimetri, ma non impediscono un giudizio strutturale serio
- copertura market structure: `robusta`
- blocchi osservabili con rigore sufficiente:
  - necessita di esistenza del protocollo
  - necessita del token
  - waterfall economico base fee / priority fee / issuance / staking
  - assenza di unlock cliff tradizionali
  - profondita di mercato e leva derivati
  - recenti sviluppi strategici della Ethereum Foundation
- blocchi ancora non chiudibili:
  - liquid float reale e percentuale precisa di supply sugli exchange
  - scomposizione live di tutte le fees correnti tra burn e validator take
  - beneficial ownership concentration pulita
  - supply reconciliation perfetta tra dashboard
- implicazione principale dei buchi dati:
  - il verdetto deve poggiare su ordini di grandezza, non su una finta precisione del burn yield o del float
- rischio principale di errore analitico:
  - sottostimare il `monetary premium` di `ETH` trattandolo troppo come una quasi-equity da fee
- confidenza preliminare: `media`

## 1. TL;DR iniziale
- Ethereum resta il principale layer permissionless per settlement, shared state, collateral e DeFi; non e un token in cerca di prodotto.
- `ETH` e necessario per pagare gas, per validare la chain in proof-of-stake e come collateral di sistema: la necessita del token e alta.
- Ma `ETH` non e equity: la `base fee` viene burnata, mentre `priority fee`, tips e gran parte dell economia di ordering vanno ai validator; non esiste revenue share universale per gli holder passivi.
- Il lato supply e molto piu pulito di quasi tutti gli alt token: `FDV ~= market cap`, niente cliff VC classici, circa `32.2%` della supply staked.
- Il problema e che il direct accrual osservabile oggi resta piccolo rispetto a `~$285B` di market cap: anche usando un burn upper bound molto generoso, il burn yield implicito resta minimo.
- Il bull case serio su `ETH` e `settlement dominance + collateral role + monetary premium + staking demand`, non `fees flow to holders`.
- Giudizio preliminare: asset di alta qualita e token di alta qualita relativa, ma sullo snapshot `2026-04-14` il prezzo appare piu `fairly priced` che chiaramente cheap.

## 2. Che cosa fa davvero il protocollo
Fatti verificabili:
- Ethereum e una blockchain general-purpose per smart contracts, settlement, shared state e applicazioni permissionless.
- La documentazione ufficiale sull `ether` dice che `ETH` e l unica forma accettata per pagare transaction fees e, dopo `The Merge`, e richiesto per validare e proporre blocchi su Mainnet.
- La Ethereum Foundation, nel post del `2026-03-23`, descrive il ruolo di `L1` come hub permissionless e resiliente per `settlement`, `shared state`, `liquidity` e `DeFi`.
- Il post `Commitment to DeFi` del `2026-02-23` descrive la DeFi su Ethereum come driver centrale di crescita e adozione e rafforza il framing di Ethereum come `global financial settlement layer`.

Inferenze ragionevoli:
- Il problema reale che Ethereum risolve non e `emettere un altro token L1`; e offrire un layer neutrale e globale dove capitale, applicazioni e asset possano interoperare senza permessi.
- Il vantaggio concreto per l utente finale non e la velocita pura rispetto a un database centralizzato. E:
  - settlement senza intermediari
  - shared state con composability
  - collateral neutrale e riusabile
  - accesso globale 24/7
- Contro alternative centralizzate, Ethereum perde su costo, UX e compliance integration, ma vince su neutralita, programmabilita, custody e composability.
- Contro open source non tokenizzato o sistemi locali, Ethereum vince quando il punto non e solo eseguire logica, ma coordinare capitale e controparte su uno stato condiviso e credibilmente neutrale.
- Se togli `ETH`, il prodotto non resta quasi identico: salta il meccanismo di fee, il security budget PoS e una parte fondamentale del collateral layer.

Confronto esplicito con alternative realistiche
- soluzione centralizzata / API tradizionale:
  - `Stripe`, `Coinbase`, `Binance`, ledger bancari, matching engine e database privati
  - vantaggio Ethereum: settlement aperto, self-custody, shared liquidity, execution permissionless
  - svantaggio Ethereum: UX, assistenza, fiat access, compliance e costi in molti casi restano migliori lato centralizzato
- open source non tokenizzato:
  - software self-hosted, permissioned ledgers, sequencer privati, sistemi di clearing chiusi
  - vantaggio Ethereum: stato comune, final settlement e composability con capitale reale gia presente sul network
  - svantaggio Ethereum: costi di coordinamento piu alti, governance piu lenta, asset nativo volatile
- soluzione locale / self-hosted / offchain:
  - utile per un singolo operatore o consorzio
  - ma non sostituisce bene una rete neutrale dove migliaia di attori possono usare lo stesso collateral e gli stessi asset senza chiedere permesso

Vantaggio di prodotto vs vantaggio di coordinamento
- vantaggio di prodotto:
  - programmabilita affidabile
  - settlement neutrale
  - standardizzazione degli asset
- vantaggio di coordinamento / capitale:
  - deepest liquidity pool in DeFi
  - reputazione istituzionale
  - network effects su wallet, stablecoins, collateral, developer tools e rollups

Mini verdict atomico
- necessita di esistenza del prodotto: `alta`
- vantaggio vs soluzione centralizzata/API: `medio`
- vantaggio vs open source non tokenizzato o locale: `forte`
- necessita del token per il prodotto: `alta`
- il progetto e soprattutto: `prodotto superiore + coordination/capital layer`

## 3. Business quality: qualita reale del protocollo
Fatti verificabili:
- `DeFiLlama` snapshot `2026-04-14` mostra:
  - `~$55.82B` di TVL DeFi
  - `~$166.08B` di stablecoins market cap
  - `~$1.57B` di DEX volume 24h
  - `~$1.50B` di perps volume 24h
  - `~725k` active addresses 24h
  - `~2.54M` transactions 24h
- Il post EF `2026-02-23` presenta Ethereum come settlement layer finanziario globale e conferma che la DeFi resta core per la crescita dell ecosistema.
- Il post EF `2026-03-23` chiarisce che la strategia Ethereum non e `L1 contro L2`, ma `L1 come settlement/liquidity hub` e `L2 come execution expansion layer`.
- Lo stesso post dice che i `blobs` sono solo `~30%` pieni, indicando headroom di scaling senza dover concludere che l ecosistema sia gia saturo.

Metric perimeter reconciliation
- `TVL DeFi` misura capitale bloccato nel perimetro DeFi onchain, non tutto il business Ethereum.
- `stablecoins market cap` misura capitale residente, non monetizzazione del token.
- `DEX volume` e `perps volume` misurano attivita, non revenue per holder di `ETH`.
- `active addresses` e `transactions` misurano usage, non qualita economica del usage.
- La crescita del perimetro `L2` puo migliorare il business di Ethereum senza comparire linearmente nelle fees `L1` di un singolo giorno.

Inferenze ragionevoli:
- La business quality di Ethereum resta `alta` in senso crypto assoluto, non solo relativo:
  - profondita di capitale
  - centralita nelle stablecoins
  - ruolo di collateral layer
  - densita di applicazioni
  - credibilita istituzionale
- La domanda e di qualita mediamente superiore a gran parte del settore:
  - piu finanza reale e collateral
  - meno dipendenza esclusiva da narrativa memecoin / one-shot activity
- Il limite non e l assenza di business. Il limite e che una parte crescente del business viene compressa o redistribuita tra:
  - L2
  - app layer
  - validator / proposer economics
  - servizi infra
- Quindi Ethereum puo essere un business/protocollo eccellente anche se il pass-through al token passivo non e lineare.

Speculazioni:
- Se il flywheel `L1 settlement + L2 execution + ETH collateral` si chiude meglio sul piano UX e liquidity sharing, la business quality puo migliorare ancora senza richiedere esplosione delle fees L1.
- Se invece il valore economico continua a spostarsi verso L2 e app token senza un rafforzamento chiaro della capture di `ETH`, il business puo restare forte ma il token puo reratare meno di quanto la narrativa spera.

## 4. Unit economics e qualita dei ricavi
Fatti verificabili:
- `ethereum.org` spiega che la fee totale e `gas used * (base fee + priority fee)`.
- La stessa documentazione dice che:
  - la `base fee` e impostata dal protocollo
  - la `priority fee` e un tip all validator
  - la `base fee` viene burnata
- Il technical intro to ether dice che nuova emissione di `ETH` viene creata come reward per validator e che i block proposers ricevono anche `tips` e `MEV-related income`, ma questi non sono nuova emissione.
- `DeFiLlama` snapshot `2026-04-14`:
  - chain fees 24h: `~$400,357`
  - chain revenue 24h: `~$78,087`
  - app fees 24h: `~$8.06M`
  - app revenue 24h: `~$1.61M`

Flow of value waterfall
- `gross user fees`:
  - gas fees pagate in `ETH` dagli utenti su L1
  - economicamente includono almeno `base fee` e `priority fee`
- `protocol revenue retained`:
  - non esiste come treasury cash-flow per holder
  - la componente trattenuta in modo irreversibile e il burn della `base fee`
- `validator revenue`:
  - issuance di nuovo `ETH`
  - `priority fees`
  - porzioni di ordering / MEV economics
- `tokenholder revenue`:
  - non esiste una revenue share universale per chi detiene passivamente `ETH`
  - l holder beneficia soprattutto via:
    - burn
    - domanda obbligatoria di gas
    - staking se decide di stakeare
    - collateral / reserve demand
- `staking rewards budget`:
  - emissione protocol-defined legata al set di validator / stake

Buyback quality test
- buyback: `non applicabile`
- fonte: nessun programma di buyback nativo del protocollo
- percentuale esatta: `0`
- base di calcolo: `nessuna`
- natura: `inesistente`
- destinazione finale di eventuali riacquisti: `non applicabile`
- effetto su supply: `non applicabile`

Stress test sulla monetizzazione diretta del token
- uso il dato `DeFiLlama` piu favorevole del giorno:
  - chain fees 24h `~$400,357`
- se assumo in modo estremamente favorevole e irrealistico che tutto questo importo corrisponda a valore burnato, l annualizzazione e solo `~$146.1M`
- contro `~$285.21B` di market cap, il `direct burn yield` massimo teorico e solo `~0.05%`
- il burn reale osservabile per gli holder e inferiore a questo upper bound, perche non tutte le componenti della spesa utente sono burnate in ugual misura

Inferenze ragionevoli:
- Il business di Ethereum e grande; il `cash-flow look-through` diretto per l holder passivo di `ETH` e piccolo.
- L economia del network si distribuisce tra:
  - burn
  - staker / validator
  - MEV / ordering rails
  - app layer
  - collateral premium di `ETH`
- Questo non rende `ETH` un token debole; rende pero fuorviante trattarlo come una quasi-equity a fee capture.

## 5. Token: come cattura valore davvero
Fatti verificabili:
- `ETH` e necessario per pagare gas.
- `ETH` e richiesto per validare e proporre blocchi dopo il passaggio a proof-of-stake.
- `ethereum.org/staking` mostra `38,884,937 ETH` staked, `923,215` validators e `2.7%` APR.
- Il technical intro to ether dice che `ETH` e usato come primary collateral nei mercati DeFi.

Inferenze ragionevoli:
- `ETH` cattura valore in modi diversi:
  - `diretto` via burn della base fee
  - `diretto ma non universalmente holder-level` via staking rewards per chi partecipa
  - `indiretto` via domanda di collateral, reserve asset e settlement asset
- Il problema e che queste forme di cattura non equivalgono a una revenue share lineare.
- Se il business cresce ma il token non segue, la spiegazione piu probabile non e che il protocollo sia inutile. E che il valore economico si sia fermato prima di arrivare al passive holder.

Claim audit
- claim: `ETH e strutturalmente deflattivo`
  - evidenza primaria a favore:
    - la `base fee` viene burnata
    - `Ultra Sound Money` mostra supply growth 7d annualized vicina a `0.00%`
  - evidenza primaria contraria:
    - esiste issuance continua da staking
    - le dashboard non mostrano un regime di deflazione ampia e stabile nello snapshot usato
  - cosa dimostra davvero:
    - `ETH` ha un meccanismo di burn reale e supply molto piu disciplinata di gran parte del settore
  - cosa non dimostra:
    - non dimostra deflazione permanente o forte
  - giudizio finale: `parzialmente supportata`

- claim: `la crescita di L2 e app layer arriva automaticamente agli holder di ETH`
  - evidenza migliore disponibile:
    - EF descrive esplicitamente il rapporto L1/L2 come flywheel strategico
    - `ETH` resta l asset di settlement e collateral del sistema
  - cosa dimostra davvero:
    - esiste un ponte economico e strategico tra crescita dell ecosistema e domanda di `ETH`
  - cosa non dimostra:
    - non dimostra pass-through lineare verso burn o holder revenue
  - giudizio finale: `parzialmente supportata`

- claim: `ETH e necessario al prodotto`
  - evidenza migliore disponibile:
    - docs ufficiali su gas, staking e intro to ether
  - cosa dimostra davvero:
    - senza `ETH` il protocollo perde fee market, PoS security e gran parte del collateral logic
  - cosa non dimostra:
    - non dimostra che il prezzo attuale sia cheap
  - giudizio finale: `supportata`

## 6. Supply, unlock e dilution analysis
Fatti verificabili:
- `CoinGecko` snapshot `2026-04-14`:
  - circulating supply `120,690,991 ETH`
  - total supply `120,690,991 ETH`
  - max supply `none`
  - market cap / FDV `1.0`
- `ethereum.org/staking`:
  - total ETH staked `38,884,937 ETH`
  - equivalente a circa `32.2%` della supply usata in questo report
- `Ultra Sound Money` snapshot `2026-04-14`:
  - current supply mostrata `~121.61M ETH`
  - supply growth 7d annualized `~+0.00%`

Float vs supply
- total supply: `~120.69M ETH` secondo `CoinGecko`
- circulating supply: `~120.69M ETH` secondo `CoinGecko`
- liquid circulating supply:
  - inferiore alla circulating nominale
  - circa `32.2%` della supply e staked
  - altra quota rilevante e immobilizzata in DeFi, bridge, treasury o custody infrastructure
- exchange float:
  - non chiuso con precisione in questo report
- treasury-held / protocol-controlled:
  - Ethereum protocol non ha una treasury holder-level comparabile a un app token
  - esiste treasury della `Ethereum Foundation`, ma non e claim degli holder di `ETH`

Source reconciliation evidence log
- dato: `current / circulating supply`
  - fonte 1: `CoinGecko`
  - tipo di fonte: `dashboard terza`
  - definizione: market-cap supply / circulating supply
  - grado di verificabilita: `probabilmente corretto ma dashboard-based`
  - implicazione analitica: `120.69M ETH`
- dato: `current supply`
  - fonte 2: `Ultra Sound Money`
  - tipo di fonte: `dashboard metodologica`
  - definizione: supply formula basata su execution balances, beacon balances e beacon deposits
  - grado di verificabilita: `probabilmente corretto ma non riconciliato qui al 100% con CoinGecko`
  - implicazione analitica: `~121.61M ETH`

Net supply change
- unlock cliff tradizionali: `assenti`
- emissioni: `presenti`, ma molto inferiori rispetto a modelli L1 inflation-heavy pre-Merge
- burn: `reale`, ma variabile con il regime di utilizzo
- treasury releases tipo VC token: `non rilevanti come blocco separato`

Inferenze ragionevoli:
- Il rischio `unlock overhang` classico non e il problema di `ETH`.
- Il rischio vero e piu sottile:
  - overpricing della narrativa `deflattiva`
  - confusione tra supply nominalmente tutta circolante e float realmente liquido
- La supply story di `ETH` resta una delle piu pulite nel settore:
  - niente cliff grandi
  - `FDV ~= market cap`
  - meccanica di burn reale
- Ma `ETH` non va venduto a se stessi come hard-cap asset alla Bitcoin: non lo e.

## 7. Treasury e capital allocation
Fatti verificabili:
- Ethereum protocol non distribuisce una `treasury revenue` ai token holder.
- La `Ethereum Foundation Treasury Policy` del `2025-06-04` dice che:
  - target annual opex = `15%` della treasury
  - `2.5` anni di opex buffer
  - possono esserci vendite periodiche di `ETH` per mantenere il buffer
  - le strategie correnti includono `solo staking` e `wETH` supplied a protocolli di lending
- Il `2026-02-24` la Ethereum Foundation ha annunciato di aver iniziato a stakeare `~70,000 ETH`, con rewards dirette di ritorno alla EF treasury.

Inferenze ragionevoli:
- La treasury rilevante da analizzare qui non e `holder treasury`, ma `EF treasury`.
- Questa treasury e `ecosystem-first`, non `holder-yield-first`.
- L allocazione puo essere positiva per il protocollo:
  - funding di sviluppo
  - uso di ETH-denominated rails
  - supporto a DeFi permissionless
- Ma non crea automaticamente una claim economica per il possessore di `ETH`.
- Esiste anche un tradeoff:
  - una governance treasury piu disciplinata migliora la fiducia
  - eventuali future vendite di `ETH` per esigenze operative restano comunque potenziale flusso di offerta

## 7A. Token accrual e net supply verdict
- il token riceve valore economico: `diretto e indiretto, ma non equity-like`
- il driver principale del bull case e: `business growth + settlement premium + collateral demand + monetary premium`
- i buyback sono materialmente rilevanti sul market cap attuale: `no`
- i buyback superano la pressione da unlock / emissioni: `no`
- i token riacquistati spariscono davvero: `non applicabile`; le `base fee` burnate si
- la supply netta appare: `stabile`
- il legame business -> token e: `medio-forte`
- mini verdict finale della sezione: `bullish per il token`

Chiusura esplicita delle 5 domande chiave
- Il token riceve valore economico diretto, indiretto o quasi nullo?
  - `diretto e indiretto`, ma con direct accrual troppo piccolo per leggerlo come equity
- I buyback sono abbastanza grandi da contare sul market cap attuale?
  - `no`, perche non esistono
- I buyback superano o no la pressione da unlock/emissioni?
  - `no`
- I token riacquistati spariscono davvero o possono tornare sul mercato?
  - `non applicabile`; il burn della base fee e permanente
- Il bull case dipende da business growth, buyback mechanics o narrativa di scarsita?
  - `business growth + collateral / settlement demand + monetary premium`, non buyback

## 8. Posizionamento competitivo
Competitor diretti
- `Solana`
- `Base` e altri L2 nel perimetro Ethereum allargato
- `BNB Chain`
- `Sui`
- `Aptos`

Competitor indiretti
- exchange custodial
- payment APIs e ledger centralizzati
- sistemi finanziari permissioned e tokenization stacks chiusi

Competitor adiacenti
- Bitcoin come asset monetario crypto di riferimento
- stablecoin stacks che catturano uso ma non necessariamente valore per `ETH`
- app layer dominanti che possono catturare economics sopra Ethereum

Fatti verificabili:
- Ethereum compete con un vantaggio evidente su:
  - liquidity density
  - DeFi depth
  - collateral credibility
  - developer and institutional trust
- La strategia ufficiale EF sul rapporto L1/L2 suggerisce che Ethereum voglia difendere il primato non su `cheap monolithic execution`, ma su `settlement + shared liquidity + security + credible neutrality`.

Inferenze ragionevoli:
- Il vantaggio vero di Ethereum non e avere l L1 piu economico. E essere il posto dove il capitale serio si fida di restare.
- Il vantaggio rispetto alle alternative centralizzate e forte solo per chi valorizza:
  - self-custody
  - composability
  - neutral settlement
- Per molti utenti retail o enterprise tradizionali, il centralizzato resta migliore lato UX e compliance.
- Il mercato riconosce gia a Ethereum un premio da `blue-chip crypto infrastructure`.
- C e spazio per rerating se il flywheel `L2 growth -> ETH demand` diventa piu leggibile.
- C e anche rischio di compressione del premio se il mercato decide che il settlement moat non monetizza abbastanza.

## 9. Moat, rischio copia e dipendenze esterne
Fatti verificabili:
- EF definisce Ethereum come rete che deve rimanere `censorship resistant`, `open source`, `private` e `secure`.
- EF presenta il rapporto L1/L2 come coordinazione intenzionale per rafforzare l ecosistema nel suo insieme.
- Il protocollo non dipende da un singolo founder operativo o da una singola azienda nel modo tipico di molti token piu giovani.

Inferenze ragionevoli:
- Il moat di Ethereum e molto piu difficile da copiare di un vantaggio di throughput:
  - brand tecnico
  - capital base
  - standard sociali e tecnici
  - layer di collateral
  - composability storica
- Le dipendenze esterne restano pero reali:
  - stablecoin issuers
  - staking providers
  - relay / MEV infrastructure
  - L2 teams
  - governance sociale del protocollo
- Ethereum appare un business/protocollo robusto, ma non e immune da valore leakage:
  - le app possono vincere sopra Ethereum
  - le L2 possono catturare UX e parte dell economics
  - i validator possono catturare una quota significativa dell ordering value

## 10. Market structure del token
Fatti verificabili:
- `CoinGecko` snapshot `2026-04-14`:
  - spot volume 24h aggregato `~$24.97B`
  - market cap `~$285.21B`
  - 24h range `~$2,178 - $2,380`
- `CoinGlass` snapshot `2026-04-14`:
  - futures volume 24h `~$42.04B`
  - spot volume 24h `~$3.25B`
  - open interest `~$25.06B`
- `CoinGecko` mostra `7d +12.1%` e `30d +12.6%`.

Inferenze ragionevoli:
- `ETH` non ha market structure da token squeezable o fragile per scarsita artificiale.
- La liquidita e profonda, globale e istituzionalizzabile.
- Il rischio di prezzo non e un cliff di supply o una float story opaca. E piu probabilmente:
  - positioning derivati
  - reflexivity macro / crypto beta
  - compressione o espansione del `monetary premium`
- L open interest e abbastanza grande da amplificare velocemente i movimenti.
- Quindi il mercato di `ETH` e `profondo e serio`, ma non affatto privo di violenza tattica.

Limiti informativi dichiarati
- non ho borrow cost e short availability puliti
- non ho funding e basis cross-venue nello stesso timestamp
- non ho una misura primaria e unica della supply sugli exchange
- quindi la confidenza sul micro-blocco derivati resta `media`

## 11. Holder base e allineamento
Fatti verificabili:
- `~38.88M ETH` sono staked secondo `ethereum.org`
- i validator mostrati sono `923,215`
- `ETH` e asset nativo, non ERC-20, quindi gli indirizzi top aggregano grandi custodian, exchange e staking providers

Inferenze ragionevoli:
- La holder base di `ETH` e fra le piu profonde e varie del settore:
  - investitori retail
  - fondi crypto
  - DeFi native treasuries
  - stakers
  - istituzioni con esposizione infrastrutturale
- Una base di holder forte esiste davvero, ma la concentrazione non va letta ingenuamente dagli address top:
  - molta concentrazione apparente e concentrazione di infrastruttura, non sempre di beneficial ownership
- Il rischio di allineamento non e tanto `insider unlock seller`.
- E piu:
  - concentrazione nei service providers
  - centralizzazione relativa dello staking
  - divergenza tra interessi dell ecosistema e interessi del passive holder

## CT-12. Recent event evidence log
- `ultimi 7d`
  - ricerca sulle fonti ufficiali usate in questo report:
    - non ho trovato un evento thesis-changing confermato su Ethereum negli ultimi `7d`
    - non ho trovato exploit core-protocol, halt o rotture di governance sufficientemente materiali da cambiare da soli la tesi

- `2026-03-23`
  - fonte: `Ethereum Foundation Blog`
  - tipo di fonte: `fonte primaria ufficiale`
  - stato: `confermato`
  - cosa e successo davvero:
    - EF ha chiarito il rapporto desiderato tra `L1` e `L2`
    - ha ribadito il ruolo di Ethereum `L1` come hub di settlement, shared state, liquidity e DeFi
    - ha dichiarato che i `blobs` sono solo `~30%` pieni, quindi c e headroom di scaling
  - cosa e solo narrativa:
    - non dimostra da solo che il valore economico catturato da `ETH` aumentera in modo materiale
  - market reaction osservata:
    - `ETH` nello snapshot `2026-04-14` e `+12.1%` sui `7d` e `+12.6%` sui `30d`, ma non ho un move isolabile attribuibile solo a questo post
  - impatto principale: `business / narrativa / fiducia`
  - stato finale: `in evoluzione`

- `2026-03-13`
  - fonte: `Ethereum Foundation Blog`
  - tipo di fonte: `fonte primaria ufficiale`
  - stato: `confermato`
  - cosa e successo davvero:
    - EF ha pubblicato il proprio `Mandate`, insistendo su principi come `censorship resistant`, `open source`, `private`, `secure`
  - cosa e solo narrativa:
    - non dimostra di per se miglioramento immediato di token accrual o crescita
  - market reaction osservata:
    - nessun repricing thesis-changing isolabile
  - impatto principale: `fiducia / governance optics`
  - stato finale: `chiuso ma con effetto reputazionale residuo`

- `2026-02-24`
  - fonte: `Ethereum Foundation Blog`
  - tipo di fonte: `fonte primaria ufficiale`
  - stato: `confermato`
  - cosa e successo davvero:
    - EF ha iniziato a stakeare `~70,000 ETH` della propria treasury
    - i rewards tornano alla EF treasury
  - cosa e solo narrativa:
    - non implica una nuova revenue share per holder di `ETH`
  - market reaction osservata:
    - impatto di prezzo diretto non isolabile
  - impatto principale: `token / fiducia / treasury discipline`
  - stato finale: `in evoluzione`

- `2026-02-23`
  - fonte: `Ethereum Foundation Blog`
  - tipo di fonte: `fonte primaria ufficiale`
  - stato: `confermato`
  - cosa e successo davvero:
    - EF ha rafforzato pubblicamente il commitment a `DeFi` e alla tesi di Ethereum come settlement layer finanziario
  - cosa e solo narrativa:
    - non dimostra automaticamente migliore monetizzazione di `ETH`
  - market reaction osservata:
    - nessun price shock isolabile in questo report
  - impatto principale: `business / narrativa`
  - stato finale: `in evoluzione`

## CT-13. Narrative break e trust shock test
- Non vedo un `thesis-changing structural break` recente su Ethereum.
- Non vedo un trust shock materiale su sicurezza, solvibilita o controllo founder.
- Vedo invece un nodo strutturale reale che il mercato continua a discutere:
  - Ethereum ha un moat forte, ma il modo in cui quel moat si traduce in valore per il passive holder di `ETH` resta meno lineare della narrativa piu bullish
- Classificazione del regime:
  - non `drama di breve`
  - non `thesis-changing structural break`
  - piu correttamente `nessun trust shock materiale, ma persiste un rischio reale di execution / value-capture interpretation`

## 12. Thesis-change synthesis
Sviluppo 1
- data: `2026-03-23`
- sviluppo o evento: `chiarimento del flywheel L1/L2 e headroom sui blobs`
- cosa e confermato:
  - EF vuole rafforzare il ruolo di Ethereum L1 come settlement and liquidity hub
  - i blobs non sono ancora saturi
- cosa resta allegation o non dimostrato:
  - che piu utilizzo L2 si trasformi presto in un miglior direct accrual per `ETH`
- market reaction osservata:
  - nessun repricing isolabile
- cosa cambia davvero:
  - migliora la leggibilita della tesi `Ethereum as settlement layer`
  - non risolve da solo il nodo `ETH not equity`
- quanto sembra gia prezzato: `parzialmente`
- orizzonte dell impatto residuo: `trimestri`

Sviluppo 2
- data: `2026-02-24`
- sviluppo o evento: `treasury staking della Ethereum Foundation`
- cosa e confermato:
  - `~70k ETH` vengono messi a staking con rewards che tornano in treasury
- cosa resta allegation o non dimostrato:
  - che questo cambi in modo materiale il profilo prezzo di `ETH`
- market reaction osservata:
  - nessun move thesis-changing isolabile
- cosa cambia davvero:
  - migliora l allineamento simbolico e operativo tra EF treasury e ETH rails
  - non crea payout universale agli holder
- quanto sembra gia prezzato: `poco`
- orizzonte dell impatto residuo: `trimestri`

Sviluppo 3
- data: `2026-03-13`
- sviluppo o evento: `EF Mandate e maggiore chiarezza su principi e stewardship`
- cosa e confermato:
  - EF ha formalizzato una postura piu chiara su valori e ruolo
- cosa resta allegation o non dimostrato:
  - che questo acceleri da solo roadmap, fees o adozione
- market reaction osservata:
  - nessun move isolabile
- cosa cambia davvero:
  - riduce un po il discount da governance opacity
  - aiuta `fiducia` piu che `token economics`
- quanto sembra gia prezzato: `poco-parzialmente`
- orizzonte dell impatto residuo: `settimane / trimestri`

Mini verdict
- `evento materiale ma transitorio`
- impatto principale: `business / fiducia / narrativa`
- stato: `in evoluzione`
- grado di pricing percepito: `parzialmente`
- orizzonte dominante: `trimestri`

## 13. Catalizzatori
Gia noti
- `maggiore utilizzo dei blobs e migliore integrazione L1/L2`
  - impatto potenziale: rafforza la tesi di Ethereum come settlement layer invece di semplice L1 costoso
  - probabilita: `alta`
  - timing: `prossimi trimestri`
  - gia prezzato: `parzialmente`
- `crescita continua di stablecoins, collateral e DeFi su Ethereum`
  - impatto potenziale: aumenta la domanda strutturale di `ETH` come collateral e reserve asset
  - probabilita: `alta`
  - timing: `trimestri`
  - gia prezzato: `in parte`

Probabili
- `miglioramento dell UX e della liquidity portability tra L1 e L2`
  - impatto potenziale: chiude meglio il flywheel economico di Ethereum
  - probabilita: `media`
  - timing: `90-180 giorni`
  - gia prezzato: `poco`
- `ulteriore crescita dello staking nativo e istituzionale`
  - impatto potenziale: comprime il float effettivo e rafforza la base holder di lungo periodo
  - probabilita: `media`
  - timing: `trimestri`
  - gia prezzato: `parzialmente`

Opzionali
- `miglioramento visibile del burn regime con piu domanda onchain`
  - impatto potenziale: rafforza la narrativa di supply discipline
  - probabilita: `media-bassa`
  - timing: `dipende dal regime di utilizzo`
  - gia prezzato: `poco`
- `rollup stack piu trustless / native rollups`
  - impatto potenziale: rende piu credibile il moat del perimetro Ethereum nel lungo termine
  - probabilita: `media-bassa`
  - timing: `trimestri / anni`
  - gia prezzato: `poco`

Puramente speculativi
- `ETH come corporate / institutional reserve asset fuori dal solo perimetro crypto-native`
  - impatto potenziale: grande multiple expansion da monetary premium
  - probabilita: `bassa`
  - timing: `anni`
  - gia prezzato: `poco`

## 14. Bull case
Bull case realistico
- milestone operative:
  - Ethereum mantiene il primato in DeFi, stablecoins e collateral
  - il rapporto L1/L2 diventa economicamente piu leggibile
  - il burn resta almeno sufficiente a mantenere supply quasi piatta nei periodi di attivita sana
- metriche che devono migliorare:
  - usage qualitativo
  - blob demand
  - ETH staked / collateralized
- rerating multiplo giustificabile:
  - premio da `settlement asset` e non da fee token puro
- market cap / FDV sensati:
  - area `~$386B - $434B`
- parte del rialzo:
  - mix di business quality, collateral demand e multiple expansion moderata

Bull case forte
- milestone operative:
  - Ethereum rafforza nettamente il proprio ruolo come base layer della finanza onchain
  - L2 e app layer crescono senza rompere il legame economico col perimetro `ETH`
  - il mercato torna a pagare un forte premium da `blue-chip crypto collateral`
- metriche che devono migliorare:
  - fees / burn normalized
  - capital resident on Ethereum
  - segnali di stronger institutional allocation
- rerating multiplo giustificabile:
  - ritorno a un premium simile o superiore al picco recente
- market cap / FDV sensati:
  - ritorno verso ATH, `~$597B`
- parte del rialzo:
  - piu `multiple expansion + monetary premium` che cash-flow economics

Bull case estremo
- milestone operative:
  - regime risk-on molto favorevole
  - narrativa dominante di `ETH` come global crypto reserve collateral dopo `BTC`
  - ulteriore compressione del float economico tramite staking e collateral lock
- metriche che devono migliorare:
  - quasi tutte le macro-metriche del perimetro Ethereum
  - crescita forte di domanda finale e allocazione di capitale
- rerating multiplo giustificabile:
  - soprattutto da narrativa e capitale, non da revenue share
- market cap / FDV sensati:
  - area `~$724B`
- parte del rialzo:
  - dominata da multiple expansion e monetary premium

## 15. Bear case
- Il business puo restare ottimo e il token puo comunque non essere cheap:
  - e il bear case piu serio.
- Le L2 possono continuare a vincere su UX mentre `ETH` cattura solo in parte quel successo.
- Le fees L1 possono restare troppo basse per sostenere una narrativa forte di burn-driven scarcity.
- Validator economics, staking providers e app layer possono catturare piu valore del passive holder.
- Il protocollo puo apparire robusto ma lento, lasciando spazio a competitor con UX migliore e piu momentum.
- Un cambio regolatorio sfavorevole su staking, stablecoins o servizi di custody puo ridurre la domanda marginale.
- La market structure profonda non elimina drawdown: con `~$25B` di open interest, il prezzo puo muoversi in modo violento anche senza cambiare i fondamentali.
- Il rischio concettuale chiave:
  - che il mercato smetta di pagare `settlement premium` e torni a guardare piu freddamente il piccolo direct accrual osservabile.

## 16. Valuation thinking
Fatti verificabili:
- prezzo attuale: `~$2,362.95`
- market cap attuale: `~$285.21B`
- FDV: `~$285.21B`
- TVL DeFi: `~$55.82B`
- chain fees 24h:
  - `DeFiLlama ~ $400,357`
  - `CoinGecko Financial Data ~ $234,448`
- chain revenue 24h:
  - `DeFiLlama ~ $78,087`
  - `CoinGecko Financial Data ~ $67,458.53`
- app revenue 24h `DeFiLlama`: `~$1.61M`

Metric perimeter reconciliation
- `TVL` non e l intero business di Ethereum.
- `chain fees` non sono sinonimo di burn e non sono sinonimo di holder revenue.
- `chain revenue` non e sinonimo di revenue distribuita agli holder.
- `app revenue` descrive economia sopra Ethereum, non economia incassata direttamente da `ETH`.
- Quindi i multipli equity-like vanno usati solo come test di severita, non come fair-value model unico.

Multipli e sanity checks
- `mcap / TVL`: `~5.1x`
- `mcap / annualized chain fees` usando `DeFiLlama`:
  - `~1,950x`
- `mcap / annualized chain fees` usando `CoinGecko` financial data:
  - `~3,330x`
- `mcap / annualized chain revenue` usando `DeFiLlama`:
  - `~10,000x`
- `mcap / annualized app revenue` usando `DeFiLlama`:
  - `~485x`
  - ma questo non e tokenholder revenue

Burn yield sanity check
- se tratto in modo iper-generoso tutte le `chain fees` `DeFiLlama` del giorno come burn value:
  - burn annualizzato massimo teorico `~$146.1M`
- questo implica appena `~0.05%` di burn yield sul market cap attuale
- il burn economico reale per l holder passivo e inferiore a questo upper bound

Inferenze ragionevoli:
- `ETH` non e economico se lo valuti come fee token.
- `ETH` non e necessariamente caro se lo valuti come:
  - collateral of system
  - settlement asset
  - reserve asset del perimetro DeFi / Ethereum
- Il mercato oggi non sta pagando i flussi di cassa correnti di `ETH`.
- Sta pagando:
  - il moat del network
  - la centralita del collateral
  - la qualita della supply story
  - la probabilita che Ethereum resti il layer dominante per il capitale onchain serio

Verdetto di valuation
- come `cash-flow token`: `costoso`
- come `strategic settlement / collateral asset`: `difendibile`
- conclusione pratica: il prezzo attuale non grida sottovalutazione evidente, ma neanche euforia pura; lo leggo come `fairly priced`

## 17. Price map e scenario map
Scenario base di riferimento
- prezzo: `~$2,362.95`
- market cap: `~$285.21B`
- FDV: `~$285.21B`
- assunzioni implicite:
  - Ethereum resta asset blue-chip del settore
  - il mercato paga gia il moat, ma non il massimo premium storico
- probabilita qualitativa: `gia reale`

Ritorno all ATH
- prezzo: `~$4,946.05`
- market cap: `~$596.85B`
- FDV: `~$596.85B`
- assunzioni implicite:
  - ritorno pieno del premium storico
  - contesto macro / crypto molto piu favorevole
- probabilita qualitativa: `bassa-media`

Rerating a premium piu forte ma sotto ATH
- prezzo: `~$3,200 - $3,600`
- market cap: `~$386.21B - $434.49B`
- FDV: `~$386.21B - $434.49B`
- assunzioni implicite:
  - migliore lettura del flywheel L1/L2
  - business forte e market premium in espansione moderata
- probabilita qualitativa: `media`

Rerating forte da monetary premium
- prezzo: `~$4,000`
- market cap: `~$482.76B`
- FDV: `~$482.76B`
- assunzioni implicite:
  - ETH viene pagato sempre piu come reserve collateral asset
  - la supply discipline viene percepita come abbastanza forte
- probabilita qualitativa: `bassa-media`

Derating a lettura piu severa del direct accrual
- prezzo: `~$1,800`
- market cap: `~$217.24B`
- FDV: `~$217.24B`
- assunzioni implicite:
  - il mercato chiede fee capture piu tangibile
  - il premium da settlement asset si comprime
- probabilita qualitativa: `media`

Derating forte
- prezzo: `~$1,500`
- market cap: `~$181.04B`
- FDV: `~$181.04B`
- assunzioni implicite:
  - crescita ecosistema deludente o non monetizzata
  - forte compressione di multiple e positioning
- probabilita qualitativa: `bassa-media`

Scenario in cui il business cresce ma il token non segue
- prezzo: `~$2,200 - $2,800`
- market cap: `~$265.52B - $337.93B`
- FDV: `~$265.52B - $337.93B`
- assunzioni implicite:
  - DeFi / L2 / app layer migliorano
  - ma il mercato continua a dubitare del pass-through economico a `ETH`
- probabilita qualitativa: `alta`

Scenario in cui il token pompa solo per narrativa
- prezzo: `~$4,500 - $6,000`
- market cap: `~$543.11B - $724.15B`
- FDV: `~$543.11B - $724.15B`
- assunzioni implicite:
  - forte capital rotation
  - rialzo guidato da premium e positioning piu che da fee economics
- probabilita qualitativa: `bassa`, ma non zero

## 18. Mispricing test
- cosa sta sottovalutando il mercato?
  - la qualita reale di Ethereum come settlement and collateral layer globale
- cosa sta sopravvalutando il mercato?
  - la facilita con cui il successo dell ecosistema si traduce in passive holder economics
- qual e la variabile piu importante che quasi tutti stanno ignorando?
  - la differenza tra `ETH come money/collateral` e `ETH come fee token`
- dove sta il vero edge dell analisi?
  - separare `business winner` da `cash-flow token` senza perdere di vista che `ETH` puo meritare un premium anche senza revenue share
- cosa sto rischiando di capire male io come analista?
  - che il mercato possa avere ragione a pagare un premium molto piu alto per il ruolo monetario di `ETH` rispetto a quanto la mia severita sui flussi correnti suggerisce
- qual e il vantaggio concreto che regge la tesi anche fuori dalla narrativa crypto, se esiste?
  - un layer neutrale di settlement e collateral globale, composable e non custodial

## 18A. Strongest countercase
- La lettura piu forte contro il mio verdict e che `ETH` non debba essere valutato quasi mai su fees o revenue, ma come principale asset monetario e collateral del sistema onchain dopo `BTC`.
- Se questo framework e corretto, allora la mia insistenza su burn yield e chain revenue e utile come guardrail ma troppo severa come anchor di fair value.
- Il singolo sviluppo che nei prossimi `90d` renderebbe questa analisi troppo prudente sarebbe una combinazione di:
  - piu forte crescita del flywheel L1/L2
  - maggiore domanda strutturale di staking / collateral
  - espansione visibile del premium di mercato senza deterioramento dei fondamentali

## 18B. Claim audit residuale
- claim: `ETH e strutturalmente deflattivo`
  - evidenza migliore disponibile: burn ufficiale della base fee + dashboard supply che mostrano regime vicino alla stabilita
  - cosa dimostra davvero: supply discipline superiore alla maggior parte del settore
  - giudizio: `parzialmente supportata`
  - implicazione sulla confidenza o sul verdict: impedisce di costruire il bull case principale su scarsita meccanica forte

- claim: `la crescita del perimetro Ethereum arriva automaticamente agli holder di ETH`
  - evidenza migliore disponibile: ruolo di ETH in gas, staking, collateral e L1 settlement
  - cosa dimostra davvero: esiste connessione economica reale
  - giudizio: `parzialmente supportata`
  - implicazione sulla confidenza o sul verdict: sostiene business quality alta, ma non un token discount evidente

- claim: `ETH e necessario al prodotto`
  - evidenza migliore disponibile: docs ufficiali su gas, staking e intro to ether
  - cosa dimostra davvero: alta necessita strutturale del token
  - giudizio: `supportata`
  - implicazione sulla confidenza o sul verdict: rafforza la token quality relativa

## 19. Residual source divergences
- `Current supply`
  - fonti in conflitto: `CoinGecko` vs `Ultra Sound Money`
  - differenza di definizione o perimetro:
    - `CoinGecko`: `120,690,991 ETH`
    - `Ultra Sound Money`: `~121,614,129.84 ETH`
  - possibile motivo della divergenza:
    - metodologia diversa
    - tempi di aggiornamento diversi
    - diversa lettura del beacon-related accounting
  - implicazione analitica:
    - la divergenza e troppo piccola per cambiare il verdict
    - ma basta per evitare precisione finta su supply-based multiples

- `24h fees / revenue`
  - fonti in conflitto: `DeFiLlama` vs `CoinGecko Financial Data`
  - differenza di definizione o perimetro:
    - `DeFiLlama`: `~$400k fees`, `~$78k revenue`
    - `CoinGecko`: `~$234k fees`, `~$67k revenue`
  - possibile motivo della divergenza:
    - timestamp diversi
    - metodologia dashboard diversa
    - perimetro diverso nel classificare revenue chain-level
  - implicazione analitica:
    - i multipli exact-point sono rumorosi
    - il messaggio strutturale pero non cambia: i flussi diretti sono piccoli contro il market cap

- `Spot volume 24h`
  - fonti in conflitto: `CoinGecko` vs `CoinGlass`
  - differenza di definizione o perimetro:
    - `CoinGecko`: `~$24.97B`
    - `CoinGlass`: `~$3.25B`
  - possibile motivo della divergenza:
    - venue coverage e metodologia differenti
    - CoinGlass e piu orientato al perimetro derivati e selected venues
  - implicazione analitica:
    - non va usato un singolo numero per giudicare la profondita
    - il punto robusto resta che `ETH` e altamente liquido

## 20. Checklist finale di investimento
- 3 motivi forti per essere bullish
  - Ethereum resta il perimetro piu credibile per settlement, collateral e DeFi di scala
  - `ETH` e necessario per gas, staking e security del protocollo
  - la supply story e molto pulita: niente grossi unlock, `FDV ~= market cap`, burn reale

- 3 motivi forti per essere cauti
  - il direct accrual osservabile resta piccolo rispetto a `~$285B` di market cap
  - una parte importante del valore economico viene catturata fuori dal passive holder di `ETH`
  - il mercato gia riconosce a Ethereum un premio di qualita consistente

- 3 segnali che confermerebbero la tesi
  - il business dell ecosistema continua a crescere piu velocemente del pass-through holder-level
  - il mercato continua a pagare `ETH` soprattutto come collateral / settlement asset
  - la supply resta disciplinata senza entrare in una forte narrativa deflattiva non meritata

- 3 segnali che invaliderebbero la tesi
  - burn e fees normalized crescono tanto da rendere il token materially better on direct accrual
  - il flywheel L1/L2 diventa piu chiaro e il mercato ha ancora pricing troppo basso
  - forte compressione del float economico tramite staking / collateral che il mercato non aveva anticipato

- 3 metriche da monitorare nei prossimi 90 giorni
  - chain fees / burn regime e relativo rapporto con issuance
  - ETH staked e segnali di compressione del float effettivo
  - stablecoins, DeFi capital e segnali di migliore economic coupling tra L2 growth e `ETH`

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
- orizzonte temporale implicito: `medio`
- motivo principale del giudizio:
  - Ethereum e uno dei pochissimi asset crypto con prodotto reale, token necessario e supply story pulita.
  - Pero il valore economico che arriva in modo diretto e universalmente osservabile agli holder di `ETH` resta piccolo rispetto alla capitalizzazione attuale; il mercato sta pagando soprattutto moat, collateral role e monetary premium.
  - Questo rende `ETH` un asset di alta qualita, ma non chiaramente sottovalutato sullo snapshot `2026-04-14`.
