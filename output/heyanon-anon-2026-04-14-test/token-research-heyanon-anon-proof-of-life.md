# Proof-of-Life Audit: `HeyAnon / ANON`

## Data audit
- Data audit: `2026-04-14`
- Obiettivo:
  - capire se `HeyAnon` sia solo una narrativa o se esista almeno una base pubblicamente verificabile di prodotto, utenti e meccaniche economiche
- Test richiesti:
  - prove pubbliche che persone reali lo usino davvero
  - tracce onchain o metriche che mostrino attivita attribuibile al prodotto
  - prove che `ANON` catturi davvero qualcosa oltre alla narrativa

## Esito sintetico
- esistenza del prodotto: `confermata in modo ragionevole`
- prova di uso pubblico reale: `parzialmente confermata`
- prova di traction economica pubblica: `debole`
- prova di token capture live oltre la narrativa: `non confermata`
- giudizio netto:
  - `HeyAnon` non appare come pagina vuota o pura finzione
  - pero il mercato non ha oggi abbastanza prove pubbliche di uso materiale e soprattutto di `ANON value capture` per trattarlo come caso forte di execution gia dimostrata
  - la lettura piu onesta e: `piu reale di un vaporware, molto meno provato di un prodotto con traction pubblica`

## Fonti usate
- Chrome Web Store `Anon HUD`:
  - https://chromewebstore.google.com/detail/anon-hud/oimcinaflljpjficmfbibjjcaailecnk
- Docs prodotto / onboarding:
  - https://docs.heyanon.ai/heyanon.ai/hey-anon/video-tutorials
  - https://docs.heyanon.ai/heyanon-v2/readme/getting-started
  - https://docs.heyanon.ai/heyanon-v2/readme/getting-started/log-in-with-web3-wallet
  - https://docs.heyanon.ai/heyanon.ai/hud/installation-of-the-hud
  - https://docs.heyanon.ai/heyanon.ai/features
  - https://docs.heyanon.ai/heyanon-v2/readme/integrated-protocols
  - https://docs.heyanon.ai/heyanon.ai/contracts
- Docs / governance token capture:
  - https://docs.heyanon.ai/heyanon.ai/general-information/anon-token
  - https://forum.heyanon.ai/t/rfc-2-heyanon-tokenomics-utility-overview/58
  - https://forum.heyanon.ai/t/rfc-3-heyanon-hud-revenue-and-anon-token-utility/106
- Community / engineering breadcrumbs:
  - https://forum.heyanon.ai/
  - https://t.me/realwagmi
  - https://github.com/RealWagmi

## 1. Prove pubbliche che persone reali lo usino davvero
### Cosa ho trovato
- `Anon HUD` esiste pubblicamente sul `Chrome Web Store` con:
  - `1,000 users`
  - `24 ratings`
  - rating `5.0/5`
  - update `2026-03-13`
- Le docs ufficiali mostrano un onboarding utente concreto, non solo marketing:
  - login via `Telegram`, `Passkey`, `Web3 Wallet`
  - generazione di wallet HeyAnon
  - account settings con referral code, wallet whitelist e CEX connection
  - tutorial base e avanzati
  - video tutorials dedicate a onboarding e connessione browser / Telegram
- La docs HUD dice esplicitamente che l estensione viene usata sopra piattaforme come:
  - `Axiom`
  - `photon`
  - `gmgn`
  - `Pumpfun advanced`
  - `TradingView`
  - `Dexscreener`
  - `Hyperliquid`
- Il canale Telegram ufficiale `Hey Anon / Wagmi` risultava pubblico con circa:
  - `5,969 members`
  - `145 online`
  - snapshot crawl `circa 3 settimane` prima dell audit

### Cosa dimostra davvero
- Dimostra che:
  - esiste un prodotto distribuibile al pubblico
  - almeno alcune persone esterne al team lo hanno installato o recensito
  - esiste una base utente / community non nulla
