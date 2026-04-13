# Test Prompt: `token-research-prompt.md`

## Input usato
- `[NOME/TICKER]`: `Hyperliquid / HYPE`
- Data snapshot principale: `2026-04-10`
- Obiettivo del test: raccogliere il materiale minimo utile all'analisi e poi produrre l'output del prompt in forma già compilata

## Materiale minimo per l'analisi

### Fonti principali
- Hyperliquid Docs, overview prodotto e architettura: https://hyperliquid.gitbook.io/hyperliquid-docs
- Hyperliquid Docs, fees / staking / HyperEVM / builder codes / aligned quote assets:
  - https://hyperliquid.gitbook.io/hyperliquid-docs/trading/fees
  - https://hyperliquid.gitbook.io/hyperliquid-docs/hypercore/staking
  - https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/hyperevm
  - https://hyperliquid.gitbook.io/hyperliquid-docs/trading/builder-codes
  - https://hyperliquid.gitbook.io/hyperliquid-docs/hypercore/aligned-quote-assets
- DefiLlama, protocol page / methodology / income statement:
  - https://defillama.com/protocol/hyperliquid
- CoinGecko, price / supply / tokenomics page:
  - https://www.coingecko.com/en/coins/hyperliquid
- Tokenomist, unlock analytics e nota sulla divergenza tra unlock teorico e claimed unlock:
  - https://tokenomist.ai/hyperliquid
  - https://tokenomist.ai/research/hype-tokenomics-330k-or-9-9m-hype-unlocks
  - https://tokenomist.ai/research/weekly-unlock-digest-apr-6-12-2026-hype-committed-claim-strategy
- Comparatori:
  - dYdX: https://defillama.com/protocol/dydx
  - Jupiter: https://defillama.com/protocol/fees/jupiter
  - GMX: https://defillama.com/protocol/fees/gmx

### Snapshot numerico essenziale
- Prezzo HYPE: `~$42.10`
- Market cap: `~$10.0B`
- Outstanding token value: `~$24.0B`
- FDV: `~$40.4B`
- Circulating supply: `238.39M`
- Outstanding supply: `570.39M`
- Total supply: `962.27M`
- Max supply: `1.00B`
- HYPE burned via Assistance Fund: `37.56M`
- Fees annualizzate: `~$766.9M`
- Revenue / holders revenue annualizzate: `~$681.2M`
- Fees 30d: `~$62.9M`
- Revenue 30d: `~$55.8M`
- Perp volume 30d: `~$196.4B`
- Spot DEX volume 30d: `~$3.6B`
- Open interest: `~$7.54B`
- Token volume 24h: `~$349M-$353M`
- Prossimo unlock teorico indicato da CoinGecko/Tokenomist: `9.92M HYPE il 6 maggio 2026`
- Ultimo dato pubblico utile sui claim effettivi: ad aprile 2026 il team aveva comunicato un claim di `~330k HYPE`, molto sotto il ceiling teorico di `9.92M`

### Punti che restano parzialmente opachi
- Split live preciso tra Assistance Fund, HLP, deployers e builder fees per singolo giorno
- Stato on-chain definitivo del claim di aprile 2026 nelle fonti aperte consultate
- Holder concentration dettagliata, basis, borrow cost, short availability e funding sul token HYPE
- Distinzione perfetta tra supply locked ma mintata, supply pianificata ma non rilasciata, e supply economicamente non destinata al mercato

---

# Output del prompt

Research status
- qualità delle fonti: `alta-media`
- copertura dati: `parziale`
- principali buchi informativi: split fee live per categoria, market structure derivata su HYPE, conferma on-chain finale del claim di aprile 2026
- rischio principale di errore analitico: trattare la supply teorica come supply che entrerà davvero sul mercato con quel ritmo
- confidenza preliminare: `media`

