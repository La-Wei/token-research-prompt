# Onchain Attribution Audit: `HeyAnon / ANON`

## Data audit
- Data audit: `2026-04-14`
- Obiettivo:
  - capire se esistono tracce onchain davvero attribuibili a `HeyAnon` come prodotto, non solo a `ANON` come token
- Domande guida:
  - l estensione puo avere funzioni reali anche senza molti contratti proprietari?
  - quali contratti pubblici esistono davvero?
  - quali flussi onchain possiamo attribuire a `HeyAnon` con rigore?
  - esiste una meccanica onchain osservabile di `ANON value capture`?

## Esito sintetico
- l estensione puo plausibilmente avere funzioni reali anche con impronta onchain proprietaria limitata: `si`
- superficie contrattuale pubblica del prodotto: `molto sottile`
- prova onchain attribuibile al prodotto: `debole`
- prova onchain attribuibile al token capture: `non trovata`
- giudizio netto:
  - il quadro e coerente con un prodotto che orchestra wallet, account, overlay browser e integrazioni terze
  - non e coerente con un protocollo onchain trasparente in cui usage, fees e token accrual si leggono facilmente da contratti pubblici propri
  - quindi l assenza di forti tracce onchain non dimostra che il prodotto sia finto, ma impedisce di usarle come prova seria di traction o token capture

## Fonti usate
- Docs contratti:
  - https://docs.heyanon.ai/heyanon.ai/general-information/contracts
- Docs prodotto e onboarding:
  - https://docs.heyanon.ai/heyanon-v2/readme/getting-started
  - https://docs.heyanon.ai/heyanon-v2/readme/getting-started/log-in-with-web3-wallet
  - https://docs.heyanon.ai/heyanon-v2/readme/getting-started/account-settings
  - https://docs.heyanon.ai/heyanon-v2/readme/writing-your-first-prompt
  - https://docs.heyanon.ai/heyanon-v2/readme/integrated-protocols
  - https://docs.heyanon.ai/heyanon.ai/hud/installation-of-the-hud
  - https://docs.heyanon.ai/heyanon.ai/hud/hyperliquid-builder-code
- Explorer / onchain:
  - https://etherscan.io/address/0x79bbf4508b1391af3a0f4b30bb5fc4aa9ab0e07c
  - https://arbiscan.io/token/0x79bbF4508B1391af3A0F4B30bb5FC4aa9ab0E07C
  - https://bscscan.com/token/0x79bbf4508b1391af3a0f4b30bb5fc4aa9ab0e07c
  - https://basescan.org/token/0x79bbf4508b1391af3a0f4b30bb5fc4aa9ab0e07c
  - https://sonicscan.org/address/0x8054a4fbd093808af4529187d3efb9f6301ab92f
  - https://etherscan.io/address/0x8054a4fbd093808af4529187d3efb9f6301ab92f
- Governance / token routing:
  - https://forum.heyanon.ai/t/rfc-2-heyanon-tokenomics-utility-overview/58
  - https://forum.heyanon.ai/t/rfc-3-heyanon-hud-revenue-and-anon-token-utility/106

## 1. L estensione puo esistere con funzioni reali anche senza molti contratti proprietari?
### Cosa dicono le fonti
- `Getting started` e `Log in with Web3 Wallet` mostrano che HeyAnon offre:
  - login via `Telegram`, `Passkey`, `Web3 Wallet`
  - generazione di un nuovo wallet HeyAnon
  - sincronizzazione di wallet `EVM`, `Solana`, `TON`
- `Account settings` mostra funzioni tipiche di una app operativa:
  - referral code HUD
  - wallet whitelist
  - token list personalizzata
  - connessioni CEX con `API key / secret`
  - recovery
  - export private keys
  - `Plan Flow` con preview delle azioni prima dell esecuzione
- `Writing your first prompt` e `Protocol Prompt List` mostrano un modello prodotto in cui l app:
  - interpreta prompt
  - sceglie protocolli / aggregatori
  - esegue azioni via wallet o integrazioni esterne
- `Installation of the HUD` descrive un overlay browser sopra piattaforme terze come:
  - `TradingView`
  - `Dexscreener`
  - `Hyperliquid`
  - `Axiom`
  - `photon`
  - `gmgn`

### Implicazione analitica
- Sì, e assolutamente possibile che l estensione abbia funzioni reali anche senza un grosso footprint di smart contract proprietari.
- In questo design, il valore puo stare soprattutto in:
  - orchestrazione offchain
  - account abstraction applicativa
  - gestione wallet
  - overlay UX
  - routing verso protocolli terzi
