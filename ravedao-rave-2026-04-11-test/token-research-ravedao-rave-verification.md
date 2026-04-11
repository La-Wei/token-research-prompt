# Verification Audit

## Data di verifica
- Protocollo / ticker verificato: `RaveDAO / RAVE`
- Report verificato: `ravedao-rave-2026-04-11-test/token-research-ravedao-rave-test.md`
- Prompt base di riferimento: `token-research-prompt.md`
- Data di verifica: `2026-04-11`
- Approccio: verifica di claim strutturali, waterfall, token rights, supply, vesting, unlock overhang, market data live ed eventi recenti usando sito ufficiale, whitepaper ufficiale, MiCAR white paper ufficiale, explorer onchain e pagine ufficiali di prodotto / exchange dove disponibili

## Esito sintetico
- Esito generale: `confermato nel nucleo, con alcune correzioni materiali e alcune rifiniture metodologiche`
- Il cuore del report regge:
  - `RaveDAO` ha un business/event brand reale e non puramente cartaceo
  - `RAVE` non conferisce diritti economici su profitti, ricavi o dividendi
  - la narrativa `buyback & burn` non e sufficientemente chiusa con rigore documentale
  - il vero rischio di supply non e l inflazione continua ma l `unlock / vesting overhang`
  - il market setup e dominato da `float scarcity + listing / narrative reflexivity`
- Le sezioni piu solide del report originale sono:
  - distinzione tra `business reale` e `token economicamente forte`
  - analisi di `waterfall`
  - analisi di `float vs supply`
  - lettura critica del contrasto tra whitepaper marketing e filing MiCAR
- Le correzioni principali che emergono dalla verifica sono:
  - `Coinbase access / listing`: nel report originale era trattato come ambiguo; nella verifica va trattato come `sostanzialmente confermato`
  - `staking / loyalty`: il filing MiCAR li presenta come funzioni pianificate per la fase successiva, non come funzioni pienamente dimostrate gia live in tutte le loro forme
  - `20+ eventi in 12 citta`: non sono riuscito a chiudere questo claim con la stessa solidita delle metriche `100k+ participants` e `50k+ NFT tickets`
  - `insider-linked selling`: resta allegation / market rumor, non confermato con sufficiente evidenza primaria nelle fonti verificate

## Fonti usate per la verifica
- https://ravedao.com/
- https://ravedao.gitbook.io/ravedao-whitepaper
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/introduction
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-in-action
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/impact-metrics
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics/introducing-usdrave
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics/token-distribution-schedule
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics/token-utilities
- https://ravedao.gitbook.io/ravedao-whitepaper/readme/ravedao-tokenomics/future-of-usdrave
- https://ravedao.github.io/rave-xhtml/
- https://www.coingecko.com/en/coins/ravedao
- https://etherscan.io/token/0x17205fab260a7a6383a81452ce6315a39370db97
- https://etherscan.io/tx/0xbb0323aff38f0308ee1df9bffed145426e7f6dd7e2ecc86ce4569f49300d3039
- https://www.coinbase.com/converter/rave/rai
- https://x.com/CoinbaseMarkets/status/2019132783679971728
- https://www.plvr.io/events/ravedao-consensus-rsvp-202602120-hk
- https://www.plvr.io/events/dim-sum-rave
- https://www.plvr.io/events/ravedao-dubai-token2049-20260501-ae
- https://www.plvr.io/events/lds-closing-party-x-ravedao-20260501-pt

## Eventi recenti verificati
- `Evento confermato`
  - `2026-02-04`: `Coinbase Markets` ha aggiunto `RAVE` alla roadmap pubblica.
  - `2026-02-11`: le fonti ufficiali di prodotto Coinbase consultate indicano che `RaveDAO` e acquistabile su `Coinbase centralized exchange`; questo conferma che la storia `Coinbase access` non era solo rumor di mercato.
  - `2026-02-12`: la pagina ufficiale evento `RaveDAO Consensus $RAVE Party` conferma un activation con incentivo esplicito in `$RAVE` per early check-in / in-person attendance.
  - `2026-04-10`: `CoinGecko` conferma nuovo `ATH` a `~$1.65` e forte market reaction; nello snapshot aperto in verifica il token segna `~$1.55`, `+62.2%` 24h, market cap `~$371.09M`, FDV `~$1.55B`, 24h volume `~$366.11M`.
  - `2026-04-18` e `2026-04-30`: le pagine ufficiali `PLVR` confermano che RaveDAO continua a promuovere eventi live a Hong Kong e Dubai; questo supporta la continuita operativa del business.

- `Allegation o claim non dimostrato`
  - il report originale trattava come plausibile una narrativa di `insider-linked selling` e market manipulation nel blocco eventi recenti; nelle fonti verificate non ho trovato una prova primaria sufficiente per chiuderla come fatto
  - il driver esatto del rally di `2026-04-10` non e chiuso con rigore pieno: listing/access, reflexivity, squeeze e bassa float possono aver contribuito insieme
  - non ho trovato una risposta ufficiale del team che chiuda in modo documentato le accuse social / rumor di selling

