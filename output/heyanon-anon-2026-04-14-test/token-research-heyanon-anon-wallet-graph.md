# Wallet Graph Audit: `HeyAnon / ANON`

## Data audit
- Data audit: `2026-04-14`
- Obiettivo:
  - mappare i nodi wallet / contract pubblicamente identificabili di `HeyAnon`
  - capire se emergono pattern credibili di treasury, buyback, distribuzione o sell pressure
  - capire se il grafo pubblico supporta una tesi `proof-of-economics` oppure resta troppo sparso

## Esito sintetico
- grafo wallet pubblico identificabile: `molto incompleto`
- nodi certi trovati: `pochi ma reali`
- prove di treasury / fee sink pubblicamente riconciliabili: `non trovate`
- prove di buyback / burn / reward distribution: `non trovate`
- pattern dominante emerso:
  - `token infrastructure cross-chain`
  - non `product revenue graph`
- giudizio netto:
  - il wallet graph pubblico oggi non mostra uno schema chiaro di cattura valore per `ANON`
  - mostra soprattutto un token LayerZero distribuito su piu chain con un deployer / delegate attivo e alcune tracce di bridging

## Fonti usate
- Docs contratti:
  - https://docs.heyanon.ai/heyanon.ai/general-information/contracts
- Docs prodotto:
  - https://docs.heyanon.ai/heyanon-v2/readme/getting-started/account-settings
  - https://docs.heyanon.ai/heyanon-v2/readme/getting-started/log-in-with-web3-wallet
  - https://docs.heyanon.ai/heyanon.ai/hud/hyperliquid-builder-code
- Explorer / labels:
  - https://etherscan.io/token/0x79bbf4508b1391af3a0f4b30bb5fc4aa9ab0e07c
  - https://bscscan.com/address/0x79bbf4508b1391af3a0f4b30bb5fc4aa9ab0e07c
  - https://arbiscan.io/token/0x79bbF4508B1391af3A0F4B30bb5FC4aa9ab0E07C
  - https://basescan.org/address/0x8054a4fbd093808af4529187d3efb9f6301ab92f
  - https://sonicscan.org/address/0x8054A4fBd093808AF4529187D3Efb9F6301ab92f

## 1. Nodi pubblici che possiamo attribuire con buona confidenza
### Nodo A: `ANON token contract`
- indirizzo EVM pubblicato ufficialmente:
  - `0x79bbF4508B1391af3A0F4B30bb5FC4aa9ab0E07C`
- la docs `Contracts` lo riporta sulle principali chain EVM supportate:
  - `Ethereum`
  - `Kava`
  - `Metis`
  - `Base`
  - `IOTA`
  - `Sonic`
  - `Arbitrum`
  - `Avalanche`
  - `BSC`
  - `HyperEVM`
- implicazione:
  - questo e il nodo piu certo dell intero grafo pubblico
  - ma e il nodo del token, non necessariamente quello dell economics del prodotto

### Nodo B: `deployer / delegate`
- address ricorrente nei constructor args del token:
  - `0x8054A4fBd093808AF4529187D3Efb9F6301ab92f`
- gli explorer lo mostrano come:
  - `_delegate` del token `OFT`
  - `Contract Creator` del contratto
  - `Hey Anon: Deployer` su `SonicScan`
- implicazione:
  - e il secondo nodo certo del grafo
  - e il principale punto pubblico di controllo / configurazione del token cross-chain

### Nodo C: `Solana OFT stack`
- la docs `Contracts` pubblica anche:
  - `programId`
  - `mint`
  - `mintAuthority`
  - `escrow`
  - `oftStore`
- implicazione:
  - il bridging multichain non e solo dichiarato; la struttura base e effettivamente pubblicata

## 2. Cosa mostrano davvero questi nodi
### Contratto token
- gli explorer mostrano codice verificato minimale:
  - `OFT`
  - `Ownable`
  - nessuna logica nativa evidente di `buyback`, `burn`, `staking`, `reward sharing`, `treasury routing`
- implicazione:
  - il token contract da solo non racconta alcun meccanismo di holder accrual

### Deployer / delegate
- su `SonicScan`, il deployer mostra come ultima azione rilevante:
  - `2026-03-24`
  - metodo `Transfer Ownership`
  - destinazione `Hey Anon: Anon Token`
- interpretazione prudente:
  - sembra esserci stato un passaggio di ownership o controllo verso il token contract stesso
  - questo puo ridurre il rischio di admin abuse diretto sul token
  - ma non dimostra nulla su revenue, treasury o tokenholder accrual

### Portfolio snapshot dei nodi pubblici
- gli snapshot explorer visibili per il deployer non mostrano una grossa treasury operativa in `ANON`
- gli snapshot visibili per il token contract mostrano solo piccoli saldi residui multi-chain
  - per esempio, nello snapshot crawl visibile da `BscScan`, il contract address aveva un portfolio multichain di poche migliaia di dollari e circa `~3,905 ANON` su `Sonic`
- implicazione:
  - non emerge un grande `treasury wallet` palese direttamente leggibile dai nodi pubblici che abbiamo

## 3. Tracce di flusso che sembrano reali
### Bridging / OFT activity
- su `Etherscan` compaiono transazioni con eventi:
  - `OFTReceived`
  - `PacketDelivered`
