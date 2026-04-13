# Verification Audit

## Data di verifica
- Protocollo / ticker verificato: `RaveDAO / RAVE`
- Report verificato: `output/ravedao-rave-2026-04-14-test/token-research-ravedao-rave-test.md`
- Prompt base di riferimento: `prompt/token-research-prompt.md`
- Data di verifica: `2026-04-14`
- Approccio:
  - verifica di claim strutturali, waterfall, token rights, supply, treasury, market structure ed eventi recenti usando docs ufficiali, filing MiCAR, CoinGecko come dashboard metodologicamente chiara, Coinbase come fonte primaria di availability spot ed Etherscan come contesto onchain

## Esito sintetico
- Esito generale: `confermato nel nucleo, con alcune correzioni e un aggiornamento importante sugli eventi recenti`
- Il cuore del report regge:
  - `RaveDAO` ha un business / event brand reale e non puramente cartaceo
  - `RAVE` non conferisce diritti economici su profitti, ricavi o dividendi
  - la narrativa `buyback & burn` resta non chiusa con rigore documentale
  - il token continua a dipendere piu da narrativa, venue quality, concentrazione del float e reflessivita che da tokenholder accrual dimostrato
  - il verdetto `sopravvalutato` resta il giudizio piu disciplinato sullo snapshot verificato
- Le correzioni principali che emergono dalla verifica sono:
  - la `Token Distribution Schedule` ufficiale va trattata come `internamente ambigua`, non solo come divergenza tra docs e dashboard
  - il blocco `recent events` del report fondamentale e gia parzialmente superato: il live di CoinGecko oggi evidenzia soprattutto `deployer-wallet / Bitget exit concerns`, `perpetuals volume spike` e `Hong Kong airdrop narrative`, non il solo lead `Binance Futures`
  - i numeri di market data e venue vanno letti come `range intraday`, non come snapshot unico autorevole, perche CoinGecko mostra variazioni molto forti anche nello stesso giorno

## Verifica del perimetro metodologico
- La scelta `full diligence` del report originale e `coerente`.
- Motivo:
  - i blocchi che contano per il fair-value work strutturale restano verificabili con rigore sufficiente:
    - business reale
    - diritti del token
    - quality del ponte business -> token
    - scala della valuation rispetto al business disclosed
    - concentrazione della supply
  - restano aperti buchi materiali su:
    - wallet treasury / buyback / burn
    - peso economico live dei token sinks
    - riconciliazione perfetta della supply release
    - derivatives microstructure
- Questi buchi impediscono `confidenza alta`, ma non forzano il report in `opacity-compressed`.
- Valutazione finale del perimetro:
  - `full diligence` corretto
  - `copertura dati parziale` corretta
  - `confidenza media` corretta

## Fonti usate per la verifica
- https://ravedao.com/
- https://ravedao.com/events
- https://ravedao.com/rave-for-light
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/impact-metrics
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics/token-distribution-schedule
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics/token-utilities
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics/usdrave-cross-chain-bridge
- https://ravedao.github.io/rave-xhtml/
- https://www.coingecko.com/en/coins/ravedao
- https://www.coinbase.com/advanced-trade/spot/RAVE-USD
- https://etherscan.io/token/0x17205fab260a7a6383a81452ce6315a39370db97

## Eventi recenti verificati
- `Evento confermato`
  - `2026-04-14`: `Coinbase Advanced Trade` mostra il pair spot `RAVE-USD`; quindi la disponibilita spot su Coinbase e confermata alla data di verifica.
  - `2026-04-14`: `CoinGecko` conferma price regime estremamente esplosivo:
    - prezzo `~$10.68`
    - `24h +89.0%`
    - `7d +4200.8%`
    - market cap `~$2.631B`
    - FDV `~$10.606B`
    - volume 24h `~$640.997M`
    - ATH `~$14.18` il `2026-04-13`
  - `2026-04-14`: `CoinGecko Markets` conferma venue spot ormai materiali e non marginali:
    - `Coinbase Exchange RAVE/USD` `~$141.7M` volume 24h, `22.11%`
    - `Gate RAVE/USDT` `~$120.8M`, `18.84%`
    - `Bitget RAVE/USDT` `~$76.7M`, `11.96%`
    - `DigiFinex RAVE/USDT` `~$72.2M`, `11.27%`
    - `Uniswap V4 (Ethereum) RAVE/USDT` con profondita `+2%/-2%` sopra `~$6.5M`
  - `2026-04-14`: `CoinGecko` conferma la forte asimmetria supply/float:
    - circulating `248,044,444`
    - vesting address `751,955,556`
    - total / max supply `1,000,000,000`