- `Risposta del team / fonte primaria`
  - non ho trovato nelle fonti primarie verificate un comunicato ufficiale strutturato del team che risponda in modo chiaro a eventuali accuse di insider selling o whale manipulation
  - la miglior fonte primaria disponibile per il perimetro evento recente resta quindi:
    - roadmap / availability ufficiale Coinbase
    - pagine ufficiali evento RaveDAO / PLVR
    - CoinGecko per il market reaction snapshot

- `Market reaction osservata`
  - `CoinGecko` nello snapshot verificato mostra:
    - prezzo `~$1.55`
    - `24h +62.2%`
    - market cap `~$371.09M`
    - FDV `~$1.55B`
    - 24h volume `~$366.11M`
    - ATH `~$1.65` il `2026-04-10`
  - il mercato ha quindi prezzato `RAVE` come asset in piena modalita reflexive / listing-driven, non come semplice utility token stabile

- `Lettura 7d / 30d / 90d`
  - ultimi `7d`: non ho trovato exploit, halt, governance dispute ufficiali o parameter changes materiali; il fatto dominante e il `price squeeze`
  - ultimi `30d`: la fonte primaria mostra continuita commerciale / evento e mantenimento della narrativa di espansione, ma nessuna prova nuova di miglioramento del waterfall token
  - ultimi `90d`: l evento piu materiale per il token e la sequenza `Coinbase roadmap -> Coinbase availability`, che migliora accesso e liquidita ma non cambia i diritti economici del token

## Confermato
- `Descrizione del progetto`: confermata. RaveDAO e meglio descritto come `entertainment / cultural protocol` o `event brand tokenizzato`, non come protocollo infrastrutturale classico.
- `Business reale`: confermato. Il sito ufficiale, il whitepaper e il filing MiCAR supportano l esistenza di eventi reali, sponsor, ticketing, membership e footprint geografica internazionale.
- `Revenue business reale`: confermato. Il MiCAR white paper dichiara `~$3M` di revenue cumulata `2024-2025 YTD` e dettaglia le principali linee di ricavo.
- `No token sale / no equity fundraising`: confermato. Il filing MiCAR dice esplicitamente che il business e bootstrapped e non si e sostenuto tramite token sale o equity fundraising.
- `Token rights limitati`: confermato. Il filing MiCAR e molto chiaro sul fatto che `RAVE` non conferisce `ownership, equity rights, or claims on profits, revenues, or dividends`.
- `Governance limitata / consultativa`: confermata. Il filing MiCAR dice che la governance non modifica i diritti legali, finanziari o strutturali del token.
- `Supply cap 1B`: confermato.
- `Issuer retained 200M`: confermato.
- `Nessuna inflazione continua`: confermato. Il filing MiCAR parla di fixed supply e di assenza di ongoing minting / inflation.
- `Vesting schedule`: confermato nel nucleo. Il whitepaper ufficiale supporta `~23.03%` a TGE e un vesting lungo con cliff / release graduali per la parte maggiore della supply.
- `Unlock overhang come rischio centrale`: confermato. La combinazione di circulating `~239.17M` e vesting `~760.83M` su CoinGecko supporta pienamente questa lettura.
- `Contrasto whitepaper vs MiCAR sul buyback`: confermato. Il whitepaper marketing parla di `Buyback & Burn`, mentre il MiCAR filing dichiara `Supply Adjustment Protocols: false` e `Token Value Protection Schemes: false`.
- `Waterfall debole verso il token`: confermato. Il business puo generare ricavi, ma il filing ufficiale non dimostra un ponte economico chiaro e hard-coded verso gli holder di `RAVE`.
- `Bridge mechanics rilevanti per interpretare i burn`: confermato. Il contratto verificato su Etherscan e costruito su `OFT / LayerZero`, e almeno una transazione con burn verso `0x000...000` mostra anche `PacketSent` / `OFTSent`, quindi la prudenza del report su burn permanenti vs bridge mechanics era corretta.
- `Piccola float / market structure riflessiva`: confermata. CoinGecko mostra market cap/FDV `~0.24`, supply circolante `~239.17M` su `1B`, e vesting molto elevato.
- `Continuita operativa del progetto`: confermata. Le pagine `PLVR` mostrano eventi passati, recenti e upcoming nel corso del 2026.

## Da correggere o aggiornare
- `Coinbase access / listing`
  - nel report originale la narrativa `Coinbase access` era trattata come `parzialmente verificata / ambigua`
  - questa parte va corretta: la combinazione tra roadmap pubblica `Coinbase Markets` del `2026-02-04` e pagina ufficiale Coinbase consultata in verifica supporta che `RAVE` sia effettivamente disponibile su Coinbase
  - implicazione: l evento `listing / access improvement` va trattato come `confermato`, non come rumor ambiguo

- `Staking / loyalty / rewards presentati come gia disponibili`
  - nel report originale alcune frasi su utility potevano far sembrare `staking` e `loyalty rewards` gia pienamente operativi
  - il filing MiCAR invece dice che, dopo le listings, accesso a ticketing / event participation / community governance e immediato, mentre `staking and loyalty reward functions are scheduled to launch in the next development phase`
  - implicazione: l utilita live del token va descritta in modo piu prudente

