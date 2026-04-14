# Verification Audit

## Data di verifica
- Protocollo / ticker verificato: `Bitcoin / BTC`
- Report verificato: `output/bitcoin-btc-2026-04-14-test/token-research-bitcoin-btc-test.md`
- Prompt base di riferimento: `prompt/token-research-prompt.md`
- Data di verifica: `2026-04-14`
- Approccio:
  - verifica di claim strutturali, waterfall, supply, absence of buyback/treasury, holder-base concentration, metriche live, eventi recenti `7d / 30d / 90d`, source reconciliation e verdetto finale usando `bitcoin.org`, `developer.bitcoin.org`, `bitcoincore.org`, `Strategy` `8-K`, `SEC`, `White House`, `CoinGecko`, `CoinGlass`, `YCharts / Blockchain.com` e `mempool.space`

## Esito sintetico
- Esito generale: `confermato nel nucleo, con aggiornamenti e una correzione metodologica sul log eventi`
- Il cuore del report regge:
  - `BTC` ha necessita del token `alta`
  - la supply cap a `21M` e reale e verificabile
  - non esiste treasury di protocollo, buyback o revenue share holder-level
  - il bull case corretto resta `monetary premium + reserve demand + balance-sheet absorption`, non fee capture
  - il verdetto `fairly priced` resta disciplinato sullo snapshot verificato
- Gli aggiornamenti principali emersi nella verifica sono:
  - il `recent event log` del fondamentale sottostima la densita delle disclosure `Strategy` negli ultimi `30d / 90d`
  - il blocco `ultimi 90d` del report originale usa anche il `2026-01-12`, che e fuori dalla finestra rigorosa di `90d` rispetto al `2026-04-14`
  - `CoinGlass` resta utile per leggere derivati e profondita del mercato, ma va maneggiato con cautela come fonte spot/market-cap perche i crawls mostrano snapshot molto diversi
- Il punto che non cambia:
  - Bitcoin non ha direct accrual holder-level sufficiente per essere letto come quasi-equity; la tesi di investimento resta monetaria, non cash-flow based

## Verifica del perimetro metodologico
- La scelta `full diligence` del report originale e `coerente`.
- Motivo:
  - i blocchi decisivi sono verificabili con rigore sufficiente:
    - cap di supply
    - fee mechanics
    - block reward mechanics
    - assenza di treasury e buyback
    - assenza di unlock discrezionali
    - holder concentration visibile lato corporate/government
    - regime recente di domanda da balance sheet
  - restano aperti ma non bloccanti:
    - float realmente liquido
    - quota precisa di coin perse
    - beneficial ownership dietro ETF, custodian e grandi indirizzi
    - sostenibilita molto long-run del security budget fee-only
- Il report quindi non andava in `opacity-compressed`.
- Anche il cap di confidenza `media` resta corretto:
  - `business / token necessity / supply` sono forti
  - la parte `fair value` resta inevitabilmente meno chiudibile con rigore da spreadsheet perche Bitcoin e un bene monetario, non un fee token

## Fonti usate per la verifica
- https://bitcoin.org/en/how-it-works
- https://bitcoin.org/en/bitcoin-core/features/validation
- https://developer.bitcoin.org/devguide/transactions.html
- https://developer.bitcoin.org/reference/block_chain.html
- https://bitcoincore.org/en/releases/30.1/
- https://www.strategy.com/press/strategy-acquires-1031-btc-and-now-holds-762099-btc_03-23-2026
- https://www.strategy.com/press/strategy-acquires-4871-btc-and-now-holds-766970-btc_04-06-2026
- https://www.strategy.com/press/strategy-acquires-13927-btc-now-holds-780897-btc_04-13-2026
- https://www.strategy.com/purchases
- https://www.sec.gov/newsroom/press-releases/2026-26-sec-cftc-announce-historic-memorandum-understanding-between-agencies
- https://www.sec.gov/newsroom/press-releases/2026-30-sec-clarifies-application-federal-securities-laws-crypto-assets
- https://www.whitehouse.gov/presidential-actions/2025/03/establishment-of-the-strategic-bitcoin-reserve-and-united-states-digital-asset-stockpile/
- https://www.coingecko.com/en/coins/bitcoin/usd?chart=7_days
- https://www.coingecko.com/en/treasuries
- https://www.coinglass.com/currencies/BTC
- https://www.coinglass.com/open-interest/BTC
- https://mempool.space/
- https://ycharts.com/indicators/bitcoin_network_hash_rate
- https://ycharts.com/indicators/bitcoin_transactions_per_day
- https://ycharts.com/indicators/bitcoin_total_transaction_fees_per_day
- https://ycharts.com/indicators/bitcoin_average_transaction_fee