- `Allegation o claim non dimostrato`
  - `2026-04-14`, blocco `Recently Happened` di CoinGecko:
    - `RaveDAO Deployer Wallets Moved RAVE to Bitget Before Pump, Raising Exit Concerns`
    - testo mostrato da CoinGecko: wallet collegati al deployer avrebbero spostato `~18.58M RAVE` a `Bitget` `10 hours before a price surge`
    - questo e materialmente piu rilevante del vecchio lead `Binance Futures`, ma nella verifica di oggi non ho una prova primaria pulita e completa per chiuderlo come fatto definitivo
  - `2026-04-14`, blocco `Recently Happened` di CoinGecko:
    - `RAVE Ranks Third in Global Perpetuals Trading Volume`
    - claim secondario utile come segnale di leva, non chiuso con fonte primaria metodologicamente forte nel perimetro odierno
  - `2026-04-14`, blocco `Recently Happened` di CoinGecko:
    - `RaveDAO Airdrops RAVE Tokens to Hong Kong Consensus Attendees`
    - non ho trovato nel perimetro verificato una fonte primaria ufficiale sufficiente per fissare entita economica e materiali implicazioni di supply/marketing
  - causalita precisa del rally di aprile 2026:
    - non e chiusa
    - venue improvement, short squeeze, perp activity, social mania e possibili exchange flows possono aver contribuito insieme
  - buyback / burn come meccanica economicamente rilevante:
    - resta non dimostrato

- `Risposta del team / fonte primaria`
  - non ho trovato nel perimetro verificato una risposta ufficiale del team che chiuda in modo numerico:
    - buyback
    - burn
    - wallet di treasury
    - spiegazione del delta tra schedule e circulating
    - allegation sui trasferimenti verso Bitget
  - la fonte primaria piu forte per i diritti del token resta il filing MiCAR
  - la fonte primaria piu forte per la schedule resta la `Token Distribution Schedule`, ma la pagina resta ambigua nel wording

- `Market reaction osservata`
  - `CoinGecko` mostra un mercato in regime di euforia / reflessivita piena:
    - market cap `~$2.63B`
    - FDV `~$10.61B`
    - volume 24h `~$641M`
    - ATH `~$14.18`
  - `CoinGecko` mostra anche turnover e venue quality tali da rendere il token molto piu esprimibile a mercato rispetto a pochi giorni prima
  - l impatto osservato colpisce soprattutto:
    - `market structure`
    - `fiducia narrativa`
    - `pricing del token`
    - non il nucleo di `token rights`

- `Lettura 7d / 30d / 90d`
  - ultimi `7d`:
    - il fatto dominante e il rally verticale con market structure molto piu aggressiva e probabile leva elevata
  - ultimi `30d`:
    - passaggio da ATL `2026-03-12` a ATH `2026-04-13`, senza prova equivalente di miglioramento del token accrual
  - ultimi `90d`:
    - la disponibilita spot su `Coinbase` e l upgrade di venue quality sono gli sviluppi piu chiaramente confermati
    - non ho trovato in fonti primarie exploit, halt, outage, governance breakdown, team departure o enforcement regolatorio thesis-changing su RaveDAO

## Confermato
- `Descrizione del progetto`: confermata.
  - RaveDAO e meglio descritto come `event / entertainment brand tokenizzato` o `cultural coordination layer`, non come protocollo infrastrutturale classico.

- `Business reale`: confermato.
  - sito ufficiale, pagina eventi, whitepaper e MiCAR supportano eventi reali, sponsor, ticketing, membership e footprint internazionale.

- `Revenue business reale`: confermato.
  - il MiCAR dichiara `~$3M` di revenue cumulata `2024-2025 YTD`, con linee di ricavo coerenti con sponsorships, ticketing, VIP tables, F&B, collectibles e service fees.

- `No token sale / no equity fundraising / no debt`: confermato.
  - il MiCAR dice che il business e `fully bootstrapped` e che `no equity fundraising or token sale has taken place`.

- `Token rights limitati`: confermato.
  - il MiCAR esclude `ownership`, `equity rights`, `claims to profits, revenues, or dividends`.

- `Governance consultativa`: confermata.
  - il MiCAR dice che i processi community sono `advisory in nature` e non modificano i termini fondamentali del token.

- `Supply cap 1B`: confermato.

- `Issuer retained 200M`: confermato.