- `Claim marketing su scala: 20+ eventi in 12 citta`
  - non ho chiuso questo numero con lo stesso rigore delle metriche `100k+ participants` e `50k+ NFT tickets`, che risultano invece piu chiaramente supportate dal whitepaper
  - implicazione: nel report originale conviene abbassare il grado di certezza di quel numero o citare una fonte primaria piu precisa

- `Allegation su insider-linked selling`
  - la sezione eventi del report originale menzionava questa narrativa con prudenza, ma per un report di rigore buy-side e ancora troppo vicina a social rumor
  - implicazione: senza wallet mapping, proof onchain robusta o risposta ufficiale, questa parte va declassata a `allegation non dimostrata`

- `Metriche live di explorer / market data`
  - i numeri esatti di Etherscan e CoinGecko sono gia cambiati nel corso della verifica
  - Etherscan, ad esempio, nello snapshot verificato mostra:
    - max total supply Ethereum-side `~972.74M`
    - holders `10,392`
    - circulating supply market cap `~$246.02M`
  - implicazione: i numeri spot del report originale non sono `sbagliati` in senso forte, ma sono gia da aggiornare se il report viene riutilizzato

## Parzialmente confermato, ma non chiuso con rigore pieno
- `Buyback & burn come meccanica economica rilevante`
  - confermato che il marketing lo promette
  - non confermato con prova primaria sufficiente che esista una meccanica sistematica, quantificata e verificabile onchain

- `On-chain transparency del business`
  - il filing MiCAR dice che una parte significativa del revenue e processata onchain
  - ma non fornisce wallet addresses o reporting che permetta di ricostruire il waterfall

- `Governance partecipativa`
  - confermato che esiste una narrativa / struttura di partecipazione community
  - non chiuso con rigore pieno quanto questa governance sia economicamente o operativamente incisiva oltre il piano consultativo

- `Metriche di impatto e scala commerciale team-reported`
  - `100k+ participants`, `50k+ NFT tickets`, `150M+ impressions` e altri numeri di impatto sono coerenti col materiale ufficiale
  - ma restano soprattutto `team-reported`, non auditati da dashboard indipendenti pienamente riconciliabili

- `Perimetro esatto di burning permanente vs bridge`
  - e confermato che almeno parte dei burn osservati e coerente con cross-chain mechanics
  - non ho una riconciliazione completa di tutti i burn / bridge events, quindi la lettura migliore resta prudente

- `Causalita del rally di aprile 2026`
  - e confermato il rally e la sua intensita
  - non e chiuso con rigore pieno quanto dipenda da listing effect, whale flows, narrative squeeze o altre dinamiche di order flow

## Valutazione del giudizio finale
- `Business quality: media-bassa`
  - confermato. Il business esiste e ha sostanza sufficiente per non essere trattato come shell, ma resta piccolo, execution-heavy e dipendente da eventi / partner / market mood.

- `Necessita di esistenza del prodotto: media-bassa`
  - confermata. Il vantaggio esiste soprattutto come brand / coordination layer crypto-native, non come prodotto inevitabile o tecnologicamente insostituibile.

- `Token quality: bassa`
  - confermata e, se possibile, rafforzata.
  - Il filing MiCAR rende ancora piu chiaro che i diritti economici del token sono deboli e che la governance non e equity-like.

- `Market setup: surriscaldato e fragile`
  - confermato. La price action e i volumi di `2026-04-10 / 2026-04-11` supportano pienamente questa lettura.

- `Verdict: overpriced`
  - resta difendibile sullo snapshot del report originale.
  - La verifica non smonta la tesi; anzi, la conferma sul punto piu importante: il mercato puo aver premiato accesso, brand e scarsita di float, ma il waterfall verso il token resta debole.

- `Confidenza del giudizio: media`
  - confermata.
  - Il livello di confidenza giusto resta `media`, non `alta`, perche:
    - la market structure puo restare irrazionale a lungo
    - il business ha una componente reale non trascurabile
    - alcuni claim di scala e buyback restano team-reported / non riconciliati pienamente

## Sintesi finale
- Il report fondamentale su `RaveDAO / RAVE` e strutturalmente buono e la sua tesi centrale regge.
- I punti davvero confermati dalla verifica sono:
  - esiste un business reale
  - il token ha diritti economici molto deboli
  - il contrasto tra `buyback narrative` e `MiCAR disclosure` e reale
  - l overhang di vesting e un rischio molto piu concreto della narrativa di scarsita
  - la market structure recente e chiaramente reflexive
- Le correzioni da portarsi dietro, se il report viene riusato o rifinito, sono quattro:
  - trattare `Coinbase access` come `confermato`
  - trattare `staking / loyalty` come `planned / partially live narrative`, non pienamente chiusi
  - abbassare il grado di certezza sui claim `20+ eventi in 12 citta`
  - declassare `insider-linked selling` a `allegation non dimostrata`
- Il giudizio finale `overpriced` con `token quality bassa` e `market setup surriscaldato e fragile` rimane il piu rigoroso anche dopo la verifica.
