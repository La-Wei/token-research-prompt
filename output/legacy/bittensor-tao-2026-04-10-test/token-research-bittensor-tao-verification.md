# Verification Audit

## Data di verifica
- Protocollo / ticker verificato: `Bittensor / TAO`
- Report verificato: `bittensor-tao-2026-04-10-test/token-research-bittensor-tao-test.md`
- Prompt base di riferimento: `token-research-prompt.md`
- Data di verifica: `2026-04-10`
- Approccio: verifica di claim strutturali, waterfall, supply, emissions, governance, market data live ed eventi recenti usando docs ufficiali, governance ufficiale, filing SEC, dashboard metodologicamente chiare e reporting giornalistico serio dove la fonte primaria diretta non era disponibile

## Esito sintetico
- Esito generale: `ampiamente confermato con poche correzioni e con una rifinitura metodologica residua`
- Il cuore del report regge: `TAO` appare come asset-base del network con `value accrual indiretto`, non come token con cash flow diretto verso gli holder.
- Le sezioni migliori sono quelle su `waterfall`, `recycling vs burn`, `source reconciliation` della supply, `governance discount` e `recent event audit`.
- Non ho trovato errori materiali sul fatto che:
  - Bittensor sia un mercato a subnet con staking / riserve / alpha locali
  - le fee di chain siano `recycled`, non revenue distribuita agli holder
  - il burn documentato nel materiale ufficiale riguardi soprattutto `alpha`, non il base token `TAO`
  - il setup di mercato sia oggi `fragile`
- Le due correzioni metodologiche che restano sono:
  - lo stato esatto di `BIP-023` non e chiuso con rigore pieno, perche la pagina ufficiale mostra metadati temporali internamente incoerenti
  - nel cappello iniziale del blocco eventi conviene separare ancora piu nettamente `fatto confermato` e `allegation`

## Fonti usate per la verifica
- https://docs.learnbittensor.org/subnets/understanding-subnets/
- https://docs.learnbittensor.org/learn/emissions
- https://docs.learnbittensor.org/staking-and-delegation/delegation
- https://docs.learnbittensor.org/staking-and-delegation/root-claims
- https://docs.learnbittensor.org/resources/glossary
- https://docs.learnbittensor.org/governance/
- https://docs.learnbittensor.org/governance/senate
- https://docs.learnbittensor.org/concepts/stake-burn
- https://docs.learnbittensor.org/subnets/create-a-subnet
- https://vote-bittensor.xyz/
- https://huggingface.co/1Covenant/Covenant72B
- https://www.coingecko.com/en/coins/bittensor
- https://www.coinglass.com/currencies/TAO
- https://defillama.com/chain/bittensor
- https://defillama.com/revenue/chain/bittensor
- https://www.grayscale.com/funds/grayscale-bittensor-trust
- https://www.sec.gov/Archives/edgar/data/2029297/000119312526104209/tao-20251231.htm
- https://www.theblock.co/post/396959/covenant-ai-exits-bittensor-tao/
- https://www.theblock.co/post/397028/bittensor-co-founder-denies-suspending-subnet-emissions-after-covenant-ai-exit
- https://www.theblock.co/post/395730/bittensor-fuels-ai-token-rally-distributed-training-gains-credibility/

## Eventi recenti verificati
- `Evento confermato`
  - `2026-03-09 / 2026-03-10`: la model card di `Covenant-72B` conferma `72B` parametri, `1.1T` token di training, `20+` participant compute su Bittensor e benchmark `MMLU 67.11`.
  - `2026-03-22`: la pagina governance `BIP-023` conferma l esistenza della proposta per cambiare lo split emissioni da `41 / 41 / 18` a `38 / 44 / 18`.
  - `2026-04-09`: `The Block` conferma che `Covenant AI` annuncia l uscita da Bittensor.
  - `2026-04-10`: `The Block` conferma che `Jacob Steeves` nega di poter sospendere le subnet emissions e risponde alle accuse.
  - `2026-04-10`: il mercato reagisce in modo violento. CoinGecko mostra `TAO ~$267.02`, `-17.90%` 24h, `24h vol ~$1.816B`. CoinGlass mostra `futures vol ~$3.79B`, `spot vol ~$592.22M`, `OI ~$461.97M`, `liq 24h ~$12.03M`.