- `Circulating vs vesting imbalance`: confermato.
  - `CoinGecko` mostra `248,044,444` circulating e `751,955,556` nel vesting address.

- `Contrasto whitepaper vs MiCAR sul buyback`: confermato.
  - `Token Utilities` parla di `Buyback & Burn`
  - il MiCAR dichiara `Supply Adjustment Protocols: false` e `Token Value Protection Schemes: false`

- `Utility documentata del token`: confermata come documentazione di design.
  - `Token Utilities` conferma layer B2B/B2C/governance
  - il MiCAR conferma accesso a ticketing, participation, staking e governance come perimetro di utilita dichiarata
  - resta separato il tema `live usage verificato`

- `Bridge mechanics`: confermate.
  - il whitepaper dice che `$RAVE` e live su `Stargate Finance` fra `Ethereum`, `Base` e `BNB Chain`

- `Venue quality molto migliorata`: confermata.
  - `Coinbase`, `Gate`, `Bitget`, `Kraken`, `DigiFinex` e DEX con depth materiale rendono il setup molto piu liquido di una lettura da microcap isolata

- `Market setup ancora riflessivo`: confermato.
  - ampiezza del rally, turnover giornaliero e nowcast `CoinGecko Alpha` sostengono pienamente questa lettura

## Da correggere o aggiornare
- `Schedule ufficiale trattata come se fosse piu chiusa di quanto sia davvero`
  - nel report fondamentale la riga su `Ecosystem 31%` viene riportata come `remaining 15.97% with 12m cliff + 36m vesting`
  - nella pagina aperta live del whitepaper, il bullet di categoria mostra `remaining 15.97% with 36-month vesting`, mentre il paragrafo sopra dice che `the remaining tokens will follow a 12-month cliff and 36-month linear vesting schedule`
  - inoltre il motore di ricerca mostra lo snippet con `12-month cliff, 36-month vesting`
  - implicazione:
    - la fonte ufficiale va trattata come `internamente ambigua`
    - non basta dire `docs vs dashboard`; c e anche una tensione dentro la rappresentazione ufficiale della stessa docs

- `Recent event evidence log`
  - il report usa come lead secondario `Binance Futures catalyst`
  - nella verifica live del `2026-04-14`, CoinGecko evidenzia invece come headline recenti:
    - `deployer wallets -> Bitget`
    - `third-largest perpetuals volume`
    - `Hong Kong Consensus airdrop`
  - implicazione:
    - il blocco eventi recenti del fondamentale va considerato gia parzialmente datato nello stesso giorno
    - la verifica deve spostare l attenzione da `futures listing narrative` a `market structure / exchange flow / optics risk`

- `Dati live di mercato`
  - il report ha gia gestito bene la volatilita usando range
  - ma i valori precisi su volume share e ATH sono gia cambiati materialmente nel live `CoinGecko` della verifica
  - implicazione:
    - i numeri puntuali vanno letti come `snapshot intraday`, non come base di claims rigidi

## Parzialmente confermato, ma non chiuso con rigore pieno
- `Buyback & burn come meccanica economica rilevante`
  - confermato che il marketing lo promette
  - non confermato che esista una meccanica sistematica, quantificata e verificabile onchain

- `On-chain transparency del business`
  - il MiCAR sostiene una forte integrazione onchain e menziona treasury multisig e decisioni visibili via governance dashboards
  - ma nella verifica di oggi non ho trovato wallet pubblici o dashboard sufficienti per ricostruire davvero il waterfall economico

- `Utility live del token oltre la partecipazione`
  - docs e MiCAR documentano ticketing, payments, staking, loyalty, grants e governance
  - non ho pero prova primaria sufficiente per chiudere il peso economico live di questi sink

- `Metriche di scala`
  - `100k+ participants`, `50k+ NFT tickets`, `150M+ impressions`, `20% proceeds` sono presenti nelle docs ufficiali
  - restano pero principalmente `team-reported`

- `Supply release di breve`
  - la grande lettura `overhang elevato` e chiarissima
  - la lettura del breve resta invece non chiusa:
    - `CoinGecko` mostra `24.80%` circulating
    - la schedule ufficiale parla di `23.03%` al TGE
    - il wording dell `Ecosystem` bucket resta ambiguo

- `Allegation Bitget / deployer-wallet`
  - e un segnale di rischio oggi troppo rilevante per ignorarlo
  - ma non e ancora chiuso con prova primaria sufficiente nel perimetro di questa verifica

