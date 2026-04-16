# Verification Audit: `HeyAnon / ANON`

## Data di verifica
- Data di verifica: `2026-04-14`
- Report verificato: `output/heyanon-anon-2026-04-14-test/token-research-heyanon-anon-test.md`
- Prompt base di riferimento: `prompt/token-research-prompt.md`

## Esito sintetico
- esito generale: `parzialmente confermato`
- scelta metodologica del report originale: `coerente`
- classificazione metodologica confermata: `opacity-compressed`
- errori materiali trovati: `1`
- punti da aggiornare: `3`
- verdetto finale originale: `fairly priced`
- valutazione della verifica sul verdetto finale: `difendibile, ma con price placement da ricalibrare`

## Verifica del perimetro metodologico
- La scelta `opacity-compressed` era corretta:
  - il prodotto e documentato e verificabile
  - il blocco decisivo `business -> token` resta troppo opaco per `full diligence`
  - non c e abbastanza evidenza primaria su revenue aggregate, treasury, buyback live, `xANON` operativo, holder concentration e net supply pressure effettiva
- Il report originale separa in modo sostanziale:
  - prodotto
  - token
  - market setup
  - pricing
- Il punto metodologico che non passa pienamente e il controllo `spot price / market cap`:
  - il report usa `Kraken Convert` come anchor live `~$1.23 / ~$16.59M`
  - la verifica same-day su `CoinGecko` mostra invece `ANON ~$0.8952`, market cap `~$12.45M`, circulating `13,896,103`, total supply `20,961,083`, max supply `21,000,000`
  - `CoinGecko` esplicita che il prezzo e una media volume-weighted su `28 exchanges` e `35 markets`
  - nella tabella mercati `CoinGecko`, le venue spot tracciate piu attive osservate sono tutte circa `~$0.894 - $0.900`:
    - `MEXC ANON/USDT ~ $0.8941`
    - `Raydium ANON/SOL ~ $0.8985`
    - `Gate ANON/USDT ~ $0.8982`
  - le superfici pubbliche di `Kraken` risultano internamente incoerenti:
    - `kraken.com/convert/anon/usd` mostra `~$1.24` e market cap `~$16.49M`
    - `kraken.com/prices/hey-anon` mostra `~$0.72` e market cap `~$9.60M`
    - la pagina `prices` contiene anche una descrizione errata del progetto come privacy coin, segnale di metadata contamination
- Conclusione metodologica:
  - `opacity-compressed` confermato
  - `Kraken Convert` non e abbastanza affidabile da diventare anchor finale unico del placement
  - per `ANON` il placement finale andava basato su fonti multi-venue coerenti o, quantomeno, con una divergenza Kraken dichiarata come irrisolta e materially blocking

## Fonti usate per la verifica
- https://docs.heyanon.ai/heyanon-v2/readme/writing-your-first-prompt
- https://docs.heyanon.ai/heyanon-v2/readme/integrated-protocols
- https://docs.heyanon.ai/heyanon.ai/general-information/anon-token
- https://docs.heyanon.ai/heyanon.ai/hud/hyperliquid-builder-code
- https://forum.heyanon.ai/t/rfc-2-heyanon-tokenomics-utility-overview/58
- https://forum.heyanon.ai/t/rfc-3-heyanon-hud-revenue-and-anon-token-utility/106
- https://forum.heyanon.ai/t/temperature-check-conditional-treasury-anon-support-below-1-revised-pilot-based/129
- https://forum.heyanon.ai/t/rfc-5-hey-anon-dao-ai-agent-launchpad-applications/132
- https://forum.heyanon.ai/
- https://www.coingecko.com/en/coins/hey-anon
- https://www.kraken.com/convert/anon/usd
- https://www.kraken.com/prices/hey-anon
- https://coinmarketcap.com/currencies/hey-anon/

## Eventi recenti verificati
- `2026-04-10` `RFC #5 Hey Anon DAO – AI Agent Launchpad Applications`
  - confermato:
    - HeyAnon DAO apre le candidature per un launchpad di AI agents
    - il testo dice che il launchpad e sviluppato `in collaboration with Raydium`
    - tutti gli agent tokens lanciati saranno `paired with ANON`
    - il DAO convertira `Sonic` dalla treasury in `ANON` con `open market purchases` in batch prima del lancio
  - allegation o claim non dimostrato:
    - che il launchpad parta davvero nei tempi proposti
    - che i flussi siano abbastanza grandi da cambiare materialmente il pricing di `ANON`
  - market reaction osservata:
    - non dimostrabile con rigore causale tick-by-tick
    - ma il tema e chiaramente `token-positive` sul piano narrativo e di design
- `2026-03-02` `Temperature Check — Conditional Treasury ANON Support Below $1`
  - confermato:
    - il moderation team scrive che la proposta `has again not generated meaningful participation`
    - la soglia di engagement `has not been met`
    - la proposta quindi non avanza
  - allegation o claim non dimostrato:
    - che esista comunque un `soft floor` implicito della treasury fuori governance
  - market reaction osservata:
    - non dimostrabile con rigore pieno
    - ma l evento indebolisce la narrativa di supporto automatico al token