- `Allegation o claim non dimostrato`
  - il merito fattuale completo delle accuse Covenant su sospensione emissions, controllo effettivo del `Triumvirate`, deprecazione unilaterale dell infrastruttura e uso punitivo delle vendite di token non e chiuso con prova primaria completa nelle fonti aperte usate
  - e confermata l esistenza delle accuse; non e confermato integralmente che ogni accusa sia vera nel merito

- `Risposta del team / fonte primaria o quasi primaria`
  - `The Block` riporta che Steeves ha negato esplicitamente di poter sospendere le emissions
  - le docs ufficiali di governance continuano comunque a mostrare che il `Triumvirate` e composto da dipendenti della `Opentensor Foundation`, quindi il `governance discount` resta giustificabile anche senza provare tutte le accuse Covenant

- `Market reaction osservata`
  - prezzo: forte selloff intraday / 24h
  - volume: molto elevato su CoinGecko e CoinGlass
  - derivati: `OI ~$461.97M`, `liquidations 24h ~$12.03M`
  - giudizio: l evento ha impattato chiaramente `fiducia + market structure`, non solo la narrativa

## Confermato
- `Descrizione del protocollo`: confermata. Le docs ufficiali definiscono il subnet come `incentive-based competition marketplace` e spiegano che l incentive mechanism puo vivere offchain nel repository del subnet creator.
- `Ruolo economico di TAO`: confermato. Le docs su staking/delegation e root claims supportano il fatto che `TAO` sia l asset-base usato per staking nel root, accesso economico ai subnet e conversione dei dividendi root.
- `Flow-based emissions / net inflows`: confermato. Le docs ufficiali dicono che il modello attivo dal novembre 2025 basa le emissioni sui `net TAO inflows` e che i subnet con flussi negativi possono arrivare a `zero emissions`.
- `Waterfall del base layer`: confermato in senso strutturale. Il report ha ragione nel dire che il base token non ha `buyback hard-coded`, `revenue share` diretta o burn permanente documentato alimentato dalle fee del protocollo.
- `Fees e recycling`: confermato. Il glossario ufficiale dice che tutte le transaction fees sono `recycled`, che le subnet creation fees sono riciclate tranne `1 TAO` usato per inizializzare la pool, e che i token riciclati possono essere emessi di nuovo.
- `Burn`: confermato. La documentazione sul `subnet stake burn` mostra che il meccanismo rimuove `alpha` dalla circolazione mentre `TAO` entra nella reserve del subnet; questo supporta bene la distinzione del report tra burn di alpha e mancata prova di burn netto materiale del base token.
- `Governance structure`: confermata. Le docs ufficiali dicono che il `Triumvirate` propone, il `Senate` approva, e che i membri del `Triumvirate` sono dipendenti della `Opentensor Foundation`.
- `No direct TAO holder revenue`: confermato in senso analitico. Non emerge un meccanismo semplice `protocol revenue -> TAO holder revenue`; il `10-K` Grayscale aggiunge anche che il possesso di TAO non conferisce diritti di governance diretti.
- `Supply divergence`: confermata. La divergenza `CoinGecko ~9.6M` vs `CoinGlass/TAO.app ~10.82M` e reale e supporta la sezione `source reconciliation`.
- `Holder concentration`: confermata. Il `10-K` SEC dice che al `2025-12-31` i `100` wallet piu grandi detenevano `~54%` del TAO in circolazione, mentre il trust deteneva `~0.3%`.
- `Grayscale wrapper`: confermato. Esiste il veicolo `GTAO` e il `10-K` conferma reporting SEC pieno sul trust.
- `Covenant-72B come prova tecnica`: confermato. La model card Hugging Face supporta bene il fatto che almeno un subnet abbia prodotto un artefatto tecnico reale e non banale.
- `Market setup fragile`: confermato. Dopo il caso Covenant, il giudizio `fragile` e oggi il piu corretto del report.

## Da correggere o aggiornare
- `BIP-023 stato live`: da rendere piu cauto. Il report lo tratta come `Active - Voting Open` nello snapshot iniziale e come evento `in evoluzione` nelle linee `64-67` e `362-373`. Il contenuto della proposta e confermato, ma la stessa pagina ufficiale mostra una contraddizione tra:
  - timeline testuale `March 22 - April 1, 2026`
  - `April 8, 2026` come effective block stimato
  - stato live `Voting Open` con countdown ancora attivo
  Quindi lo `status` va trattato come `non chiuso con rigore pieno`, non come stato live pienamente affidabile.