- Quindi:
  - `assenza di app contracts pubblici` non implica automaticamente `assenza di funzioni`
  - implica pero che il ledger da solo racconta molto meno del prodotto di quanto succede in un protocollo onchain nativo

### Verdict
- giudizio: `si, e plausibile`
- frase secca:
  - HeyAnon sembra piu simile a un `execution/orchestration layer` sopra protocolli esistenti che a un protocollo onchain autonomo con forte settlement interno

## 2. Quali contratti pubblici esistono davvero?
### Cosa e pubblicato ufficialmente
- La pagina `Contracts` pubblica solo i contratti `ANON TOKEN OFT_V2`.
- Per le chain EVM compare sempre lo stesso indirizzo:
  - `0x79bbF4508B1391af3A0F4B30bb5FC4aa9ab0E07C`
- Per Solana compaiono:
  - `programId`
  - `mint`
  - `mintAuthority`
  - `escrow`
  - `oftStore`
- Non sono pubblicati, nella stessa pagina, indirizzi espliciti per:
  - treasury wallet operativo
  - reward distributor
  - staking contract `xANON`
  - buyback module
  - burn module
  - fee vault
  - router / executor / settlement contracts del prodotto
  - builder address Hyperliquid

### Cosa mostrano gli explorer
- Il contratto `ANON` su explorer e verificato come codice minimale LayerZero `OFT` + `Ownable`.
- Il costruttore passa:
  - `_name = HeyAnon`
  - `_symbol = Anon`
  - `_delegate = 0x8054A4fBd093808AF4529187D3Efb9F6301ab92f`
- Il wallet `0x8054...ab92f` appare come deployer / delegate su piu chain e compie soprattutto chiamate di configurazione:
  - `Set Peer`
  - `Set Config`
  - `Set Enforced Options`
- Su Sonic l explorer etichetta questo indirizzo come `Hey Anon: Deployer`.

### Implicazione analitica
- La superficie contrattuale pubblica che possiamo attribuire con sicurezza a HeyAnon e quasi tutta `token infrastructure`, non `product infrastructure`.
- Questo e un punto molto importante:
  - onchain vediamo bene `ANON the token`
  - vediamo molto meno `HeyAnon the app`

### Verdict
- giudizio: `pubblicato soprattutto il token, non il motore economico del prodotto`

## 3. Cosa ci dicono davvero i contratti onchain sul token?
### Fatti verificabili
- Il codice del token verificato sugli explorer e essenzialmente:
  - un `OFT` di LayerZero
  - con `Ownable(_delegate)`
- Non emerge nel contratto pubblico del token una logica nativa di:
  - buyback
  - burn automatico
  - staking rewards
  - revenue share
  - fee redistribution
  - treasury streaming
  - xANON

### Implicazione analitica
- Questo da solo non uccide il token.
- Pero significa una cosa molto concreta:
  - qualsiasi `token capture` seria non e leggibile dal contratto `ANON` stesso
  - deve vivere altrove: offchain, in altri contratti non pubblicati, o in processi discrezionali del team / DAO

### Verdict
- giudizio: `il token onchain non mostra accrual meccanico nativo`

## 4. Esistono tracce onchain di attivita che suggeriscono vita del sistema?
### Cosa si vede
- Gli explorer mostrano attivita non nulla del token e della sua infrastruttura:
  - `Etherscan` per il token contract indica `3,317` transazioni totali
  - `BscScan` per il token contract indica `8,149` transazioni totali
  - `Arbiscan` mostra, nello snapshot crawl, `857` holders e supply locale `~160,904 ANON`
  - `BscScan` mostra `388` holders e supply locale `~87,350 ANON`
  - `BaseScan` mostra `77,102` holders e supply locale `~1,074,703 ANON`
- I contratti e il deployer mostrano configurazioni cross-chain ripetute via LayerZero.

### Cosa dimostra davvero
- Dimostra che:
  - il token esiste davvero cross-chain
  - il team / deployer ha configurato e mantenuto la rete OFT
  - esiste attivita reale sul token come infrastruttura di bridging / distribuzione / trading

### Cosa non dimostra
- non dimostra:
  - che quelle transazioni derivino da uso del prodotto HeyAnon
  - che i holder del token siano utenti del prodotto
  - che i volumi del token corrispondano a usage della HUD o della app
