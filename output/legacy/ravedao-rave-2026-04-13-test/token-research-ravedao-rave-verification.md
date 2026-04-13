# Verification Audit

## Data di verifica
- Protocollo / ticker verificato: `RaveDAO / RAVE`
- Report verificato: `output/ravedao-rave-2026-04-13-test/token-research-ravedao-rave-test.md`
- Prompt base di riferimento: `prompt/token-research-prompt.md`
- Data di verifica: `2026-04-13`
- Approccio: verifica di claim strutturali, waterfall, token rights, supply, vesting, treasury, metriche live ed eventi recenti usando sito ufficiale, whitepaper ufficiale, filing MiCAR, explorer onchain, CoinGecko come dashboard metodologicamente chiara per market data e pagine ufficiali di Coinbase dove disponibili

## Esito sintetico
- Esito generale: `confermato nel nucleo, con alcune correzioni metodologiche importanti`
- Il cuore del report regge:
  - `RaveDAO` ha un business / event brand reale e non puramente cartaceo
  - `RAVE` non conferisce diritti economici su profitti, ricavi o dividendi
  - la narrativa `buyback & burn` non e sufficientemente chiusa con rigore documentale
  - il mercato oggi ha venue quality migliore ma resta dominato da `reflexivity + float dynamics + narrative`
  - il verdetto `token quality bassa` resta il punto piu robusto dell analisi
- Le correzioni principali che emergono dalla verifica sono:
  - `Coinbase spot availability` va trattata come `confermata`, non solo come indizio di venue improvement
  - la lettura `ecosystem residual gia in vesting lineare` e `molto plausibile`, ma non va elevata a fatto pienamente chiuso senza una disclosure ufficiale piu esplicita
  - `staking`, `loyalty rewards` e parte delle utility vanno distinte tra `documentate come design` e `live usage verificato`
  - il sanity check sui buyback e utile come bound analitico, ma non e una prova primaria di meccanica economica effettiva

## Fonti usate per la verifica
- https://ravedao.com/
- https://ravedao.gitbook.io/ravedao-whitepaper
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/impact-metrics
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics/token-distribution-schedule
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics/token-utilities
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics/usdrave-cross-chain-bridge
- https://ravedao.github.io/rave-xhtml/
- https://www.coingecko.com/en/coins/ravedao
- https://www.coinbase.com/advanced-trade/spot/RAVE-USD
- https://x.com/CoinbaseMarkets/status/2019132783679971728
- https://etherscan.io/token/0x17205fab260a7a6383a81452ce6315a39370db97
- https://etherscan.io/tx/0xbb0323aff38f0308ee1df9bffed145426e7f6dd7e2ecc86ce4569f49300d3039

## Eventi recenti verificati
- `Evento confermato`
  - `2026-02-04`: `Coinbase Markets` ha aggiunto `RAVE` alla roadmap pubblica tramite account ufficiale.
  - `2026-04-13`: la pagina ufficiale `Coinbase Advanced Trade` mostra il mercato spot `RAVE-USD`, quindi la disponibilita spot su Coinbase e confermata alla data di verifica.
  - `2026-04-13`: `CoinGecko` conferma ATH `~$9.79`, `24h +272.6%`, `7d +3830.3%`, market cap `~$2.386B`, FDV `~$9.620B`, volume 24h `~$638.17M`.
  - `2026-04-13`: `CoinGecko Markets` mostra venue spot rilevanti e piu credibili del setup precedente, con `Coinbase Exchange`, `Kraken`, `Gate` e `Bitget` tra le venue principali.

- `Allegation o claim non dimostrato`
  - `Binance Futures catalyst`: CoinGecko lo segnala nel blocco `Recently Happened`, ma nella verifica non ho recuperato un annuncio Binance primario sufficientemente pulito per chiudere il punto con pieno rigore.
  - causalita precisa del rally di aprile 2026: non e chiusa. Venue improvement, roadmap/listing effect, leverage, meme reflexivity e order flow possono aver contribuito insieme.
  - buyback / burn come meccanica economicamente rilevante: resta non dimostrato.

- `Risposta del team / fonte primaria`
  - non ho trovato nel perimetro verificato una risposta ufficiale del team che chiarisca in modo numerico buyback, burn, wallet di treasury o andamento del vesting beyond quanto mostrato nei docs
  - la fonte primaria piu forte per i diritti del token resta il filing MiCAR
  - la fonte primaria piu forte per la schedule resta la page `Token Distribution Schedule`, che pero contiene un wording ambiguo tra summary e category detail