## Eventi recenti verificati
- `Evento confermato`
  - `2026-04-13`: `Strategy` ha acquistato `13,927 BTC` e ha dichiarato holdings totali pari a `780,897 BTC`
  - `2026-04-06`: `Strategy` ha acquistato `4,871 BTC` e ha dichiarato holdings totali pari a `766,970 BTC`
  - `2026-03-23`: `Strategy` ha acquistato `1,031 BTC` e ha dichiarato holdings totali pari a `762,099 BTC`
  - `2026-03-17`: la `SEC` ha pubblicato `SEC Clarifies the Application of Federal Securities Laws to Crypto Assets`
  - `2026-03-11`: `SEC` e `CFTC` hanno annunciato un `historic Memorandum of Understanding` tra le agenzie
  - non ho trovato, nelle fonti ufficiali controllate per gli ultimi `7d / 30d / 90d`, un exploit di consenso, halt di rete o rottura di sicurezza core-protocol thesis-changing

- `Allegation o claim non dimostrato`
  - il claim `treasury demand stringe in modo dimostrabile il float liquido` resta solo `parzialmente dimostrato`:
    - e dimostrato che grandi holder stanno accumulando
    - non e chiudibile con rigore il float liquido residuo
  - il claim `regime regolatorio USA piu chiaro = domanda marginale inevitabilmente piu alta su BTC` non e dimostrato in modo lineare
  - il claim `security budget futuro fee-only sara sufficiente` non e chiudibile con i dati correnti

- `Risposta del team / fonte primaria`
  - la fonte primaria piu forte per il cap monetario e `Bitcoin Core Validation`, che esplicita che la validazione piena impedisce di accettare blocchi che violano il limite di `21M`
  - la fonte primaria piu forte per fee mechanics e `developer.bitcoin.org`, che esplicita che la transaction fee viene data al miner
  - la fonte primaria piu forte per `block reward = subsidy + fees` e la documentazione `block_chain`
  - la fonte primaria piu forte per gli acquisti corporate recenti e la sequenza di `8-K` di `Strategy`

- `Market reaction osservata`
  - `CoinGecko` snapshot verificato `2026-04-14` mostra:
    - prezzo `~$70,869.91`
    - market cap `~$1.4186T`
    - volume 24h `~$28.10B`
    - performance `24h +0.9%`, `7d +1.6%`, `30d +0.5%`, `1y +16.5%`
    - 24h range `~$70,617 - $71,524`
    - 7d range `~$67,947 - $73,538`
  - `CoinGlass` crawls recenti confermano comunque una struttura derivati molto grande, ma con spot snapshot non perfettamente stabili tra una cattura e l altra
  - `mempool.space` mostra un regime operativo non congestionato:
    - fee rates bassi
    - nessuna evidenza di fee panic o chain stress

- `Lettura 7d / 30d / 90d`
  - ultimi `7d`:
    - evento materiale confermato: `Strategy` `8-K` del `2026-04-13`
    - nessun trust shock di protocollo
  - ultimi `30d`:
    - sequenza `Strategy` del `2026-03-23`, `2026-04-06`, `2026-04-13`
    - chiarimento regolatorio USA con `SEC` `2026-03-17`
  - ultimi `90d`:
    - `SEC/CFTC` `2026-03-11`
    - accumulation corporate continua
    - nessun evento core-protocol negativo thesis-changing confermato nelle fonti ufficiali controllate