## 1. TL;DR iniziale
Fatti verificabili:
- Hyperliquid è un L1 costruito intorno a perps e spot onchain con order book nativo; a snapshot `2026-04-10` fa `~$196.4B` di perp volume 30d, `~$62.9M` di fees 30d e `~$55.8M` di revenue 30d.
- HYPE non è solo un governance token: è gas del HyperEVM, asset di staking e soprattutto destinatario di buyback automatizzati via Assistance Fund che, secondo la documentazione ufficiale, finiscono in burn.
- La business quality è alta. La token quality è reale, non cosmetica. Ma la supply liquida è solo una frazione della supply economica totale.

Inferenze ragionevoli:
- Il mercato tende a fare due errori opposti: alcuni sottostimano la qualità del value accrual perché guardano solo a “DEX token”; altri sopravvalutano la scarsità perché guardano i buyback e ignorano outstanding supply e discrezionalità dei claim.
- Il vero edge non è “Hyperliquid è forte”, cosa ovvia. Il vero edge è capire se la discipline sui claim resta molto sotto il vesting teorico.

Speculazioni:
- Se il regime attuale regge, HYPE può ancora fare bene.
- Se il ritmo dei claim accelera o il business perde momentum, il token smette rapidamente di sembrare economico.

Giudizio preliminare:
- protocollo eccellente, token investibile, ma non chiaramente asimmetrico ai prezzi attuali; lo leggo più come `fairly priced` che come regalo evidente.

## 2. Che cosa fa davvero il protocollo
Fatti verificabili:
- Hyperliquid è una blockchain L1 con due componenti, `HyperCore` e `HyperEVM`; l’order book di perps e spot è onchain e la chain dichiara supporto a `200k orders/sec`.
- Il prodotto principale resta l’exchange derivati/spot. Il resto dell’ecosistema oggi è ancora opzionalità attorno a quel core.
- HYPE è usato per gas su HyperEVM, per staking e per fee discounts nel trading.

Inferenze ragionevoli:
- Il problema reale che risolve è offrire execution ad alte performance con trasparenza onchain e distribuzione permissionless verso builder terzi.
- La forma onchain ha senso perché trasparenza di ordini, liquidazioni, funding e composability sono parte del prodotto. Non è solo packaging.
- Se togli il token, il protocollo come venue di trading continua a funzionare quasi uguale per l’utente trader medio, che usa collateral in USDC. Quello che peggiora è il layer di sicurezza, burn/accrual, staking e coordinamento economico del network.

Speculazioni:
- Se HyperEVM e app esterne diventano più importanti del solo exchange, la necessità economica del token aumenta. Oggi questa optionality esiste, ma non è ancora il motore principale.

## 3. Business quality: qualità reale del protocollo
Fatti verificabili:
- Snapshot DefiLlama `2026-04-10`: `Perp volume 30d ~$196.4B`, `DEX volume 30d ~$3.6B`, `Open Interest ~$7.54B`, `Fees annualized ~$766.9M`, `Revenue annualized ~$681.2M`.
- Income statement DefiLlama: `Q1 2026 gross protocol revenue ~$214.95M`, dopo `Q4 2025 ~$286.53M` e `Q3 2025 ~$354.94M`.
- Builder code fees in `Q1 2026`: `~$17.42M`.
- Hyperliquid Docs riportano inoltre `>$45M` di revenue generata da team terzi tramite builder codes.

Inferenze ragionevoli:
- La crescita non è cosmetica. Qui c’è uso pagante reale, non TVL ornamentale.
- Il business è altamente scalabile ma ancora molto concentrato: i perps dominano nettamente, mentre spot e applicazioni satellite sono piccole rispetto al core.
- La stabilità della crescita non è perfetta: i numeri restano enormi, ma rispetto ai trimestri di picco si vede già la sensibilità al market regime.

Speculazioni:
- Se Hyperliquid riesce a trasformare il vantaggio in execution in un vantaggio più ampio di “liquidity layer”, la seconda gamba di crescita può arrivare da builder, stablecoin aligned e HyperEVM.