- `2026-02-11` -> `2026-02-15` `RFC #4 Treasury ANON Price Support Below $1`
  - confermato:
    - la proposta esiste
    - il thread chiede chiarimenti su importi, meccaniche e insider selling
    - non riceve backing sufficiente per proseguire
  - implication:
    - conferma che la floor-policy non era gia un meccanismo live e chiuso
- ultimi `7d / 30d / 90d` su fonti ufficiali controllate:
  - non risultano confermati su forum e docs ufficiali un exploit materiale, un halt operativo, un founder exit, una security incident disclosure, un delisting materiale o un cambio hard-coded di tokenomics che imponga da solo il ribaltamento del verdict

## Confermato
- `Che cosa fa davvero il protocollo`
  - confermato: `HeyAnon v2` si presenta come assistente DeFi che esegue prompt conversazionali per swap, bridge, staking e portfolio actions
  - confermato: la docs dice che HeyAnon `finds the best route`, `optimizes gas fees` ed `executes the swap`
- `Breadth di integrazioni`
  - confermato: la pagina `Integrated protocols` mostra supporto reale e ampio per piu ecosistemi, moduli e CEX integrations
  - confermato: la docs elenca `15` reti EVM e `2` non-EVM, quindi una superficie multi-chain ampia
- `Tokenomics headline`
  - confermato: la pagina `Anon token` riporta `Total Supply 21,000,000`, `ICO 10,500,000`, `Team 6,100,000`, `Foundation / treasury 4,200,000`
  - confermato: la stessa pagina mostra un release schedule mensile da `87,500` token dal `Mar-25` al `Feb-29`
- `Monetizzazione localizzata`
  - confermato: la pagina `Hyperliquid builder code` descrive una fee di `10 bps` applicata alle sole posizioni chiuse in profitto
- `Token utility come design goal, non come holder cash flow live`
  - confermato: `RFC #2` e `RFC #3` parlano di pass, locking, penalty sharing, burn, `xANON staking` e treasury routing come architettura / proposta, non come meccanismo gia definitivamente verificato onchain e live
- `Classificazione metodologica`
  - confermato: `opacity-compressed` resta la classificazione giusta

## Da correggere o aggiornare
- `Spot anchor / market cap`
  - errore materiale del report originale:
    - il blocco `Kraken Convert` usato come anchor finale `~$1.23 / ~$16.59M` non regge la verifica cross-source
    - `CoinGecko` same-day mostra `~$0.8952 / ~$12.45M`
    - le venue spot osservate nella market table di `CoinGecko` sono tutte circa `~$0.894 - $0.900`
    - `Kraken` stesso ha superfici pubbliche incoerenti: `convert ~ $1.24` contro `prices ~ $0.72`
  - sezioni del report originale da correggere o ricalibrare:
    - `Materiale minimo per l analisi > Snapshot numerico essenziale`
    - `Source reconciliation evidence log > spot price`
    - `2A.3 Market structure / holders compressed`
    - `16. Valuation thinking`
    - `17. Price map e scenario map`
    - `17A. Verdict calibration bridge`
- `Numero di reti / protocolli`
  - da aggiornare:
    - il report originale parla di `14 networks` e `150+ protocols`
    - la pagina `Integrated protocols` verificata mostra invece `15` reti EVM + `2` non-EVM, quindi `17` reti totali
    - la stessa pagina elenca molti moduli e protocolli, ma la cifra esatta `150+ protocols` non e dimostrata dal source citato
- `Gap di supply spiegato in modo incompleto`
  - da aggiornare:
    - il report originale dice che restano `~1.9M ANON` non spiegati
    - la docs ufficiale aggiunge che `from the Treasury allocation, we have dedicated 2% for KOL's and partnerships`
    - questo non chiude del tutto la riconciliazione, ma riduce il gap non spiegato a circa `~1.48M` se quel `2%` e letto come `2 punti percentuali` della total supply presi dalla treasury
    - resta anche un residuo di `~200k` tra somma assoluta delle bucket (`20.8M`) e max supply (`21.0M`)

## Parzialmente confermato, ma non chiuso con rigore pieno
- `Necessita del prodotto`
  - parzialmente confermato: il prodotto ha sostanza e una surface area reale
  - non e chiudibile con rigore pieno l entita del vantaggio vs wallet, aggregatori e assistenti non tokenizzati
- `Bridge business -> token debole`
  - parzialmente confermato: tutta la documentazione punta nella stessa direzione
  - ma manca ancora prova forte di un flusso economico live, ricorrente e verificabile a favore dell holder di `ANON`
- `Supply / unlock / treasury overhang`
  - parzialmente confermato: la docs fornisce headline, schedule e una nota sulle partnership
  - non chiude pero in modo pieno:
    - la bucket `Team / Partnerships`
    - la differenza tra assoluti e percentuali
    - la vera supply liquida
    - la treasury effettivamente disponibile