## Source reconciliation residua
- `Schedule ufficiale interna`
  - conflitto:
    - summary ufficiale: `remaining tokens` con `12-month cliff and 36-month linear vesting`
    - bullet category `Ecosystem`: `remaining 15.97% with 36-month vesting`
    - search snippet della stessa pagina: `remaining 15.97% with 12-month cliff, 36-month vesting`
  - implicazione analitica:
    - la supply story di breve non va trattata come chiusa nemmeno sul piano documentale primario

- `Docs vs dashboard su circulating`
  - conflitto:
    - `23.03%` teorico al TGE
    - `248,044,444` circulating osservata su `CoinGecko`
  - implicazione analitica:
    - abbassa la confidenza sulla narrativa di scarsita limpida

- `Vesting address vs issuer retained`
  - conflitto:
    - `751.955M` nel vesting address
    - `200M` retained dell issuer
  - implicazione analitica:
    - non vanno sommati automaticamente
    - confermano concentrazione, non mappa precisa

- `Market data intraday`
  - conflitto:
    - il report fondamentale usava un range `~$2.2B-2.6B`
    - la verifica live spinge verso il lato alto del range
  - implicazione analitica:
    - nessun cambio del verdetto, ma serve trattare tutti i prezzi del `2026-04-14` come snapshot ad alta volatilita

## Valutazione del giudizio finale
- `Business quality: media`
  - giudizio confermato.
  - La verifica conferma che il business esiste davvero ed e piu sostanziale della media dei token puramente narrativi, ma resta piccolo, team-reported su molte metriche e execution-heavy.

- `Necessita di esistenza del prodotto: media-bassa`
  - giudizio confermato.
  - Il vantaggio concreto esiste soprattutto come brand / sponsor coordination / crypto-native distribution, molto meno come superiorita prodotto inevitabile per l utente finale.

- `Necessita del token per il prodotto: bassa`
  - giudizio confermato.
  - Le utilita documentate esistono, ma il business puo ancora essere immaginato in forma quasi intatta anche senza token liquido.

- `Token quality: bassa`
  - giudizio confermato e rafforzato.
  - Il MiCAR e molto netto su assenza di diritti economici forti e governance consultativa.

- `Token accrual verdict: debole`
  - giudizio confermato.
  - Nulla nella verifica chiude un ponte economico robusto fra revenue business e holder esterni.

- `Market setup: fragile`
  - giudizio confermato.
  - Va letto come `fragile ma molto piu liquido`, non come `illiquido`.
  - La liquidita migliore non riduce la fragilita fondamentale; amplia la scala del movimento.

- `Regime eventi recente: evento ancora aperto`
  - giudizio confermato ma con aggiornamento.
  - Oggi il regime recente non e solo `listing / hype`: include anche `allegation di exchange flows insider-linked`, `perpetuals overheating` e `airdrop narrative`.

- `Verdict: sopravvalutato`
  - resta il giudizio piu rigoroso sullo snapshot verificato.
  - La verifica non smonta la tesi; semmai la irrigidisce:
    - venue quality migliore
    - business reale
    - ma token rights deboli
    - e market setup ancora piu chiaramente dominato da reflessivita e leverage-driven optics

- `Confidenza del giudizio: media`
  - giudizio corretto.
  - Non va alzata a `alta` perche restano aperti:
    - vesting interpretation
    - live token usage
    - treasury transparency
    - exchange-flow allegations

## Sintesi finale
- Il report fondamentale `2026-04-14` su `RaveDAO / RAVE` regge nel suo asse principale:
  - `business reale`
  - `token rights deboli`
  - `buyback narrative non chiusa`
  - `valuation troppo aggressiva rispetto all accrual`

- I punti piu forti confermati dalla verifica sono:
  - il filing MiCAR sul lato rights / governance / supply
  - la conferma di venue spot piu solide, in particolare `Coinbase`
  - la forte concentrazione della supply e il mismatch tra business scale e prezzo del token

- Le correzioni piu importanti da portarsi dietro sono tre:
  - trattare la `Token Distribution Schedule` come `fonte ufficiale internamente ambigua`, non come schedule pienamente chiusa
  - aggiornare il blocco `recent events` per includere le attuali allegation su `Bitget / deployer wallets` e il segnale di overheating sui perp
  - leggere tutti i market data del `2026-04-14` come `range intraday`, non come singolo snapshot definitivo

- Verdetto finale della verifica:
  - `confermato nel nucleo, con aggiornamenti materiali sul source reconciliation e sul recent-event risk`
  - il giudizio `sopravvalutato` con `token quality bassa`, `token accrual debole` e `market setup fragile ma liquido` resta il piu disciplinato anche dopo la verifica