## 4. Unit economics e qualità dei ricavi
Fatti verificabili:
- DefiLlama `Q1 2026`: `Gross Protocol Revenue ~$214.95M`, `Cost of Revenue ~$22.69M`, `Gross Profit ~$192.25M`.
- DefiLlama methodology modella `1%` della trading revenue verso `HLP` e `99%` delle fee di perps/spot verso `Assistance Fund` per comprare HYPE, escludendo builders fees e unit protocol fees.
- Hyperliquid Docs dicono che le fee vanno alla community: `HLP`, `assistance fund`, `deployers`; i deployers spot/HIP-3 possono trattenere fino al `50%` delle trading fees dei mercati che hanno deployato.

Inferenze ragionevoli:
- La top-line è di qualità alta: utenti pagano per eseguire trading, non è emission-driven.
- La revenue però è ciclica e regime-sensitive. Non è un SaaS lineare: se volatilità, partecipazione retail e speculative flow scendono, la top-line scende.
- Il grosso del valore economico arriva davvero fino al token, ma non il `100%` delle fees lorde. Parte resta a builders, deployers, HLP e altre voci del fee stack.

Speculazioni:
- L’attuale run-rate può essere troppo alto se normalizzato su regime meno favorevole.

## 5. Token: come cattura valore davvero
Fatti verificabili:
- Docs ufficiali: l’`Assistance Fund` usa l’indirizzo di sistema `0xfefe...fefe`, converte trading fees in HYPE “in fully automated manner as part of the L1 execution” e “HYPE in the assistance fund is burned, removing the tokens permanently from the circulating and total supply”.
- Docs ufficiali: HYPE è gas token del HyperEVM; su HyperEVM vengono burnate sia base fees sia priority fees.
- Docs ufficiali: HYPE dà fee discounts nel trading tramite staking tiers da `5%` a `40%`.

Inferenze ragionevoli:
- Il token ha value accrual reale e diretto nel senso economico del prezzo: c’è domanda ricorrente automatizzata e c’è burn permanente.
- Non ha però un diritto cash-flow tipo equity. Il valore arriva via buyback/burn e utility di network, non via distribuzione in stablecoin.
- La necessità d’uso del token per il prodotto principale è limitata: per fare trading core, HYPE non è indispensabile come collateral.

Speculazioni:
- Se il burn da EVM fees e le future fee sinks su HyperEVM crescono, il token passa da “exchange token molto buono” a “network asset più completo”.

Claim audit:
- Claim: `il token cattura revenue`.
- Evidenza primaria: docs ufficiali Assistance Fund + burn; docs HyperEVM fee burn.
- Cosa dimostra davvero: parte molto rilevante delle fee si trasforma in domanda automatica di HYPE e poi burn.
- Cosa non dimostra: non dimostra che ogni dollaro di crescita del protocollo si traduca linearmente in upside del token.
- Giudizio finale: `supportata`.

- Claim: `i buyback mangiano l’offerta`.
- Evidenza primaria: CoinGecko stima `37.56M HYPE` già burnati nell’Assistance Fund.
- Cosa dimostra davvero: la total supply è stata ridotta in modo permanente.
- Cosa non dimostra: non dimostra che la pressure netta futura resterà deflattiva contro claim, unlock e future emissions.
- Giudizio finale: `parzialmente supportata`.

## 6. Supply, unlock e dilution analysis
Fatti verificabili:
- CoinGecko `2026-04-10`: `circulating 238.39M`, `outstanding 570.39M`, `total supply 962.27M`, `max supply 1.00B`.
- Breakdown disponibile: `HyperLabs 241.50M`, `Hyper Foundation 60.76M`, `Future Emissions 418.63M`, `Community Grant 3.00M`.
- Assistance Fund burned: `37.56M HYPE`.
- CoinGecko/Tokenomist indicano il prossimo unlock teorico il `6 maggio 2026` per `9.92M HYPE`.
- Tokenomist ha mostrato che il claim annunciato per aprile 2026 era `~330k HYPE`, contro un ceiling teorico di `9.92M`; i claim storici osservati erano molto inferiori allo schedule teorico.

