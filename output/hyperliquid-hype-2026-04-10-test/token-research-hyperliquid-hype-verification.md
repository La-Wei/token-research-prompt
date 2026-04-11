# Verification Audit: `token-research-hyperliquid-hype-test.md`

Data di verifica: `2026-04-10`

## Esito sintetico
- Struttura analitica: `solida`
- Claim strutturali sul protocollo/token: `in gran parte confermati`
- Numeri live di mercato e protocol metrics: `confermati come snapshot del momento in cui ho scritto, ma non più tutti aggiornati`
- Correzione più importante: `builder codes >$65M`, non più `>$45M`
- Correzione più importante sul giudizio: `market setup` meglio `neutro` che `favorevole`, perché i dati di market structure restano incompleti

## Fonti usate per la verifica
- Hyperliquid Docs:
  - https://hyperliquid.gitbook.io/hyperliquid-docs/trading/fees
  - https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/hyperevm
  - https://hyperliquid.gitbook.io/hyperliquid-docs/about-hyperliquid/hyperliquid-101-for-non-crypto-audiences
  - https://hyperliquid.gitbook.io/hyperliquid-docs/hypercore/aligned-quote-assets
- Hyper Foundation:
  - https://hypefoundation.io/
- CoinGecko:
  - https://www.coingecko.com/en/coins/hyperliquid
  - https://www.coingecko.com/en/coins/jupiter
  - https://www.coingecko.com/en/coins/gmx
  - https://www.coingecko.com/en/coins/dydx-chain
- DefiLlama:
  - https://defillama.com/protocol/hyperliquid
  - https://defillama.com/protocol/dydx
  - https://defillama.com/protocol/fees/jupiter
  - https://defillama.com/protocol/fees/gmx
- Tokenomist:
  - https://tokenomist.ai/hyperliquid
  - https://tokenomist.ai/hyperliquid/supply-analytics
  - https://tokenomist.ai/research/hype-tokenomics-330k-or-9-9m-hype-unlocks
  - https://tokenomist.ai/research/weekly-unlock-digest-apr-6-12-2026-hype-committed-claim-strategy

## Confermato
- `Assistance Fund`: i docs ufficiali confermano che usa l’indirizzo di sistema `0xfefe...fefe`, converte trading fees in HYPE in modo automatico e che l’HYPE nell’Assistance Fund viene burnato, rimuovendolo da circulating e total supply.
- `HyperEVM`: i docs ufficiali confermano che HYPE è il gas token e che su HyperEVM vengono burnate sia base fees sia priority fees.
- `Staking fee discounts`: confermati i tier `5% / 10% / 15% / 20% / 30% / 40%`.
- `No investors / no paid market makers / no VCs`: supportato da Hyper Foundation home e dai docs aggiornati.
- `Supply structure`: CoinGecko conferma `238,385,315` circulating, `570,394,028` outstanding, `962,274,028` total supply, `1,000,000,000` max supply e `37,561,181` HYPE burnati via Assistance Fund.
- `Unlock framework`: CoinGecko/Tokenomist confermano il prossimo unlock teorico di `9.92M HYPE` il `6 maggio 2026`.
- `Claim vs projected unlock`: Tokenomist conferma per aprile 2026 un announced claim di `~330k HYPE` contro un projected unlock di `9,916,666 HYPE`.
- `No private investor overhang` come idea generale: supportata meglio del normale per un token crypto, anche se resta comunque forte concentrazione fuori dalla circolante.
- `Aritmetica interna del file`: multipli, burn yield implicito e scenario map erano coerenti con i numeri di snapshot usati nel file originale.

## Da correggere o aggiornare

### 1. Builder codes revenue
- Nel file ho scritto `>$45M`.
- I docs aggiornati mostrano `>$65M`.
- Stato: `da correggere`.

### 2. Numeri live di prezzo / market cap
- Il file originale usava uno snapshot CoinGecko coerente con `~$42.10` e `~$10.0B` market cap.
- Un ricontrollo live oggi mostra invece circa `~$39.81` e `~$9.48B`.
- Stato: `non falsi nello snapshot originale, ma non più aggiornati`.