## Confermato
- `Supply cap a 21M`: confermato.
  - `Bitcoin Core Validation` conferma esplicitamente che la validazione piena protegge il limite finale di `21M`.

- `Fee flow ai miner`: confermato.
  - `developer.bitcoin.org` conferma che la transaction fee viene data al miner.

- `Block reward = subsidy + fees`: confermato.
  - la documentazione `block_chain` conferma che transaction fees e block subsidy insieme costituiscono il `block reward`.

- `Assenza di treasury, buyback e holder revenue share`: confermata.
  - il protocollo non trattiene fees per gli holder
  - non esistono buyback nativi
  - non esiste payout holder-level passivo

- `Token necessity alta`: confermata.
  - `BTC` coincide con l asset monetario del protocollo; senza `BTC` salta il fee market, il reward economics e il bene stesso che la rete vuole preservare

- `Supply story pulita`: confermata.
  - `CoinGecko` verificato `2026-04-14` mostra:
    - circulating supply `20,015,150 BTC`
    - max supply `21,000,000 BTC`
    - `market cap / FDV = 1.0`
  - il run-rate di emissione corrente resta basso e deterministico

- `Il bull case non e fee-capture`: confermato.
  - con `~$197,568` di fees giornaliere il `2026-03-11`, l annualizzazione resta circa `~$72.1M`
  - contro `~$1.4186T` di market cap verificato, il multiplo `market cap / annualized fees` resta circa `19,673x`
  - il messaggio del report originale regge: Bitcoin non va letto come quasi-equity

- `Security budget oggi subsidy-led`: confermato.
  - fees giornaliere `~$197,568`
  - miners revenue giornaliero `~$34.09M`
  - quindi le fees restano una quota piccola del security budget corrente

- `Holder concentration crescente via balance sheets`: confermata nel segnale, non nel float finale.
  - le `8-K` di `Strategy` confermano accumulo materiale e ricorrente

- `Verdetto finale fair value`: confermato.
  - `fairly priced` resta la sintesi piu rigorosa sullo snapshot verificato

## Da correggere o aggiornare
- `Finestra 90d da ripulire`
  - nel `CT-12` originale compare la sequenza `2026-01-12 -> 2026-04-13`
  - rispetto a data report `2026-04-14`, il `2026-01-12` e fuori dalla finestra rigorosa degli ultimi `90d`
  - implicazione:
    - il dato `2026-01-12` puo restare come contesto holder-base piu ampio
    - non va presentato come `recent event evidence log` strettamente `90d`

- `Event log corporate incompleto`
  - il report fondamentale logga bene `2026-04-06` e `2026-04-13`, ma omette almeno:
    - `2026-03-23` `Strategy` `+1,031 BTC`
  - implicazione:
    - il report sottostima la densita delle disclosure `Strategy` negli ultimi `30d`

- `CoinGlass non va trattato come anchor spot principale`
  - i crawls recenti di `CoinGlass` mostrano snapshot spot/material cap abbastanza variabili:
    - un crawl recente mostra `BTC ~ $68,551`, market cap `~$1.367T`, OI `~$45.63B`
    - il report originale usa `~$72,373`, market cap `~$1.44T`
    - `CoinGecko` verificato mostra `~$70,869.91`, market cap `~$1.4186T`
  - implicazione:
    - `CoinGlass` e utile soprattutto per derivati, `OI`, liquidazioni e struttura di mercato
    - per lo spot valuation anchor conviene usare `CoinGecko` o fonte spot equivalente

- `Regime eventi recente leggermente da riqualificare`
  - il report chiude `regime eventi recente: evento materiale ma transitorio`
  - alla luce della sequenza di accumulation corporate e del backdrop regolatorio USA, il framing piu preciso sembra:
    - `evento materiale e ancora aperto`
  - questo non basta a cambiare il `verdict` finale, ma cambia il tono del regime recente