- `Market reaction osservata`
  - `CoinGecko` nello snapshot verificato mostra:
    - prezzo `~$9.62`
    - `24h +272.6%`
    - market cap `~$2.386B`
    - FDV `~$9.620B`
    - 24h volume `~$638.17M`
    - ATH `~$9.79` il `2026-04-13`
  - `CoinGecko Markets` mostra inoltre:
    - `Coinbase Exchange RAVE/USD` circa `~$155.0M` di volume 24h
    - `Gate RAVE/USDT` circa `~$101.7M`
    - `Bitget RAVE/USDT` circa `~$78.9M`
    - `Kraken RAVE/USD` circa `~$51.1M`

- `Lettura 7d / 30d / 90d`
  - ultimi `7d`: il fatto dominante e il price shock verticale, non un miglioramento dimostrato del waterfall economico
  - ultimi `30d`: passaggio da ATL `2026-03-12` a ATH `2026-04-13`; enorme rerating di prezzo senza prova equivalente di rerating del token accrual
  - ultimi `90d`: l evento piu materiale e la sequenza `Coinbase roadmap -> spot availability`, che migliora accesso e venue quality ma non cambia i diritti economici del token
  - non ho trovato in fonti primarie exploit, halt, outage, governance breakdown, azioni regolatorie o team departure materialmente thesis-changing negli ultimi `90d`

## Confermato
- `Descrizione del progetto`: confermata. RaveDAO e meglio descritto come `event / entertainment brand tokenizzato` o `cultural coordination layer`, non come protocollo infrastrutturale classico.
- `Business reale`: confermato. Sito ufficiale, whitepaper e MiCAR supportano eventi reali, sponsor, ticketing, membership e footprint internazionale.
- `Revenue business reale`: confermato. Il filing MiCAR dichiara `~$3M` di revenue cumulata `2024-2025 YTD` e dettaglia le linee di ricavo.
- `Event economics dichiarate`: confermate come team-reported nel filing. Il MiCAR indica costi per evento `~$100k - $1.5M` e gross margins tipici `20% - 40%`.
- `No token sale / no equity fundraising / no debt`: confermato dal filing MiCAR.
- `Token rights limitati`: confermato. Il filing MiCAR esclude `ownership`, `equity rights`, `claims on profits`, `revenues` e `dividends`.
- `Governance consultativa`: confermata. Il filing MiCAR dice che la governance non modifica i diritti legali, finanziari o strutturali del token.
- `Supply cap 1B`: confermato.
- `Issuer retained 200M`: confermato nel filing MiCAR.
- `Circulating vs vesting imbalance`: confermato. CoinGecko mostra `248,044,444` circulating contro `751,955,556` nel vesting address.
- `Contrasto whitepaper vs MiCAR sul buyback`: confermato. Il whitepaper marketing parla di `Buyback & Burn`, mentre il MiCAR dichiara `Supply Adjustment Protocols: false` e `Token Value Protection Schemes: false`.
- `Bridge mechanics rilevanti per leggere i burn`: confermato. Il docs ufficiale dichiara bridge via Stargate fra Ethereum, Base e BNB Chain, e un tx example mostra `Transfer` verso zero address assieme a `LayerZero PacketSent`.
- `Venue quality molto migliorata`: confermata. CoinGecko Markets e la pagina ufficiale `Coinbase Advanced Trade` supportano la lettura che il setup non sia piu solo da venue marginali.
- `Market setup ancora riflessivo`: confermato. L ampiezza del rally e il turnover giornaliero supportano pienamente questa lettura.

## Da correggere o aggiornare
- `Ecosystem residual gia in vesting lineare`
  - nel report originale la formulazione e abbastanza assertiva: `il dettaglio live della token schedule implica che... stia gia vestando linearmente`
  - questa lettura e numericamente molto coerente con la circolante attuale, ma resta una `inferenza forte`, non una disclosure esplicita e univoca
  - implicazione: il punto va mantenuto, ma con wording piu prudente tipo `best-fit inference` invece di `fatto chiuso`

- `Staking / loyalty / payments`
  - il report originale presenta queste utilita come caratteristiche del token in modo corretto sul piano documentale, ma in alcuni passaggi il lettore puo recepirle come `live verified usage`
  - il filing MiCAR dice che `staking and loyalty reward functions are scheduled to launch in the next development phase`
  - implicazione: distinguere meglio tra `documented utility design` e `live verified operational usage`