- Il dato piu forte qui e il `Chrome Web Store`:
  - e la prova pubblica migliore trovata che persone reali abbiano almeno installato e toccato il prodotto

### Cosa non dimostra
- non dimostra:
  - uso ricorrente
  - volume reale eseguito
  - utenti attivi giornalieri o mensili
  - retention
  - monetizzazione
  - quanti dei `1,000 users` siano attivi oggi

### Verdict del test 1
- giudizio: `parzialmente confermato`
- lettura pratica:
  - per dire `nessuno lo usa / non esiste`, le prove pubbliche vanno nella direzione opposta
  - per dire `ha adoption reale`, le prove sono ancora troppo leggere

## 2. Tracce onchain o metriche attribuibili al prodotto
### Cosa ho trovato
- La docs prodotto e viva e aggiornata su piu superfici:
  - `Getting started` aggiornato `3 mesi fa`
  - `Log in with Web3 Wallet` aggiornato `3 mesi fa`
  - `Video Tutorials` aggiornata `11 mesi fa`
  - `Integrated protocols` aggiornata `ultimo mese`
  - `Anon token` aggiornata `2 mesi fa`
- La docs `Integrated protocols` mostra una superficie funzionale ampia:
  - `15` reti EVM
  - `2` non-EVM
  - quindi `17` reti totali dichiarate
- La docs `Contracts` pubblica gli indirizzi `OFT_V2` di `ANON` su piu chain, incluso `Ethereum`, `Base`, `Arbitrum`, `BSC`, `Sonic`, `Solana`, `Hyperliquid`
- La docs `Hyperliquid builder code` descrive una fee performance-based `10 bps` sulle chiusure profittevoli, con settlement nativo del builder code
- Il forum DAO ha attivita pubblica recente:
  - `RFC #5` attiva ad `aprile 2026`
  - `RFC #3` ancora visibile con `23 replies` e `~1,191 views`
  - `RFC #2` con `13 replies` e `~4,285 views`
- Il GitHub `RealWagmi` mostra repo pubblici collegati, inclusi:
  - `heyanon-sdk`
  - `anon-integration-guide`
  - `heyanon-tokenlist`
  - con aggiornamenti pubblici visibili fino a `settembre-novembre 2025`

### Cosa dimostra davvero
- Dimostra che:
  - esiste una base di prodotto / documentazione / integrazione reale
  - esistono artefatti pubblici coerenti con un team che ha effettivamente costruito qualcosa
  - il progetto non e solo una promessa generica senza superficie tecnica

### Cosa non sono riuscito a trovare
- non ho trovato una dashboard pubblica e pulita con:
  - `DAU / MAU`
  - numero di prompt
  - numero di wallet attivi
  - volume instradato
  - numero di transazioni eseguite via HeyAnon
  - fee generate dal prodotto
  - revenue della HUD / builder
  - referral payouts aggregati
- non ho trovato una prova onchain semplice e pubblica che isoli:
  - `queste transazioni sono state eseguite via HeyAnon`
  - `questi fee flows sono entrati al progetto grazie a HeyAnon`

### Implicazione analitica
- Qui sta il buco decisivo:
  - c e `proof-of-build`
  - non c e `proof-of-usage-at-scale`
  - e soprattutto non c e `proof-of-economics`

### Verdict del test 2
- giudizio: `debole / non chiuso con rigore pieno`
- lettura pratica:
  - il prodotto lascia tracce pubbliche di costruzione e manutenzione
  - non lascia ancora tracce pubbliche abbastanza forti di utilizzo economico misurabile

## 3. Prove che `ANON` catturi davvero qualcosa oltre alla narrativa
### Cosa ho trovato
- La docs `Anon token` dice che `ANON` offre:
  - governance
  - accesso gratuito o scontato ai servizi AI
  - supporto treasury per accesso gratuito, talent, compute e grants
- `RFC #2` descrive una architettura in cui:
  - si stakea `ANON` per ottenere `ANONs`
  - esistono pass di accesso
  - l uso oltre i limiti free o pass puo essere pagato in `ANON`
  - ci sono fee di staking e penalty mechanics