Inferenze ragionevoli:
- Il rischio unlock di breve non va letto in modo meccanico dal whitepaper schedule. Il mercato che prezza `9.92M` ogni mese come supply certa rischia di sovrastimare la pressione imminente.
- Il rischio dilution di medio-lungo resta comunque serio: la circolante è bassa rispetto a outstanding/total, e gran parte del potenziale overhang è ancora fuori mercato.
- La qualità della circolante è migliore di molti token post-TGE perché non c’è allocazione VC esplicita, ma resta una circolante piccola rispetto alla supply economicamente controllata dal sistema/team/foundation.

Speculazioni:
- Se i claim continuano a restare nell’ordine di poche centinaia di migliaia al mese, l’overhang percepito è troppo alto rispetto a quello reale.
- Se il team smette di gestire la supply in modo conservativo, il rerating si inverte in fretta.

Net supply change
- Burn 30d implicito al run-rate attuale: `~$55.84M / $42.10 ~= 1.33M HYPE` al mese.
- Questo run-rate di burn supera il claim annunciato di aprile `~330k HYPE`, ma resta molto sotto lo schedule teorico di `9.92M HYPE`.
- Conclusione: `sul realized supply path recente, buyback > claim`; `sul paper schedule pieno, buyback < unlock`.

## 7. Treasury e capital allocation
Fatti verificabili:
- L’indirizzo `Hyper Foundation` indicato da CoinGecko contiene `~60.76M HYPE`; al prezzo spot vale circa `~$2.56B`.
- Esiste inoltre un address `Future Emissions` da `~418.63M HYPE`, economicamente molto più grande della foundation treasury.

Inferenze ragionevoli:
- Il progetto non ha rischio runway. Ha rischio di capital allocation.
- Una treasury così ampia protegge l’operatività ma rappresenta anche un potenziale strumento di dilution indiretta.
- Il fatto che la treasury sia quasi interamente token-denominated lega la governance del capitale al prezzo del token stesso.

Speculazioni:
- Se il capitale viene usato con disciplina per builder grants, aligned stables e infra, può rafforzare il moat.
- Se il capitale viene usato per distribuzioni aggressive o iniziative poco produttive, il token ne paga il costo.

## 8. Posizionamento competitivo
Fatti verificabili:
- `dYdX`: `30d perp volume ~$4.85B`, `30d revenue ~$274.7k`, `market cap ~$71.8M`.
- `Jupiter`: `30d fees ~$40.5M`, `30d holders revenue ~$4.82M`, `market cap ~$581M`.
- `GMX`: `30d holders revenue ~$0.96M`, `market cap ~$63M`.
- HYPE: `30d revenue ~$55.84M`, `market cap ~$10.0B`.

Inferenze ragionevoli:
- Hyperliquid non compete più davvero alla pari con i vecchi perp DEX minori sul piano della scala economica.
- Il confronto corretto è: da un lato i perp DEX onchain, dall’altro la qualità UX/liquidity dei CEX. È qui che si gioca il premio di valutazione.
- Rispetto a JUP e GMX, HYPE quota più caro su holders revenue, ma con una qualità di business e una presa sul flow nettamente superiori.

Speculazioni:
- Il competitor più pericoloso non è il fork onchain piccolo; è una venue che combini distribuzione, velocità e liquidità comparabili con listing depth maggiore.

## 9. Moat, rischio copia e dipendenze esterne
Fatti verificabili:
- L’architettura è proprietaria ma la documentazione e il design del prodotto rendono il format concettualmente copiabile.
- Il business dipende in modo forte da una singola chain, da market structure trading-led e dalla capacità di mantenere la liquidità.

Inferenze ragionevoli:
- Il moat vero non è il codice. È `liquidità + brand + execution + distribuzione builder + abitudine del trader`.
- Il network effect esiste, ma è più vicino a un liquidity network effect che a un moat impossibile da replicare.
- È un business robusto finché resta top venue. Se perde leadership, la compressione può essere rapida.

Speculazioni:
- L’eventuale spostamento del moat da “exchange forte” a “financial infra layer” sarebbe un upgrade importante del profilo.