### 3. Numeri live di protocol metrics su DefiLlama
- Il file originale era coerente con uno snapshot di DefiLlama che mostrava circa:
  - `Fees annualized ~$766.9M`
  - `Revenue annualized ~$681.2M`
  - `Fees 30d ~$62.9M`
  - `Revenue 30d ~$55.8M`
  - `Perp volume 30d ~$196.4B`
  - `DEX volume 30d ~$3.6B`
  - `Open interest ~$7.54B`
- Nel ricontrollo odierno, le stesse metriche oscillano in un range circa:
  - `Fees annualized ~$747M-$848M`
  - `Revenue annualized ~$664M-$730M`
  - `Fees 30d ~$61M-$70M`
  - `Revenue 30d ~$54M-$60M`
  - `Perp volume 30d ~$185B-$207B`
  - `DEX volume 30d ~$3.6B-$4.2B`
  - `Open interest ~$7.1B-$7.7B`
- Stato: `snapshot originario plausibile e supportato, ma già driftato`.

### 4. Q1 2026 income statement
- Nel file ho usato:
  - `Gross Protocol Revenue ~$214.95M`
  - `Builder code fees ~$17.42M`
- Un ricontrollo successivo su DefiLlama mostra più vicino a:
  - `Gross Protocol Revenue ~$203.99M`
  - `Builder code fees ~$16.40M`
- Stato: `da aggiornare`.
- Nota: qui il punto importante non cambia. Il business resta molto grande; cambia il numero puntuale.

## Parzialmente confermato, ma non chiuso con rigore pieno

### 1. Fee waterfall percentuale esatta
- Confermato:
  - i docs dicono che le fee vanno a `HLP + Assistance Fund + deployers`
  - i docs confermano burn dell’HYPE nell’Assistance Fund
  - DefiLlama methodology modella `1% HLP / 99% Assistance Fund` per perps e spot protocol fees, con eccezioni su builders/unit
- Non chiuso:
  - una fonte secondaria Tokenomist parla anche di `97%` delle trading fees verso daily HYPE buybacks
- Giudizio:
  - `meccanismo confermato`
  - `percentuale esatta da non trattare come fatto definitivo senza verifica onchain/contabile più profonda`

### 2. Claim di aprile 2026 completato onchain
- Confermato: esiste l’`announced claim` di `~330k HYPE`
- Non confermato con sufficiente rigore nelle fonti aperte consultate: `completed on-chain claim`
- Giudizio: il mio file era corretto a lasciarlo come punto aperto

### 3. Market structure del token
- Confermato:
  - HYPE scambia su molte venue
  - la liquidità secondaria è reale
  - il volume 24h è materiale
- Non confermato:
  - borrow cost
  - short availability
  - basis
  - funding completo
  - holder concentration aggiornata con qualità sufficiente
- Giudizio:
  - il file originale era giusto a segnalare limiti informativi
  - il label finale `market setup: favorevole` era un po’ troppo sicuro

## Valutazione del giudizio finale

### Business quality
- `Alta`: confermata

### Token quality
- `Alta`: confermata
- Motivo: HYPE ha utility reale, buyback meccanico e burn permanente documentato

### Market setup
- Originale: `favorevole`
- Revisione: `neutro`
- Motivo: la liquidità è buona, ma mancano ancora dati completi su market structure derivata e concentrazione holder per chiamarlo favorevole con rigore alto

### Verdict
- Originale: `fairly priced`
- Revisione: `fairly priced`
- Motivo: resta la conclusione più robusta anche dopo il controllo

### Confidenza
- Originale: `media`
- Revisione: `media`
- Motivo: sufficiente sui fondamentali; non alta per via di waterfall percentuale esatta, claim completion e market structure incompleta

## Sintesi finale
- Il file originale è `buono sul framework`, `buono sulle tesi strutturali`, `discreto sui numeri live`.
- Le parti da correggere davvero sono poche ma importanti:
  - `>$45M` builder codes va aggiornato a `>$65M`
  - alcuni numeri live di prezzo/fees/revenue/volume sono già mossi
  - `market setup: favorevole` era troppo assertivo; meglio `neutro`
- La conclusione principale non cambia:
  - `business quality alta`
  - `token quality alta`
  - `verdict: fairly priced`