- `RFC #3` dice che una frazione delle referral fees HUD da fonti come `Hyperliquid`, `Axiom`, `Photon`, `gmgn` dovrebbe essere instradata verso value accrual per holder `ANON`
  - con opzioni tipo `buyback & burn`
  - `xANON staking`
  - referrals
  - treasury share
- `RFC #3` e molto chiara su un punto:
  - vuole `formalize` come la revenue venga instradata ai token holders
  - quindi il testo stesso implica che la formalizzazione / implementazione non fosse ancora una meccanica chiusa e pienamente verificata al momento della proposta

### Cosa dimostra davvero
- Dimostra che il progetto ha almeno pensato un ponte `product -> token` non banale.
- Dimostra anche che qualche sorgente di fee del prodotto e concettualmente reale:
  - performance fee Hyperliquid via builder code
  - referral revenue HUD su venue integrate

### Cosa non dimostra
- non dimostra che oggi esista pubblicamente:
  - buyback live verificabile
  - burn live verificabile
  - `xANON` operativo con backing osservabile
  - dashboard di revenue streaming verso holder
  - quota di usage effettivamente pagata in `ANON`
  - dati pubblici su ANON speso per query, pass o transazioni

### Implicazione analitica
- Il token ha `design optionality`.
- Non ha ancora `proof of capture` abbastanza forte da poter dire:
  - `ANON` cattura valore in modo gia dimostrato oltre la narrativa

### Verdict del test 3
- giudizio: `non confermato`
- lettura pratica:
  - la token capture esiste piu come roadmap / governance design / meccanica proposta che come reality check pubblico gia osservabile

## Mappa finale dei 3 test
- `prove pubbliche che persone reali lo usino davvero`
  - esito: `parzialmente si`
  - forza della prova: `media`
  - motivo: `Chrome Web Store 1,000 users + 24 ratings` e onboarding pubblico concreto
- `tracce onchain o metriche che mostrino attivita attribuibile al prodotto`
  - esito: `deboli`
  - forza della prova: `bassa`
  - motivo: esistono docs, contratti e repo, ma non una telemetry pubblica credibile di usage e fee
- `prove che ANON catturi davvero qualcosa oltre alla narrativa`
  - esito: `non provato`
  - forza della prova: `bassa`
  - motivo: molta architettura proposta, poca evidenza live misurabile

## Risposta pratica alla domanda `molto early` vs `molto raccontato`
- `HeyAnon` non e abbastanza vuoto da liquidarlo come semplice sito senza prodotto.
- Ma non e neanche abbastanza trasparente da meritare oggi la lettura `prodotto gia validato, token solo ignorato dal mercato`.
- La sintesi piu utile e:
  - `molto costruito`
  - `solo parzialmente visibile`
  - `non ancora provato pubblicamente nella traction`
  - `token capture ancora soprattutto raccontata`

## Cosa servirebbe per promuoverlo da `raccontato` a `provato`
- una dashboard pubblica con:
  - utenti attivi
  - prompt / task eseguiti
  - wallet connessi
  - volume instradato
  - fee generate
  - referral revenue
- una prova pubblica di token capture live:
  - buyback
  - burn
  - `xANON`
  - ANON speso per accesso o usage
- una metrica pubblica e verificabile che leghi il prodotto a un cash flow osservabile

## Conclusione netta
- verdict del proof-of-life:
  - `prodotto esistente: si`
  - `utenti pubblicamente dimostrati: un po`
  - `traction economica pubblicamente dimostrata: no`
  - `ANON value capture pubblicamente dimostrata: no`
- motivo principale:
  - la migliore evidenza trovata dimostra che HeyAnon esiste davvero come prodotto e distribuzione software, ma non che abbia gia una traction pubblica forte o un meccanismo di token accrual live abbastanza verificabile da giustificare una tesi bullish strutturale sul solo `proof-of-life`