- `Sanity check sui buyback`
  - il bound fatto nel report e utile per mostrare ordini di grandezza
  - ma non va letto come verifica di buyback reali ne come misura del vero buyback budget
  - implicazione: trattarlo esplicitamente come `stress test illustrativo`, non come dato osservato

- `CoinGecko vesting address + issuer retained 200M`
  - entrambi i numeri sono reali nelle rispettive fonti
  - ma senza wallet mapping non va assunto che rappresentino due inventory completamente separate e additive
  - implicazione: usare i due dati come segnali di concentrazione, non come somma certa di supply controllata non-overlapping

## Parzialmente confermato, ma non chiuso con rigore pieno
- `Buyback & burn come meccanica economica rilevante`
  - confermato che il marketing lo promette
  - non confermato che esista una meccanica sistematica, quantificata e verificabile onchain

- `On-chain transparency del business`
  - il MiCAR dice che una parte significativa dei ricavi e processata onchain
  - ma non fornisce wallet addresses o reporting che permetta di ricostruire il waterfall

- `Utility live del token oltre la partecipazione`
  - `ticketing`, `payments`, `staking`, `loyalty`, `community rewards` sono ben documentati nei materiali ufficiali
  - non ho pero prova primaria sufficiente, nella verifica di oggi, per chiudere il perimetro di adozione live e il peso economico di ciascun sink

- `Metriche di scala`
  - `100k+ participants`, `50k+ NFT tickets`, `150M+ impressions` sono presenti nel whitepaper ufficiale
  - restano pero principalmente `team-reported`, non auditati da dashboard indipendenti riconciliate

- `Perimetro burn permanente vs bridge`
  - e confermato che almeno parte delle burn-looking traces e compatibile con bridge mechanics
  - non ho una riconciliazione completa di tutti i transfer verso zero address, quindi la prudenza del report resta corretta

- `Binance Futures catalyst`
  - il blocco `Recently Happened` di CoinGecko lo cita
  - ma senza un annuncio Binance primario, nella verifica va lasciato come `secondario / non pienamente chiuso`

## Valutazione del giudizio finale
- `Business quality: media`
  - giudizio difendibile.
  - La verifica conferma che il business esiste davvero ed e piu sostanziale della media dei token narrativi, ma resta piccolo, team-reported su molte metriche e execution-heavy.

- `Necessita di esistenza del prodotto: media-bassa`
  - giudizio confermato.
  - Il vantaggio concreto esiste soprattutto come brand / sponsor coordination / crypto-native distribution, molto meno come superiorita prodotto inevitabile per l utente finale.

- `Token quality: bassa`
  - giudizio confermato e, se possibile, rafforzato.
  - Il filing MiCAR rende molto chiaro che il token non e equity-like e che la governance e consultativa.

- `Market setup: fragile ma liquido`
  - giudizio confermato.
  - La parte `liquido` e oggi meglio supportata di prima grazie alle venue spot osservate; la parte `fragile` resta vera per via di valuation, float dynamics e reflexivity.

- `Verdict: sopravvalutato`
  - resta il giudizio piu rigoroso sullo snapshot verificato.
  - La verifica non smonta la tesi; semmai la rende piu precisa: venue quality migliore e business reale non bastano a colmare la debolezza del value accrual del token.

- `Confidenza del giudizio: media`
  - giudizio corretto.
  - Non va alzata a `alta` perche restano aperti i punti su vesting interpretation, live token usage, wallet transparency e causalita esatta del rally.

## Sintesi finale
- Il report fondamentale su `RaveDAO / RAVE` regge nel suo asse principale:
  - `business reale`
  - `token rights deboli`
  - `buyback narrative non chiusa`
  - `market setup riflessivo`
- I punti piu forti confermati dalla verifica sono:
  - il filing MiCAR sul lato rights / governance / supply
  - il contrasto con il whitepaper marketing sul lato `buyback & burn`
  - la conferma di venue spot piu solide, in particolare `Coinbase`
- Le correzioni principali da portarsi dietro sono quattro:
  - trattare `Coinbase spot` come `confermato`
  - trattare `ecosystem residual in vesting` come `inferenza forte`, non come fatto definitivamente chiuso
  - distinguere meglio `utility documentata` da `live usage verificato`
  - non leggere il sanity check sui buyback come evidenza primaria di accrual
- Il giudizio finale `sopravvalutato` con `token quality bassa` e `market setup fragile ma liquido` resta il piu disciplinato anche dopo la verifica.