## Parzialmente confermato, ma non chiuso con rigore pieno
- `Float liquido davvero compresso`
  - gli acquisti corporate sono confermati
  - il float liquido residuo non e chiudibile con rigore pieno perche ETF, custodian, exchange e coin perse non sono riconciliati in un unico dataset primario

- `Holder base reale`
  - la lettura qualitativa del report e buona
  - la beneficial ownership dietro grandi veicoli e wallet aggregati resta poco leggibile

- `Security budget long-run`
  - il report ha ragione a segnalare il tema
  - non si puo chiudere con rigore pieno solo dai dati live di oggi se il fee-only regime futuro sara sufficiente

- `Impatto regolatorio USA sul pricing`
  - `SEC/CFTC` e `SEC` confermano un backdrop piu leggibile
  - non chiudono da soli l entita del pass-through su domanda e prezzo di `BTC`

## Source reconciliation residua
- `Spot price / market cap`
  - `CoinGecko` verificato `2026-04-14`:
    - prezzo `~$70,869.91`
    - market cap `~$1.4186T`
  - `CoinGlass` crawls recenti:
    - range osservato circa `~$68.6k - $72.4k`
    - market cap circa `~$1.367T - $1.44T`
  - implicazione:
    - divergenza non thesis-changing
    - abbastanza grande da imporre disciplina sul tipo di fonte usata per ciascuna metrica

- `Treasury holdings`
  - `Strategy` ufficiale `2026-04-13`: `780,897 BTC`
  - `CoinGecko Treasuries` crawl pubblico piu vecchio:
    - `Strategy 762,099 BTC`
    - `Total Treasury Holding 1,796,225 BTC` circa
  - `CoinGecko` coin page verificata `2026-04-14`:
    - `Total Treasury Holding 1,797,196 BTC`
  - implicazione:
    - i dashboard treasury sono utili per il panorama
    - le filing ufficiali prevalgono sempre per la verifica dei grandi holder

- `Metriche onchain live`
  - `YCharts / Blockchain.com` porta series utili ma con lag di alcuni giorni o settimane a seconda della metrica
  - `mempool.space` e piu adatto al regime operativo immediato
  - implicazione:
    - il report fondamentale era corretto nel distinguere live market snapshot da metriche strutturali non same-timestamp

## Valutazione del giudizio finale
- `Business quality`: confermata `alta`
- `Necessita di esistenza del prodotto`: confermata `alta`
- `Necessita del token per il prodotto`: confermata `alta`
- `Token quality`: confermata `alta`
- `Token accrual verdict`: confermato `medio`
  - il token riceve valore soprattutto `indiretto`
  - non esistono buyback
  - la supply netta resta in aumento ma lentamente e in modo deterministico
- `Market setup`: confermato `favorevole`
  - profondita spot elevata
  - struttura derivati molto ampia
  - nessun unlock cliff o treasury overhang di protocollo
- `Regime eventi recente`: da leggere come `evento materiale e ancora aperto` piu che `transitorio`
- `Verdetto finale`: `fairly priced` confermato
  - la qualita del token e altissima
  - ma il mercato la riconosce gia in larga misura
  - il rialzo residuo dipende soprattutto da ulteriore monetization del premium e assorbimento del float, non da fee yield

## Sintesi finale
- Il report fondamentale su `Bitcoin / BTC` regge bene sui blocchi che contano davvero:
  - necessity of existence
  - token necessity
  - supply discipline
  - absence of buyback/treasury/unlock mechanics
  - corretto framing del bull case come `monetary premium`, non `cash flow`
- Le correzioni utili sono soprattutto tre:
  - pulire il `recent event log` dagli elementi appena fuori finestra `90d`
  - aggiungere almeno la disclosure `Strategy` del `2026-03-23`
  - usare `CoinGlass` come fonte derivati piu che come anchor spot
- Con queste correzioni, il giudizio finale non cambia:
  - `BTC` resta asset di qualita altissima
  - il setup di mercato resta costruttivo
  - il prezzo non appare chiaramente cheap sullo snapshot verificato