- In particolare:
  - holders di un token microcap possono derivare da exchange accounts, LP dust, farming, bridge activity o semplice trading speculativo
  - non sono una misura affidabile di adozione prodotto

### Verdict
- giudizio: `vita del token si, vita del prodotto non isolabile`

## 5. Esiste una traccia onchain osservabile di revenue o fee del prodotto?
### Cosa dicono le fonti
- La pagina `Hyperliquid builder code` dice che:
  - gli utenti approvano una `builder address`
  - HeyAnon applica `10 bps` sulle chiusure profittevoli
  - il fee viene distribuito al builder address HeyAnon
- `RFC #3` dice che:
  - esistono `HUD-generated revenue` e referral fees da venue come `Hyperliquid`, `Axiom`, `Photon`, `gmgn`
  - il punto del proposal e `formalize` come questa revenue venga instradata a beneficio dei token holder

### Cosa sono riuscito a verificare
- Sono riuscito a verificare che la meccanica sia descritta pubblicamente.
- Non sono riuscito a verificare con rigore:
  - quale sia il `builder address` di HeyAnon
  - quali address ricevano i referral fees
  - quanti fee siano stati incassati
  - se ci sia una treasury onchain pubblicamente riconciliabile che riceva questi flussi

### Implicazione analitica
- Questo e il buco piu importante dell intero audit.
- La revenue del prodotto potrebbe anche esistere.
- Ma senza address pubblici, dashboard o flussi riconciliabili:
  - non possiamo trattarla come prova economica forte
  - non possiamo collegarla con rigore a `ANON`

### Verdict
- giudizio: `revenue plausibile, ma non auditabile pubblicamente con rigore`

## 6. Esiste una prova onchain che `ANON` catturi valore?
### Cosa ho verificato
- Il contratto `ANON` pubblico non contiene meccaniche native di accrual.
- `RFC #2` e `RFC #3` parlano di:
  - `ANONs`
  - pass
  - fee routing
  - staking / xANON
  - buyback & burn
- pero queste fonti sono:
  - governance design
  - proposta di formalizzazione
  - non prova onchain live gia misurabile

### Cosa non ho trovato
- non ho trovato:
  - contract address pubblici di `xANON`
  - proof di burn sistematico
  - proof di buyback sistematico
  - treasury wallet pubblicamente etichettato e riconciliato
  - revenue distributor osservabile
  - bridge esplicito `fee wallet -> ANON holder`

### Verdict
- giudizio: `no, non c e prova onchain pulita di token capture`

## 7. Cosa significa questo per il caso `molto early`?
- Se il prodotto fosse completamente finto, mi aspetterei:
  - docs povere
  - nessuna integrazione credibile
  - nessuna distribuzione software
  - nessun repo o guida tecnica
- Qui non vediamo questo.
- Ma se il prodotto fosse gia `provato economicamente`, mi aspetterei anche:
  - address pubblici
  - fee wallet pubblici
  - builder address pubblico
  - dashboard usage / revenue
  - meccanica live di token capture
- Questo secondo blocco invece manca.

### Sintesi pratica
- `molto early` sul prodotto:
  - `possibile`
- `molto early` sul token con edge misurabile:
  - `non ancora dimostrato`
- `molto raccontato`:
  - `si, ancora parecchio`

## Checklist finale
- cose che l audit conferma:
  - HeyAnon puo avere funzioni reali anche senza pesante infra onchain propria
  - il token e davvero deployato e mantenuto cross-chain
  - esiste un deployer / delegate attivo
- cose che l audit non conferma:
  - uso economico del prodotto leggibile onchain
  - fee flow riconciliabile
  - token accrual dimostrato
- cose che servirebbero per cambiare giudizio:
  - pubblicazione del builder address HeyAnon
  - pubblicazione di treasury / fee wallets
  - dashboard pubblica di usage e revenue
  - contratti pubblici per `xANON`, buyback, burn o reward distribution

## Conclusione netta
- risposta alla domanda `ma possibile che ci sia l estensione senza funzioni?`
  - `si, in teoria`
  - ma qui la lettura piu corretta e un po diversa:
  - `non sembra un estensione senza funzioni`
  - `sembra un estensione / app con funzioni plausibili, ma con economics e traction pubblicamente poco verificabili`
- motivo principale:
  - la superficie onchain pubblica mostra soprattutto il token `ANON` e la sua infrastruttura cross-chain; non mostra ancora in modo trasparente il motore economico del prodotto ne una cattura di valore del token abbastanza leggibile da ledger