- `Cappello iniziale del blocco eventi`: da rifinire leggermente. Nelle linee `332-337` il report mette nello stesso cappello il fatto dell exit Covenant e il contenuto accusatorio. Il blocco per-evento dopo, invece, e gia buono. Conviene solo riallineare il cappello iniziale alla tassonomia piu rigorosa.
- `Metriche live`: da aggiornare se il report viene riusato oltre il `2026-04-10`. Rispetto ai numeri scritti nelle linee `42-67` e `295-299`, le metriche live sono gia intraday-volatile.

## Parzialmente confermato, ma non chiuso con rigore pieno
- `Emission run-rate corrente`: il report gestisce bene la divergenza, ma il punto resta solo parzialmente chiuso. La doc `glossary` dice `0.5 TAO every 12 seconds`, mentre la pagina `halving` consultata in passato usa ancora la formulazione `~7,200 -> ~3,600 after first halving`. La conclusione del report e prudente, ma la fonte ufficiale non e perfettamente sincronizzata.
- `Nessun classico calendario VC unlock visibile`: plausibile e ben formulato, ma non e una prova assoluta su tutta la holder map e sulla distribuzione originaria. Vale come giudizio prudente, non come chiusura totale.
- `Treasury opacity / foundation control`: condivido il rischio, ma resta parzialmente chiuso. Le docs e il filing SEC non danno una disclosure operativa completa di foundation wallets, reserves e capital allocation interna.
- `Business monetization`: il report ha ragione a dire che la monetizzazione aggregata dei subnet e ancora opaca. Allo stesso tempo, la lettura `DefiLlama TVL $0 / revenue bassa` va sempre interpretata come metrica di perimetro limitato, non come misura totale dell attivita economica del network.
- `Covenant shock gia prezzato o no`: il report lo tratta come `parzialmente prezzato`, il che e ragionevole; ma questa resta necessariamente una stima analitica, non un fatto verificabile.
- `Event audit 30d / 90d`: buono sullo shock negativo, meno chiuso sul rally precedente. `The Block` il `2026-04-02` scrive che `TAO nearly doubled in March`, quindi il contesto di euforia precedente esiste davvero e spiega parte della violenza del repricing.

## Valutazione del giudizio finale
- `Business quality: media`: confermato. Il report non sopravvaluta Bittensor come se avesse gia dimostrato PMF AI finale ampio e monetizzato.
- `Necessita di esistenza del prodotto: media`: confermata. Il vantaggio concreto c e soprattutto come coordination layer per operatori, staker e builder, piu che come prodotto consumer chiaramente superiore.
- `Token quality: media`: confermato. TAO e migliore della media di molti AI token per ruolo economico e profilo supply, ma l accrual resta indiretto.
- `Market setup: fragile`: confermato e rafforzato dagli eventi del `2026-04-09` e `2026-04-10`.
- `Verdict: fairly priced`: ancora difendibile. Il selloff ha gia reintrodotto un governance discount materiale, ma non vedo ancora un edge forte da token chiaramente sottovalutato.
- `Confidenza del giudizio: media-bassa`: confermata. E il livello giusto dato il mix di sostanza tecnica, opacita monetaria e governance dispute aperta.

## Sintesi finale
- Il report fondamentale su `Bittensor / TAO` e complessivamente solido e coerente con il prompt aggiornato.
- Le sue tesi principali risultano confermate:
  - `TAO` come asset-base con accrual indiretto
  - nessun cash flow diretto pulito agli holder
  - supply non chiaramente deflattiva
  - governance discount reale
  - market setup oggi fragile
- La principale rifinitura da tenere a mente non riguarda il nucleo della tesi ma due dettagli di rigore:
  - stato live di `BIP-023` da trattare con piu cautela
  - separazione ancora piu netta tra `evento confermato` e `allegation` nel cappello iniziale degli eventi
- Il giudizio finale `fairly priced` con `market setup fragile` e `confidenza media-bassa` resta il piu rigoroso anche dopo la verifica.