## 10. Market structure del token
Fatti verificabili:
- CoinGecko: HYPE scambia su `64 exchanges` e `84 markets`.
- CoinGecko: token volume 24h `~$349M`.
- DefiLlama: token volume 24h `~$352.8M`, di cui `~58.8%` su DEX.
- Revenue/holders revenue 24h: `~$2.25M`.

Inferenze ragionevoli:
- La liquidità secondaria è reale. Non sembra un token sostenuto solo da float microscopico e venue deboli.
- I buyback giornalieri hanno impatto economico continuo ma, contro `~$350M` di token volume 24h, non sono abbastanza grandi da imporre da soli il prezzo giorno per giorno.
- L’impatto dei buyback è molto più forte sulla traiettoria di supply che sulla market structure intraday.

Speculazioni:
- Senza dati sufficienti su borrow, basis, short availability e concentrazione wallet aggiornata, non è rigoroso chiamarlo token “squeezabile” o pienamente robusto a distribuzioni insider.

## 11. Holder base e allineamento
Fatti verificabili:
- Le fonti di distribuzione pubbliche riportano `nessuna allocazione a private investors, CEX o market makers`.
- Una porzione enorme della supply non circolante resta in address riconducibili a `HyperLabs`, `Hyper Foundation` e `Future Emissions`.

Inferenze ragionevoli:
- La holder base iniziale è più pulita di molti token comparabili. Questo è un plus reale.
- L’allineamento resta comunque misto: community forte nella genesis distribution, ma controllo economico ancora concentrato fuori dalla circolante.

Speculazioni:
- Se nel tempo la quota realmente community-owned sale più rapidamente delle emissioni, il profilo di allineamento migliora molto.

## 12. Catalizzatori
Fatti verificabili:
- `Già noti`: burn continuativi via Assistance Fund; updates mensili sui claim; espansione builder ecosystem; crescita di HyperEVM.
- `Probabili`: più attività su aligned quote assets/stablecoins; maggiore utilizzo del token come gas e staking asset.
- `Opzionali`: nuovi flussi fee-linked da applicazioni buildate sopra Hyperliquid.
- `Speculativi`: narrative rotation, ETF-style products, listing-driven repricing.

Inferenze ragionevoli:
- I catalizzatori che contano davvero sono due: `business growth` e `continued supply restraint`.
- Listing e narrative aiutano il prezzo, ma non sono il cuore del mispricing.

Speculazioni:
- Se un aligned stable significativo si materializza, la requirement di `1M HYPE staked` e del `50%` di reserve income verso il protocollo sarebbe un catalizzatore qualitativo interessante.

## 13. Bull case
Fatti verificabili:
- Il token oggi tratta circa `14.7x` holders revenue annualizzata su market cap corrente.

Inferenze ragionevoli:
- Bull case realistico:
  - milestone: mantenere leadership perps, tenere i claim molto sotto il ceiling teorico, far crescere HyperEVM senza perdere execution quality
  - metrica chiave: holders revenue verso `~$850M-$900M` annualizzata
  - rerating plausibile: `18x-20x` holders revenue
  - market cap sensata: `~$15B-$18B`
  - driver del rialzo: più crescita del business che narrativa

- Bull case forte:
  - milestone: maggiore monetizzazione builder/EVM, ulteriori fee sinks, supply discipline confermata
  - holders revenue: `~$1.1B-$1.2B`
  - multiplo: `~20x-22x`
  - market cap: `~$22B-$26B`
  - driver del rialzo: mix di business growth e multiple expansion

- Bull case estremo:
  - milestone: Hyperliquid si consolida come layer dominante del trading onchain e la market perception inizia a trattarlo come infra winner
  - market cap: `~$30B+`
  - driver del rialzo: multiple expansion molto più che mera meccanica buyback

Speculazioni:
- Lo scenario estremo esiste, ma non è il base case a `~$10B` di market cap.

## 14. Bear case
Fatti verificabili:
- Il business dipende molto dai volumi di trading; i perps sono il cuore della macchina economica.
- La circolante è piccola rispetto a outstanding/total supply.