- `Holder base e market structure`
  - parzialmente confermato: `CoinGecko` mostra circulating `13.896M`, market list, depth e volume per alcune venue
  - non chiude con rigore pieno:
    - top wallet concentration
    - quote su exchange
    - presenza / ruolo dei market maker
    - quality del float tradabile
- `Catalizzatore RFC #5`
  - parzialmente confermato: il proposal e reale e token-positive sulla carta
  - non e ancora un evento economico concluso o un flusso live verificato

## Source reconciliation residua
- `Spot price`
  - `CoinGecko` aggregate same-day: `~$0.8952`
  - `MEXC / Raydium / Gate` osservati via `CoinGecko Markets`: `~$0.894 - $0.900`
  - `Kraken Convert`: `~$1.24`
  - `Kraken Prices`: `~$0.72`
  - implicazione:
    - non esiste un anchor singolo pulito su Kraken
    - per il placement finale bisogna usare una media multi-venue coerente o dichiarare la divergenza come non chiusa
- `Market cap`
  - `CoinGecko`: `~$12.45M`
  - `Kraken Convert`: `~$16.49M`
  - `Kraken Prices`: `~$9.60M`
  - implicazione:
    - il market cap del report originale era troppo dipendente da una venue surface contestata
- `Supply`
  - `docs`: max `21.0M`, assoluti `20.8M`, schedule `4.2M`, nota `2%` partnership dalla treasury
  - `CoinGecko`: total supply `20,961,083`, circulating `13,896,103`, max `21,000,000`
  - implicazione:
    - la supply story e leggibile solo in forma prudente, non come narrativamente pulita
- `Token utility`
  - `RFC #2 / RFC #3 / RFC #5`: design e proposals
  - `docs product`: prodotto e fee localizzate
  - implicazione:
    - utilita e potential accrual esistono come direzione
    - l accrual holder-level resta in larga parte non dimostrato come meccanica live end-to-end

## Valutazione del giudizio finale
- `business quality: media`
  - valutazione verifica: `confermabile`
  - motivo: il prodotto e reale e ampio, ma il moat resta discutibile
- `necessita di esistenza del prodotto: media`
  - valutazione verifica: `confermabile`
  - motivo: c e un bisogno reale di UX compression, ma non chiaramente un bisogno che richieda per forza un token
- `necessita del token per il prodotto: bassa`
  - valutazione verifica: `confermabile`
  - motivo: la docs non dimostra che senza token il prodotto collassi
- `token quality: bassa`
  - valutazione verifica: `difendibile`
  - motivo: il problema non e l assenza totale di design, ma l opacita di implementation, supply e accrual
- `token accrual verdict: debole`
  - valutazione verifica: `confermabile`
  - motivo: le fonti ufficiali supportano meglio un frame di optionality e governance design che non un holder cash flow gia in funzione
- `market setup: fragile`
  - valutazione verifica: `confermabile`
  - motivo: microcap, depth limitata e spot divergence materiale tra venue / aggregatori
- `verdict: fairly priced`
  - valutazione verifica: `difendibile, ma da ricalibrare`
  - motivo:
    - con il `Kraken` usato dal report originale il prezzo sembrava vicino alla parte alta del range
    - con il cross-check multi-venue `CoinGecko / MEXC / Raydium / Gate`, il prezzo e piu vicino alla parte bassa o al centro-basso del corridoio base, non alla parte alta
    - il verdict `fairly priced` puo restare in piedi perche:
      - il market cap aggregato `~$12.45M` resta dentro il `base case` originale `~$10-18M`
      - il prezzo aggregato `~$0.8952` resta dentro il corridoio originale `~$0.75 - $1.35`
    - non emerge pero abbastanza rigore per una chiamata piu aggressiva tipo `sottovalutato`

## Sintesi finale
- Il report fondamentale su `HeyAnon / ANON` passa la verifica metodologica sulla scelta `opacity-compressed`, sulla lettura del prodotto come `coordination layer / product wrapper` e sulla tesi centrale che il ponte `business -> token` sia ancora debole.
- L errore materiale del file originale e il blocco `spot / market cap`: `Kraken Convert` non e un anchor affidabile per questo asset, e la verifica multi-venue porta il prezzo verso `~$0.895` e il market cap verso `~$12.45M`, non verso `~$1.23 / ~$16.59M`.
- Ci sono poi tre aggiornamenti importanti ma non thesis-breaking:
  - la docs supporta `17` reti, non `14`
  - il claim `150+ protocols` non e dimostrato dal source citato
  - la nota `2% for KOL's and partnerships` riduce il gap di supply non spiegato, pur senza chiuderlo del tutto
- Non emerge alcuna evidenza che imponga di riclassificare il report da `opacity-compressed` a `full diligence`.
- Non emerge alcuna evidenza che imponga di ribaltare il verdetto finale da `fairly priced`, ma il posizionamento corretto e:
  - `fairly priced`
  - con confidenza `bassa`
  - e con prezzo piu vicino alla parte bassa / centro-bassa del corridoio, non alla parte alta.