- esempi osservabili nei risultati explorer:
  - tx `0x5afbd5500bb6dd949e06f5428747908b0060f7aac4bd760fdaa4d99558b5e01e`
    - ricevente: `0x49719D256A5eA16bFa579ea16E95bea9fa41A452`
    - `amountReceivedLD`: `210.506758 ANON`
  - tx `0x7761caf4d2e6991a2452fe1a1c5a41724d8021b97b73d0c2da7fce16ae6733a2`
    - ricevente: `0x3d126d6B1581f7566a34bD4e912920bBA41367D5`
    - `amountReceivedLD`: `313.211587 ANON`
  - tx `0x3de46aec4ea550abc3a8dee98bc3ab602fa5139d331ce824601ca5b40641a905`
    - ricevente: `0xAFF53fB46d0B10C90b3ef5C29Df101C661e05620`
    - `amountReceivedLD`: `50.644959 ANON`
- implicazione:
  - il token si muove davvero cross-chain
  - ma questo prova soltanto infrastruttura di bridging e distribuzione
  - non prova uso del prodotto HeyAnon

### Attivita del token su piu chain
- snapshot explorer osservati:
  - `Ethereum`:
    - `1,254 holders`
    - supply locale `~325,475 ANON`
  - `Arbitrum`:
    - `857 holders`
    - supply locale `~160,905 ANON`
  - `BSC`:
    - `388 holders`
    - supply locale `~87,350 ANON`
  - `Base`:
    - `77,102 holders`
    - supply locale `~1,074,704 ANON`
- implicazione:
  - esiste una distribuzione / frammentazione cross-chain reale del token
  - ma holder count e local supply non bastano da soli a identificare treasury, insiders o utenti prodotto

## 4. Nodi che ci aspetteremmo di trovare se esistesse economics trasparente
### Non trovati pubblicamente in modo chiaro
- `builder address` HeyAnon per `Hyperliquid`
- wallet treasury ufficiale e riconciliato
- wallet fee sink ufficiale e riconciliato
- contract `xANON`
- contract / module di `buyback`
- contract / module di `burn`
- contract / module di `reward distribution`
- address pubblici per incasso `referral revenue`

### Implicazione analitica
- Se questi nodi esistono ma non sono pubblici, il progetto puo comunque funzionare.
- Ma da investitore questo significa:
  - non posso costruire un grafo di accrual serio
  - non posso verificare buyback o burn
  - non posso misurare il ponte `product fees -> token`

## 5. Pattern di rischio / pressione vendita
### Cosa possiamo dire
- non emerge un mega-wallet pubblico ovvio che sembri una treasury gigantesca sul set di nodi identificati
- non emerge neppure un wallet pubblico ovvio che sembri `buyback sink`
- il deployer non appare, dagli snapshot visibili, carico di una grossa inventory `ANON`

### Cosa non possiamo dire
- non possiamo dire con rigore:
  - chi siano i top holders reali
  - dove sieda la vera treasury
  - quanta supply sia exchange-held
  - quanta supply sia ancora controllata da insiders o partnership wallets
- quindi:
  - il rischio di overhang non e eliminato
  - semplicemente non e chiuso dal grafo pubblico

## 6. Mini grafo pubblico ricostruibile
```text
HeyAnon Docs
  -> pubblicano token contract OFT_V2
  -> pubblicano deployer/delegate
  -> pubblicano Solana OFT stack
  -> non pubblicano fee wallets / treasury / builder address

Deployer / Delegate 0x8054...ab92f
  -> deploy/config del token cross-chain
  -> transfer ownership verso token contract su Sonic
  -> nessuna prova pubblica di treasury operativa ampia

ANON Token Contract 0x79bb...0E07C
  -> OFT cross-chain
  -> holders e transfers su piu chain
  -> eventi OFTReceived visibili
  -> nessuna accrual logic nativa osservabile

Unknown product economics nodes
  -> builder address Hyperliquid
  -> referral wallets
  -> treasury wallets
  -> xANON / buyback / burn / rewards
  -> non pubblicamente riconciliati
```

## 7. Cosa significa per la tesi
- Se il tuo obiettivo era provare che `HeyAnon` sia puro teatro senza nulla dietro, questo audit non lo dimostra.
- Se il tuo obiettivo era trovare un wallet graph chiaro che provi `ANON value capture`, questo audit fallisce.
- La conclusione seria e intermedia:
  - il grafo pubblico prova `token infra`
  - non prova `product economics`
  - e non prova `holder accrual`

## Checklist finale
- cose confermate:
  - token e deployer esistono davvero
  - il token si muove cross-chain via LayerZero
  - c e stata almeno una manutenzione / ownership action recente il `2026-03-24`
- cose non confermate:
  - treasury pubblica e leggibile
  - revenue wallet leggibile
  - buyback / burn
  - value capture verso `ANON`
- segnale pratico piu importante:
  - il wallet graph oggi non ti da edge bullish; ti da soprattutto visibilita sui limiti della trasparenza

## Conclusione netta
- verdict del wallet graph:
  - `grafo pubblico reale ma troppo sparso`
- motivo principale:
  - i nodi certi che vediamo riguardano quasi tutti l infrastruttura del token cross-chain, mentre i nodi che servirebbero per provare economics del prodotto e cattura di valore del token restano opachi o non pubblicati