Inferenze ragionevoli:
- Le cose che rompono la tesi:
  - normalizzazione forte dei volumi e della volatilità
  - problema tecnico/regolatorio sulla venue o sui listing sintetici
  - aumento materiale dei claim rispetto al pattern recente
  - scenario in cui il protocollo resta forte ma il token derata su outstanding/FDV anziché su circulating mcap

Speculazioni:
- Il rischio più subdolo è proprio questo: business ottimo, token mediocre perché il mercato smette di premiare la supply discipline come credibile e torna a prezzare l’overhang pieno.

## 15. Valuation thinking
Fatti verificabili:
- Market cap: `~$10.0B`
- Outstanding token value: `~$24.0B`
- FDV: `~$40.4B`
- Holders revenue annualizzata: `~$681.2M`
- Fees annualizzate: `~$766.9M`
- Multipli impliciti:
  - `mcap / holders revenue ~= 14.7x`
  - `mcap / fees ~= 13.1x`
  - `outstanding value / holders revenue ~= 35.2x`
  - `FDV / holders revenue ~= 59.3x`

Inferenze ragionevoli:
- Su circulating market cap il token non è cheap, ma nemmeno delirante per un leader con buyback/burn hard-coded.
- Su outstanding e soprattutto su FDV il token è caro. La differenza tra questi frame è la vera frattura dell’analisi.
- Rispetto ai comparabili:
  - più caro di JUP e GMX su holders revenue
  - più economico di dYdX su holders revenue
  - con qualità di business superiore a tutti i comparabili onchain osservati

Speculazioni:
- Se il mercato continua a trattarlo con logica da “realized circulating asset” invece che da “eventuale FDV asset”, il prezzo può ancora reggere o salire.

## 16. Price map e scenario map
Fatti verificabili:
- Ritorno all’ATH `($59.30)`: market cap `~$14.1B`.
- Rerating a `20x` holders revenue run-rate attuale: market cap `~$13.6B`, prezzo implicito `~$57.2`.
- Derating a `10x` holders revenue run-rate attuale: market cap `~$6.8B`, prezzo implicito `~$28.6`.
- Scenario “business +30%, multiplo 10x”: market cap `~$8.9B`, prezzo implicito `~$37.2`.
- Scenario “pump solo narrativa, business invariato, multiplo 20x”: market cap `~$13.6B`.

Inferenze ragionevoli:
- Il token non ha bisogno di narrativa estrema per tornare vicino all’ATH: basta un rerating moderato o un po’ di crescita con supply discipline credibile.
- Allo stesso tempo, è facile costruire uno scenario in cui il business continua a performare ma il token resta piatto o scende per compressione multipli.

Speculazioni:
- La parte più fragile del bull case è il multiplo, non il business.

## 17. Mispricing test
Fatti verificabili:
- Il mercato vede un token con buyback/burn reale ma anche con grande overhang potenziale.

Inferenze ragionevoli:
- Cosa sta sottovalutando il mercato:
  - la differenza tra `projected unlock` e `actual/committed claim`
  - la qualità relativamente rara di un burn meccanico e non puramente narrativo
- Cosa sta sopravvalutando il mercato:
  - la scarsità percepita se si guarda solo alla circulating supply
  - l’idea che buyback = supply problem risolto
- Variabile più importante ignorata:
  - `realized net supply change`, non il vesting teorico
- Vero edge dell’analisi:
  - leggere HYPE come token con business quality alta ma con valuation che cambia molto a seconda che si usi `market cap`, `outstanding value` o `FDV`
- Cosa rischio di capire male io:
  - assumere che la disciplina sui claim sia strutturale e non discrezionale

### Token accrual verdict
- Il token riceve valore economico diretto, indiretto o quasi nullo?
  - `Diretto sul prezzo via buyback/burn; non diretto come cash distribution.`
- I buyback sono abbastanza grandi da contare sul market cap attuale?
  - `Sì sul market cap circolante: yield implicita ~6.8% annualizzata. Molto meno impressionante su outstanding/FDV.`
- I buyback superano o no la pressione da unlock/emissioni?
  - `Superano i claim recenti osservati/annunciati; non superano lo schedule teorico pieno.`
- I token riacquistati spariscono davvero o possono tornare sul mercato?
  - `Secondo docs ufficiali, l’HYPE dell’Assistance Fund è burnato e rimosso da circulating e total supply.`
- Il bull case dipende da business growth, da buyback mechanics, o da semplice narrativa di scarsità?
  - `Principalmente da business growth + supply discipline. La narrativa di scarsità da sola non basta.`

## 18. Source reconciliation
Divergenza rilevante 1
- metrica o dato: `fee waterfall`
- fonti in conflitto: `Hyperliquid Docs` vs `DefiLlama methodology`
- differenza di definizione o perimetro: i docs dicono che le fee vanno a `HLP + Assistance Fund + deployers`; DefiLlama esplicita un modello `1% HLP / 99% Assistance Fund` per perps e spot protocol fees, escludendo builders e unit fees
- possibile motivo della divergenza: docs ufficiali descrittivi, DefiLlama normalizza per contabilità economica
- implicazione analitica: il senso del waterfall è chiaro; il live split preciso per categoria può variare e non va trattato come dato perfetto onchain senza ulteriore verifica

Divergenza rilevante 2
- metrica o dato: `unlock mensile`
- fonti in conflitto: `whitepaper schedule / calendari standard` vs `Tokenomist announced claim`
- differenza di definizione o perimetro: `9.92M` è ceiling teorico; `~330k` ad aprile 2026 era il claim comunicato
- possibile motivo della divergenza: HYPE usa una gestione discrezionale del claim, non una meccanica lineare osservabile solo da vesting math
- implicazione analitica: l’analisi della supply senza distinzione tra projected e claimed è incompleta

Divergenza rilevante 3
- metrica o dato: `TVL`
- fonti in conflitto: `CoinGecko ~$5.35B` vs `DefiLlama ~$4.95B`
- differenza di definizione o perimetro: differenze di crawl time e di perimetro metodologico
- possibile motivo della divergenza: timing e classificazione degli asset
- implicazione analitica: qui conta poco; per Hyperliquid le metriche decisive sono volumi, OI e fee generation più che TVL

## 19. Checklist finale di investimento
3 motivi forti per essere bullish
- Business quality nettamente sopra la media del settore.
- Token accrual reale via buyback/burn hard-coded, non solo storytelling.
- Near-term realized dilution finora molto più contenuta del vesting teorico.

3 motivi forti per essere cauti
- Circulating supply molto più bassa di outstanding/total supply.
- Il core business è fortemente ciclico e dipende dai volumi.
- La disciplina sui claim sembra positiva ma resta una variabile da monitorare, non una legge di natura.

3 segnali che confermerebbero la tesi
- Claim mensili che restano molto sotto `9.92M`.
- Holders revenue che tiene `>$50M` su base 30d.
- Crescita di HyperEVM / builder monetization senza erosione dei volumi core.

3 segnali che invaliderebbero la tesi
- Accelerazione materiale dei claim o release dalla treasury.
- Discesa strutturale di volumi e OI con compressione dei fee run-rate.
- Evento tecnico/regolatorio che colpisce la venue o la credibilità del burn/value accrual.

3 metriche da monitorare nei prossimi 90 giorni
- `Claimed unlock` mensile vs `projected unlock`.
- `Holders revenue 30d` / `token buyback 30d`.
- `Perp volume 30d` e `open interest`.

## 20. Conclusione netta
- business quality: `alta`
- token quality: `alta`
- market setup: `favorevole`
- verdict: `fairly priced`
- confidenza del giudizio: `media`
- orizzonte temporale implicito: `medio`
- motivo principale del giudizio: `HYPE ha un business eccellente e un meccanismo di accrual raro e reale, ma il mercato già gli riconosce un premio importante. Il vero upside non sta nel “buyback meme”, ma nel fatto che i claim reali restino molto sotto il vesting teorico mentre il business continua a produrre fee elevate. Se quella disciplina venisse meno, il token smetterebbe rapidamente di sembrare economico.`
