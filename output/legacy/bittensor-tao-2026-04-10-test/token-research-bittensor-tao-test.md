# Test Prompt: `token-research-prompt.md`

## Input usato
- `[NOME/TICKER]`: `Bittensor / TAO`
- Data snapshot principale: `2026-04-10`
- Obiettivo del test: eseguire il prompt aggiornato con focus esplicito su waterfall economico, source reconciliation e recent event audit

## Materiale minimo per l'analisi

### Fonti principali
- Bittensor Docs:
  - https://docs.learnbittensor.org/subnets/understanding-subnets
  - https://docs.learnbittensor.org/learn/emissions
  - https://docs.learnbittensor.org/staking-and-delegation/delegation
  - https://docs.learnbittensor.org/staking-and-delegation/root-claims
  - https://docs.learnbittensor.org/learn/fees
  - https://docs.learnbittensor.org/resources/glossary
  - https://docs.learnbittensor.org/governance
  - https://docs.learnbittensor.org/concepts/halving
  - https://docs.learnbittensor.org/concepts/stake-burn
  - https://docs.learnbittensor.org/subnets/create-a-subnet
  - https://docs.learnbittensor.org/learn/announcements
- TAO.app:
  - https://www.tao.app/metrics
  - https://www.tao.app/tokenomics
- Market data:
  - https://www.coingecko.com/en/coins/bittensor
  - https://www.coinglass.com/currencies/TAO
- Governance:
  - https://vote-bittensor.xyz/
- Recent business proof:
  - https://huggingface.co/1Covenant/Covenant-72B
- Recent event reporting:
  - https://www.theblock.co/post/396959/covenant-ai-exits-bittensor-tao/
  - https://www.theblock.co/post/397028/bittensor-co-founder-denies-suspending-subnet-emissions-after-covenant-ai-exit
- Institutional wrapper / ownership context:
  - https://www.grayscale.com/funds/grayscale-bittensor-trust
  - https://www.sec.gov/Archives/edgar/data/2029297/000119312526104209/tao-20251231.htm
- Metric perimeter cross-check:
  - https://defillama.com/chain/bittensor
  - https://defillama.com/revenue/chain/bittensor

### Snapshot numerico essenziale
- `CoinGecko` snapshot `2026-04-10`:
  - prezzo `~$262.89`
  - market cap `~$2.52B`
  - FDV `~$5.51B`
  - 24h volume `~$1.38B`
  - circulating supply `9,597,491 TAO`
  - total / max supply `21,000,000 TAO`
  - performance `24h -22.6%`, `7d -15.2%`, `30d +30.9%`
  - ATH `~$757.60` il `2024-03-07`
- `TAO.app` snapshot `2026-04-10`:
  - prezzo `~$263.88`
  - market cap `~$2.86B`
  - FDV `~$5.54B`
  - circulating supply `10.82M TAO`
  - `Root TAO 5,251,804`
  - `% TAO in Subnets 18.10%`
  - `% TAO on Root 47.91%`
  - `% TAO on Wallets 33.99%`
  - `Keep Addresses 666`
  - `Root TAO (Keep) 193,617`
- `CoinGlass` snapshot `2026-04-10`:
  - prezzo `~$264.47`
  - futures volume 24h `~$3.78B`
  - spot volume 24h `~$578.36M`
  - open interest `~$451.73M`
  - circulating supply `10.82M`
- `DefiLlama` snapshot `2026-04-10`:
  - chain TVL `~$0`
  - chain app fees / revenue 24h `~$17,027`
  - chain revenue 30d `~$465,257`
- `Governance`:
  - `BIP-023` proposta il `2026-03-22`
  - status visto nella pagina consultata: `Active - Voting Open`
  - split proposto: `41 / 41 / 18 -> 38 / 44 / 18`
- `Covenant-72B`:
  - paper / model card pubblicati a marzo 2026
  - `72B` parametri
  - `1.1T` token di training
  - `20+` participant compute nella model card
  - `MMLU 67.11`
- `Grayscale Bittensor Trust`:
  - ticker `GTAO`
  - veicolo pubblico e oggetto di reporting SEC nel `2025-2026`
- `SEC 10-K`:
  - al `2025-12-31` il trust deteneva `~0.3%` del TAO in circolazione
  - i `100` wallet piu grandi detenevano `~54%` del TAO in circolazione

### Punti che restano parzialmente opachi
- non esiste una disclosure semplice e consolidata del `waterfall` economico del base token oltre alle fee di chain
- non ho una mappa aggiornata completa di holder concentration, borrow cost, funding e short availability
- la supply live diverge in modo materiale tra `CoinGecko` e `TAO.app/CoinGlass`
- la documentazione sull halving non appare perfettamente sincronizzata in tutti i punti
- le accuse Covenant AI su governance e poteri del founder restano solo parzialmente verificabili con fonti primarie aperte

---

# Output del prompt

Research status
- qualita delle fonti: `alta-media`
- copertura dati: `parziale ma sufficiente per un giudizio strutturale`
- principali buchi informativi: revenue esterna aggregata dei subnet, holder map aggiornata, market structure derivata completa
- rischio principale di errore analitico: sopravvalutare il nesso tra successo di alcuni subnet e value accrual del base token TAO
- confidenza preliminare: `media`

## 1. TL;DR iniziale
Fatti verificabili:
- Bittensor e un network a subnet dove `TAO` e l asset-base usato per staking, accesso economico ai subnet e coordinamento del capitale.
- Il protocollo ha prodotto almeno una prova tecnica reale nel periodo recente con `Covenant-72B`, ma il base token non ha `cash flow` diretto verso gli holder.
- Il mercato ha appena prezzato un forte `trust shock` di governance dopo l uscita di `Covenant AI`, con crollo `double digit`, volumi altissimi e leva in unwind.

Inferenze ragionevoli:
- Il business e piu interessante del token letto in modo isolato: Bittensor puo avere senso come `coordination layer` AI anche se TAO non cattura valore in modo pulito come un equity-like asset.
- Il mercato tende a sbagliare in due direzioni: o tratta TAO come AI winner inevitabile, o lo liquida come puro token narrativo. La realta sta nel mezzo.

Speculazioni:
- Se i subnet dimostrano output ripetibili e la governance si apre davvero, TAO puo ancora reratare.
- Se la frattura Covenant diventa il sintomo di un controllo troppo concentrato, il discount di governance si allarga ancora.

Giudizio preliminare:
- business non banale, token con accrual `indiretto`, setup di mercato oggi `fragile`; ai prezzi correnti lo leggo piu come `fairly priced` che come disallineamento evidente.

## 2. Che cosa fa davvero il protocollo
Fatti verificabili:
- Bittensor definisce ogni subnet come un `incentive-based competition marketplace` che produce una commodity digitale legata all AI.
- Ogni subnet ha un AMM interno con `TAO reserve` e `alpha reserve`; quando l utente stakea TAO in un subnet, mette TAO nella riserva e riceve alpha.
- Il `Root Subnet` e il subnet speciale senza alpha proprio, dove si puo stakeare TAO direttamente ai validator.
- La governance ufficiale dichiara esplicitamente una transizione graduale da gestione centralizzata a community ownership, ma oggi il `Triumvirate` resta composto da membri della `Opentensor Foundation`.

Inferenze ragionevoli:
- Il prodotto non e principalmente una AI app consumer. E un mercato tokenizzato di incentivi, capitale e ranking per subnet AI.
- Il vero vantaggio onchain non e la UX per l utente finale; e il coordinamento permissionless tra miner, validator, staker e subnet creator.
- Se togli il token, gran parte del livello di incentivo, staking, ranking economico e discovery di capitale peggiora molto. Se togli la blockchain ma tieni solo le app AI finali, alcune app potrebbero continuare a esistere.
- Il vantaggio contro una soluzione centralizzata non e "miglior prodotto per tutti"; e "mercato aperto di partecipazione e capitale" per operatori che accettano complessita maggiore.

Speculazioni:
- Se i subnet diventano veri mercati di servizi AI con domanda esterna ripetibile, la necessita del layer crypto aumenta.
- Se invece restano soprattutto luoghi in cui il capitale specula sulle alpha locali, il protocollo rischia di restare piu mercato interno che prodotto necessario.

Mini verdict atomico
- necessita di esistenza del prodotto: `media`
- vantaggio vs soluzione centralizzata/API: `debole-medio`
- vantaggio vs open source non tokenizzato o locale: `medio` per coordinamento, `debole` per utente finale
- necessita del token per il prodotto: `media`
- il progetto e soprattutto: `coordination layer / mercato tokenizzato`

## 3. Business quality: qualita reale del protocollo
Fatti verificabili:
- La pagina `BIP-023` parla di `64+ active subnets`, quindi il network ha gia una base di subnet non triviale.
- `TAO.app` mostra una distribuzione del capitale dove `47.91%` del TAO e sul root, `18.10%` nei subnet e `33.99%` nei wallet.
- La model card di `Covenant-72B` dimostra che almeno un subnet ha prodotto un artefatto tecnico reale e competitivo su benchmark.
- `DefiLlama` mostra `TVL $0` per la chain e `Revenue 30d ~$465k`, cioe metriche molto piccole rispetto alla market cap del token.

Inferenze ragionevoli:
- La business quality non va giudicata con la lente DeFi classica. `TVL` e `chain revenue` catturano solo una piccola parte del sistema e rischiano di farlo sembrare un business inesistente.
- Allo stesso tempo, non va nemmeno trattato come se avesse gia PMF consumer ampio. La domanda oggi appare molto piu forte tra operatori del network, staker, validator e speculatori AI che tra utenti finali paganti.
- Il punto piu bullish e che esiste prova di output tecnico non banale. Il punto piu cauto e che il network monetizza ancora in modo opaco e frammentato.
- La crescita recente del prezzo sembra aver anticipato una lettura molto ottimista di questi successi tecnici.

Speculazioni:
- Se i subnet piu forti iniziano a mostrare revenue esterna consolidata, il protocollo puo passare da `business quality media` a `medio-alta`.
- Se resta un mercato interno di staking e narrativa AI, la qualita del business non giustifica multipli da winner lineare.

## 4. Unit economics e qualita dei ricavi
Fatti verificabili:
- Le transaction fees di Bittensor includono fee weight/length e fee dello `0.05%` su stake / unstake / move; le docs dicono che queste fee sono `recycled`, non distribuite agli holder.
- Il glossario chiarisce che il recycling riduce `TotalIssuance` ma permette a quella quantita di essere riemessa in futuro.
- La creation fee di un nuovo subnet e anch essa `recycled`, tranne `1 TAO` che inizializza la pool del subnet.
- `DefiLlama` riporta per la chain `Revenue 24h ~$17k` e `Revenue 30d ~$465k`, cioe un numero piccolo su scala token.

Waterfall economico del base token TAO
- `gross user fees`: fee di chain su transazioni e fee da staking / unstaking; costi di subnet creation; eventuali fee locali dei subnet non aggregate in modo pulito per il base token
- `protocol revenue retained`: molto limitata sul base layer; le fee consultate vengono riciclate, non trattenute come cassa disponibile per holder
- `tokenholder revenue / buyback budget / burn budget`: non ho trovato un meccanismo hard-coded di `TAO buyback`, `TAO revenue share` o `TAO burn` permanente alimentato dalle fee del protocollo
- `destinazione finale`: il valore economico oggi scorre soprattutto verso staking dynamics, alpha emissions, subnet economics e coordinamento del capitale, non verso holder revenue lineare in TAO

Inferenze ragionevoli:
- La top-line economicamente osservabile sul base layer e debole se la si misura come chain revenue.
- Il valore del network puo essere reale anche con revenue bassa, ma in quel caso si sta pagando opzionalita, capitale coordinato e domanda di staking, non un business cash-generative nel senso classico.
- Molta della "attivita economica" di Bittensor e interna al sistema: staking, emissioni, alpha pricing, subnet flows. Non va confusa automaticamente con domanda finale per prodotti AI.

Speculazioni:
- Se Bittensor riuscisse a consolidare metriche economiche esterne dei subnet e a legarle al base token, la lettura cambierebbe molto.
- Oggi questa dimostrazione non c e ancora.

## 5. Token: come cattura valore davvero
Fatti verificabili:
- TAO e l asset usato per stakeare ai validator e per entrare economicamente nei subnet.
- Nel `Root Claim`, i dividendi dei root staker possono essere tenuti in alpha o convertiti in TAO e restakati sul root.
- La governance ufficiale conferma che peso, proposals e struttura di potere passano per staking e rappresentanza nel sistema.
- Le docs sul `stake burn` riguardano `alpha` dei subnet, non il base token `TAO`.
- Non ho trovato un fee switch che giri revenue diretta agli holder di TAO, ne buyback sistematici di TAO.

Inferenze ragionevoli:
- Il token riceve valore economico soprattutto in modo `indiretto`: piu capitale vuole esporsi ai subnet o al root, piu TAO viene assorbito nelle riserve e nello staking.
- Questo non equivale a un diritto economico diretto. Il TAO messo in riserva o in staking non sparisce per sempre; puo tornare sul mercato via unstake o rotazione.
- Il bull case del token non e "cash flow verso gli holder", ma "TAO come asset-base scarso che il network deve usare per coordinare la crescita".
- Il rischio centrale e che il business cresca ma il valore si disperda tra alpha locali, operatori, validator e narrativa, senza trasmettersi pienamente al base token.

Speculazioni:
- Se TAO diventasse sempre piu il collaterale universalmente preferito per i subnet e per eventuali prodotti finanziari attorno al network, il suo accrual indiretto si rafforzerebbe.

Claim audit
- claim: `TAO cattura valore`
  - evidenza primaria: staking locale ai subnet, root staking, reserve role, root claims
  - cosa dimostra davvero: TAO e asset-base del network e viene assorbito dal meccanismo economico
  - cosa non dimostra: non dimostra revenue share diretta o cash flow ai token holder
  - giudizio finale: `parzialmente supportata`

- claim: `TAO e deflattivo`
  - evidenza primaria: fee recycle, subnet creation recycle, docs burn riferite soprattutto ad alpha
  - cosa dimostra davvero: esiste recycling che riduce temporaneamente l issuance osservata
  - cosa non dimostra: non dimostra distruzione permanente netta del base token TAO
  - giudizio finale: `non dimostrata`

## 6. Supply, unlock e dilution analysis
Fatti verificabili:
- `CoinGecko` mostra `9,597,491 TAO` di circulating supply e `21M` total/max supply.
- `TAO.app` e `CoinGlass` mostrano `10.82M` di circulating supply.
- Il glossario Bittensor dice che `attualmente 0.5 TAO` vengono mintati ogni `12 secondi`.
- Le docs sulle halving dicono invece `current daily emission ~7,200 TAO -> ~3,600 TAO after first halving`, quindi la documentazione non appare perfettamente sincronizzata.
- Transaction fees e subnet creation fees vengono riciclate e possono ritardare l arrivo delle halving.
- Nelle fonti consultate non emerge un classico calendario di unlock VC mensile come nei token post-TGE tradizionali.

Inferenze ragionevoli:
- Il rischio principale di supply non e un cliff tradizionale, ma una inflation strutturale ancora significativa su una circolante relativamente bassa.
- Se prendo per buono il dato piu aggiornato del glossario, `0.5 TAO` ogni `12 sec` implica `~3,600 TAO/day` e `~1.314M TAO/year`.
- Questo equivale grossolanamente a un inflation run-rate del `~12.1%` se uso `10.82M` di supply, o `~13.7%` se uso `9.60M`.
- Il recycling riduce la pressione netta rispetto alla semplice emissione lorda, ma non basta a rendere TAO chiaramente deflattivo.

Speculazioni:
- Se la percentuale di TAO assorbita stabilmente in root e subnet continua a salire, il mercato potrebbe tollerare meglio l emissione residua.
- Se invece il capitale ruota fuori dai subnet in modo persistente, l inflazione torna piu visibile sul prezzo.

Net supply change
- `unlock`: nessun classico cliff VC visibile nelle fonti consultate
- `emissions`: probabilmente `~3,600 TAO/day` come run-rate piu aggiornato, ma con documentazione non totalmente allineata
- `treasury releases`: non abbastanza trasparenti per una quantificazione seria
- `burned tokens`: nessuna prova forte di burn permanente materiale del base token TAO
- `recycled tokens`: fees e creation fees vengono sottratte da `TotalIssuance` ma sono, per definizione, riemissibili
- conclusione: `supply netta non deflattiva`; e piu corretto parlare di `inflazione moderata da recycling` che di scarsita dura

## 7. Treasury e capital allocation
Fatti verificabili:
- La governance ufficiale non offre una vista semplice e consolidata di `treasury size`, `runway`, `foundation wallets` e potenziale piano di distribuzione.
- Il `Triumvirate` e ancora formato da membri della `Opentensor Foundation`.
- `Grayscale Bittensor Trust` esiste e al `2025-12-31` deteneva `~0.3%` del TAO in circolazione secondo il `10-K`.
- Lo stesso `10-K` segnala che `DCG` e riportata come uno dei maggiori holder di TAO.

Inferenze ragionevoli:
- Qui il rischio non e il runway operativo di breve. E la trasparenza della capital allocation e il potere effettivo della governance.
- Anche senza provare tutte le accuse Covenant, il semplice fatto che la governance resti in una fase di transizione giustifica un `governance discount`.
- La presenza di wrapper istituzionali e positiva per la legittimazione del token, ma non risolve il tema di controllo economico interno.

Speculazioni:
- Una disclosure piu chiara di wallets, foundation reserves e criteri di spesa potrebbe essere un catalizzatore di rerating.
- L opacita persistente, al contrario, rende ogni drama di governance piu costoso per il prezzo.

## 8. Posizionamento competitivo
Fatti verificabili:
- Bittensor si presenta come mercato decentralizzato per commodity AI, non come singola app AI verticale.
- `Covenant-72B` dimostra che almeno un subnet ha raggiunto un output competitivo nel training distribuito.
- Le migliori alternative per l utente finale restano spesso centralizzate: API tradizionali, cloud GPU e modelli open source serviti da terzi o in locale.

Inferenze ragionevoli:
- Il competitor diretto non e solo un altro token AI. E qualsiasi sistema che coordina compute, modelli, ranking o distribuzione in modo piu semplice.
- Per l utente finale, una API centralizzata ben funzionante spesso resta superiore per UX, affidabilita e procurement.
- Per operatori, staker e builder, Bittensor ha un vantaggio diverso: coordinamento aperto del capitale e dell incentivo. Questo e il suo vero posizionamento.
- Quindi il protocollo non vince per superiorita di prodotto consumer. Vince, se vince, come `mercato di coordinamento` difficilmente replicabile senza un asset-base comune.

Speculazioni:
- Se il network continua a produrre subnet tecnicamente credibili e crea una reputazione forte per discovery di talenti e capitale AI, il vantaggio competitivo migliora molto.
- Se i migliori risultati restano episodici, le alternative centralizzate continueranno a dominare la parte piu redditizia della catena del valore.

## 9. Moat, rischio copia e dipendenze esterne
Fatti verificabili:
- L incentivo mechanism di ciascun subnet puo vivere offchain nel repository del creatore del subnet.
- La governance resta parzialmente centralizzata nel `Triumvirate`.
- Il network dipende in modo rilevante da validator, subnet leader e dal comportamento di grandi staker / delegate.
- L evento Covenant mostra che un conflitto con un team importante puo colpire direttamente fiducia e prezzo del base token.

Inferenze ragionevoli:
- Il moat vero non e il codice. E `capitale + attenzione + subnet quality + coordinamento sociale`.
- E piu facile copiare il concetto che copiare il network di partecipanti e la sua liquidita reputazionale.
- Allo stesso tempo, questo moat e meno robusto di quello di una piattaforma consumer con lock-in utente forte.
- Il business appare robusto se la rete continua ad attrarre subnet forti; appare fragile se pochi team chiave concentrano troppo la sostanza reale.

Speculazioni:
- Il rischio piu sottovalutato e la `subnet concentration`: se pochi subnet portano quasi tutta la narrativa e la credibilita, il base asset resta piu vulnerabile di quanto sembri.

## 10. Market structure del token
Fatti verificabili:
- `CoinGecko` mostra `24h volume ~$1.38B`, `24h -22.6%`, `7d -15.2%`, `30d +30.9%`.
- `CoinGlass` mostra `futures volume 24h ~$3.78B`, `spot volume 24h ~$578.36M`, `OI ~$451.73M`.
- Il `10-K` del trust dice che i `100` wallet piu grandi detenevano `~54%` del TAO in circolazione al `2025-12-31`.
- `TAO.app` mostra che circa `66%` del TAO osservato e tra root e subnet, con solo `33.99%` nei wallet.

Inferenze ragionevoli:
- TAO non e un microcap illiquido, ma resta un mercato capace di muoversi violentemente quando la narrativa cambia.
- Il fatto che il token sia ancora `+30.9%` sui `30d` anche dopo il selloff dice che parte del rally precedente non e stata cancellata: il mercato ha prezzato lo shock, ma non necessariamente tutto il repricing di medio periodo.
- La combinazione `OI alto + holder concentration + governance shock` e precisamente il tipo di setup che produce liquidazioni e gap veloci.
- L assorbimento di TAO in root e subnet aiuta il float, ma non equivale a offerta distrutta in modo irreversibile.

Speculazioni:
- Se il flusso news si stabilizza, il mercato puo tentare una base di medio periodo.
- Se emergono altri attriti di governance o altri subnet chiave prendono le distanze, il derating puo continuare anche senza nuove cattive metriche tecniche.

Limiti informativi dichiarati
- non ho funding rate, basis, borrow cost e short availability completi e verificabili nello snapshot consultato
- non ho una mappa live della liquidita per venue e profondita del book
- la confidenza sul solo `market setup` resta quindi `media-bassa`

## 11. Holder base e allineamento
Fatti verificabili:
- `TAO.app` mostra grande quota del capitale bloccata o impiegata economicamente tra root e subnet.
- Il `10-K` segnala concentrazione rilevante: `top 100 wallets ~54%` della circolante a fine 2025.
- `Grayscale` detiene una quota piccola ma istituzionale del circolante.

Inferenze ragionevoli:
- La holder base non e solo retail speculativo. C e una base di staker, validator, delegate e operatori di subnet con orizzonte almeno medio.
- Pero non e neppure una base perfettamente allineata e diffusa: la concentrazione resta alta e il peso di soggetti influenti e materiale.
- Questo rende TAO migliore della media dei token AI con classico overhang VC, ma non lo rende automaticamente sano come market structure.

Speculazioni:
- Se la base istituzionale via wrapper e staking disciplinato cresce, il profilo di holder quality migliora.
- Se invece prevale l uso come puro beta AI, la volatilita strutturale resta molto alta.

## 12. Sviluppi recenti e thesis-change events
Fatti verificabili:
- `2026-03-09` / `2026-03-10`: la model card di `Covenant-72B` e il relativo paper mostrano un output reale recente del network.
- `2026-03-22`: `BIP-023` propone un rebalance delle emissioni da `41 / 41 / 18` a `38 / 44 / 18`.
- `2026-04-09`: `The Block` riporta che `Covenant AI` lascia Bittensor e accusa il network di `decentralization theatre`.
- `2026-04-10`: `The Block` riporta la risposta di `Jacob Steeves`, che contesta almeno parte delle accuse e nega di poter sospendere le emissions.
- `2026-04-10`: il mercato reagisce con selloff violento, forte volume e leva in unwind.

Inferenze ragionevoli:
- Gli ultimi `30d` contengono sia la prova tecnica positiva piu forte della tesi, sia lo shock di fiducia piu grave.
- Gli ultimi `7d` sono chiaramente dominati dal tema `governance / fiducia`, non dal progresso tecnico.
- Gli ultimi `90d` non mostrano nelle fonti consultate exploit o halt di rete comparabili; il vero rischio recente e reputazionale / di controllo, non tecnico di base layer.

Speculazioni:
- Se il team riesce a chiudere il conflitto Covenant come episodio isolato, il danno puo essere soprattutto di optics e market setup.
- Se l evento rivela un problema persistente di concentrazione del potere, allora siamo davanti a un discount strutturale, non a rumore.

Per ogni evento materiale
- `Covenant-72B`
  - data: `2026-03-09` / `2026-03-10`
  - evento: pubblicazione della prova tecnica di un LLM `72B`
  - fonte: `Hugging Face model card` + paper arXiv collegato
  - stato: `confermato`
  - cosa e confermato: modello `72B`, `1.1T` token di training, benchmark `MMLU 67.11`, training permissionless su infrastruttura Bittensor
  - cosa resta allegation o non dimostrato: che questo successo si traduca in revenue esterna sostenibile per il network o per TAO
  - market reaction osservata: non isolabile con rigore solo da fonte primaria, ma coerente con un forte rerating del token nel mese
  - impatto su business / token / market structure / fiducia: `business + narrativa + token`
  - quanto sembra gia prezzato: `parzialmente`
  - orizzonte dell impatto: `trimestri`
  - se cambia o no la tesi: `si, migliora la credibilita tecnica del protocollo`

- `BIP-023`
  - data: `2026-03-22`
  - evento: proposta di rebalance delle emissioni a favore di validator e staker
  - fonte: `vote-bittensor.xyz`
  - stato: `in evoluzione`
  - cosa e confermato: esistenza della proposta e dello split `38 / 44 / 18`
  - cosa resta allegation o non dimostrato: esito finale e impatto economico effettivo dopo implementazione
  - market reaction osservata: non isolabile da sola
  - impatto su business / token / market structure / fiducia: `token + governance`
  - quanto sembra gia prezzato: `parzialmente`
  - orizzonte dell impatto: `settimane / trimestri`
  - se cambia o no la tesi: `rafforza la lettura di token economy policy-driven`

- `Covenant AI exit`
  - data: `2026-04-09`
  - evento: uscita di uno sviluppatore subnet importante con accuse pesanti di centralizzazione
  - fonte: `The Block`
  - stato: `confermato come evento, contestato nel merito di parte delle accuse`
  - cosa e confermato: Covenant AI lascia il network e formula accuse pubbliche contro il founder
  - cosa resta allegation o non dimostrato: sospensione unilaterale delle emissions e piena natura dei poteri esercitati
  - market reaction osservata: `TAO -22.6% 24h` su CoinGecko nello snapshot consultato; volume spot/futures molto elevato e `OI ~$451.73M`
  - impatto su business / token / market structure / fiducia: `fiducia + market structure + token`
  - quanto sembra gia prezzato: `parzialmente`
  - orizzonte dell impatto: `settimane`
  - se cambia o no la tesi: `si, aumenta il governance discount e peggiora il setup di mercato`

- `Steeves response`
  - data: `2026-04-10`
  - evento: risposta pubblica del co-founder che contesta le accuse
  - fonte: `The Block`
  - stato: `confermato`
  - cosa e confermato: Steeves nega almeno parte del claim sulla possibilita di sospendere emissions
  - cosa resta allegation o non dimostrato: il grado reale di controllo politico e sociale sul network
  - market reaction osservata: nessuna normalizzazione piena nello snapshot consultato
  - impatto su business / token / market structure / fiducia: `fiducia`
  - quanto sembra gia prezzato: `poco`
  - orizzonte dell impatto: `giorni`
  - se cambia o no la tesi: `non chiude l evento, lo tiene aperto`

Classificazione del trust shock
- `Covenant AI exit` non e semplice drama di breve
- lo classifico come `rischio reale di governance / key-person / centralizzazione`
- non e ancora dimostrato come `thesis-changing structural break` definitivo, ma e il test piu serio visto di recente sulla credibilita della decentralizzazione

Mini verdict
- `evento materiale e ancora aperto`
- impatto principale: `fiducia / market structure`
- stato: `in evoluzione`
- grado di pricing percepito: `parzialmente`
- orizzonte dominante: `settimane`

## 13. Catalizzatori
Fatti verificabili:
- esiste un wrapper pubblico istituzionale `GTAO`
- `BIP-023` e un catalizzatore governativo materiale
- il network ha appena prodotto un artefatto tecnico forte con `Covenant-72B`

Catalizzatori
- `gia noti`
  - eventuale chiusura / approvazione / implementazione di `BIP-023`
  - prosecuzione del lavoro dei subnet AI piu forti dopo `Covenant-72B`
  - sviluppo del wrapper `GTAO`

- `probabili`
  - ulteriore crescita dello staking su root e subnet se la fiducia regge
  - chiarimenti pubblici sulla governance dopo il caso Covenant
  - maggiore attenzione di mercato ai subnet che dimostrano output reali

- `opzionali`
  - maggiore trasparenza su treasury / foundation / source of control
  - nuove integrazioni o casi d uso esterni che monetizzano davvero servizi AI del network

- `puramente speculativi`
  - conversioni ETF o upgrade istituzionali molto piu aggressivi
  - nuova ondata di narrativa AI che separa Bittensor dal resto dei token AI

Valutazione rapida
- `BIP-023`: impatto `medio`, probabilita `media`, timing `settimane`, gia prezzato `parzialmente`
- `governance clarification`: impatto `alto`, probabilita `media`, timing `giorni / settimane`, gia prezzato `poco`
- `nuove prove tecniche tipo Covenant-72B`: impatto `alto`, probabilita `media`, timing `trimestri`, gia prezzato `parzialmente`
- `institutional wrapper growth`: impatto `medio`, probabilita `media`, timing `trimestri`, gia prezzato `parzialmente`

## 14. Bull case
Fatti verificabili:
- il token e ancora molto sotto l ATH storico `~$757.60`
- il network ha una prova tecnica recente non banale
- esiste gia una forma di accesso istituzionale via `GTAO`

Bull case realistico
- milestone operative richieste: nessun nuovo drama di governance, stabilizzazione post-Covenant, continuita del lavoro dei subnet forti
- metriche che devono migliorare: quota TAO in subnet, crescita staking, tenuta del prezzo sopra l area di panic low, maggiore chiarezza sulla governance
- rerating giustificabile: ritorno verso `~$330-$350`
- market cap / FDV sensati: `~$3.2B-$3.4B` di market cap su supply CoinGecko attuale; `~$6.9B-$7.4B` di FDV
- parte del rialzo da business growth: `media`
- parte del rialzo da multiple expansion o narrativa: `medio-alta`

Bull case forte
- milestone operative richieste: piu subnet con output reale, chiarimento governance convincente, nessun altro key team exit
- metriche che devono migliorare: crescita organica di staking nei subnet, piu prova di utilita economica esterna, miglioramento del market setup
- rerating giustificabile: `~$450-$500`
- market cap / FDV sensati: `~$4.3B-$4.8B` di market cap; `~$9.5B-$10.5B` di FDV
- parte del rialzo da business growth: `media`
- parte del rialzo da multiple expansion o narrativa: `alta`

Bull case estremo
- milestone operative richieste: Bittensor riconosciuto come vero winner strutturale della decentralizzazione AI
- metriche che devono migliorare: monetizzazione esterna dei subnet, adozione istituzionale piu ampia, narrativa AI fortissima, governance de-risked
- rerating giustificabile: ritorno verso `ATH ~$757.60`
- market cap / FDV sensati: `~$7.3B` di market cap su supply CoinGecko attuale; `~$15.9B` di FDV
- parte del rialzo da business growth: `bassa-media`
- parte del rialzo da multiple expansion o narrativa: `molto alta`

## 15. Bear case
Fatti verificabili:
- il token non ha revenue share diretta
- il market setup e stato appena colpito da un forte shock di fiducia
- la governance formale resta ancora in fase di transizione

Inferenze ragionevoli:
- Il bear case piu serio non e "Bittensor muore". E "il protocollo continua a esistere ma il token derata per governance discount e accrual indiretto".
- Se il mercato smette di pagare il premio AI e torna a chiedere cash flow piu visibile, TAO puo comprimersi anche con subnet tecnicamente vivi.
- Se altri team importanti mostrano sfiducia o escono, il problema diventa `subnet concentration risk`, non solo drama.
- Se l emissione residua incontra outflow da staking, la pressione di offerta torna visibile.

Speculazioni:
- Uno scenario bear credibile e ritorno in area `~$180-$220`, cioe market cap `~$1.7B-$2.1B`, senza che il network smetta di funzionare.
- Uno scenario piu duro richiede una prova forte di governance failure o deterioramento netto del flusso nei subnet.

## 16. Valuation thinking
Fatti verificabili:
- market cap spot CoinGecko `~$2.52B`
- FDV `~$5.51B`
- chain revenue 30d DefiLlama `~$465k`
- chain TVL DefiLlama `~$0`

Inferenze ragionevoli:
- Se prendo la metrica `chain revenue` alla lettera, TAO sembra costosissimo. Annualizzando `~$465k` su `30d` arrivo a `~$5.6M` annui, che su `~$2.52B` di market cap implica multipli enormi.
- Pero quella metrica non misura il valore economico del network nel suo complesso; misura soprattutto fee di chain, che per di piu vengono riciclate.
- Quindi i classici `P/S`, `P/F` o `P/revenue` sul base token sono poco utili e spesso fuorvianti.
- Il mercato sta pagando soprattutto tre cose:
  - opzionalita che Bittensor diventi il principale `coordination layer` AI onchain
  - ruolo di `TAO` come asset-base del network
  - scarsita relativa della circolante rispetto all interesse speculativo/narrativo

Speculazioni:
- Ai prezzi correnti non leggo un token ovviamente economico.
- Ma dopo il selloff non lo leggo neppure come euforia piena finita fuori scala, perche il mercato ha gia reintrodotto un governance discount rilevante.

Token accrual verdict
- Il token riceve valore economico diretto, indiretto o quasi nullo? `indiretto`
- I buyback sono abbastanza grandi da contare sul market cap attuale? `non risultano buyback di TAO da considerare`
- I buyback superano o no la pressione da unlock/emissioni? `no, perche non ho evidenza di buyback strutturali di TAO`
- I token riacquistati spariscono davvero o possono tornare sul mercato? `n.a. sul base token; il TAO assorbito in staking/riserve puo tornare sul mercato`
- Il bull case dipende da business growth, da buyback mechanics, o da semplice narrativa di scarsita? `dipende soprattutto da business proof + staking demand + narrativa, non da buyback`

## 17. Price map e scenario map
Fatti verificabili:
- prezzo spot usato: `~$262.89`
- supply per map principale: `9,597,491 TAO` CoinGecko

Scenari
- `ritorno al pre-shock recente`
  - prezzo: `~$330-$350`
  - market cap: `~$3.17B-$3.36B`
  - FDV: `~$6.93B-$7.35B`
  - assunzioni implicite: evento Covenant contenuto, nessun nuovo deterioramento, narrativa AI regge
  - probabilita qualitativa: `media`

- `ritorno all ATH`
  - prezzo: `~$757.60`
  - market cap: `~$7.27B`
  - FDV: `~$15.91B`
  - assunzioni implicite: rerating massiccio della narrativa, governance de-risked, subnet con forte validazione esterna
  - probabilita qualitativa: `bassa`

- `derating a multipli mediocri`
  - prezzo: `~$180-$220`
  - market cap: `~$1.73B-$2.11B`
  - FDV: `~$3.78B-$4.62B`
  - assunzioni implicite: governance discount piu alto, narrativa AI piu fredda, niente nuova prova economica forte
  - probabilita qualitativa: `media`

- `business cresce ma il token non segue`
  - prezzo: `~$240-$300`
  - market cap: `~$2.30B-$2.88B`
  - FDV: `~$5.04B-$6.30B`
  - assunzioni implicite: alcuni subnet migliorano, ma il mercato continua a dubitare del value accrual del base token
  - probabilita qualitativa: `medio-alta`

- `token pompa solo per narrativa`
  - prezzo: `~$400+`
  - market cap: `~$3.84B+`
  - FDV: `~$8.40B+`
  - assunzioni implicite: rotazione AI molto aggressiva, senza cambio sostanziale del waterfall
  - probabilita qualitativa: `media in bull regime, bassa fuori bull regime`

## 18. Mispricing test
Risposte secche
- cosa sta sottovalutando il mercato?
  - la qualita di Bittensor come `coordination layer` aperto per capitale e incentivi AI, e il fatto che esista almeno una prova tecnica seria come `Covenant-72B`

- cosa sta sopravvalutando il mercato?
  - la facilita con cui il successo di pochi subnet si traduce in accrual pulito per il base token `TAO`
  - il grado reale di decentralizzazione gia raggiunto oggi

- qual e la variabile piu importante che quasi tutti stanno ignorando?
  - se il network riesce a convertire attenzione, staking e successo tecnico in `inflow persistenti` e non solo in rotazione narrativa

- dove sta il vero edge dell analisi?
  - separare `business interesting` da `token automatically cheap`
  - leggere il caso Covenant come governance discount vero, ma senza buttare via la parte di sostanza tecnica del network

- cosa sto rischiando di capire male io come analista?
  - potrei sottostimare la velocita con cui un coordination layer AI puo diventare economicamente indispensabile
  - oppure potrei sottostimare quanto sia serio il problema di controllo founder-centric

- qual e il vantaggio concreto che regge la tesi anche fuori dalla narrativa crypto, se esiste?
  - esiste, ma e per operatori e capital providers piu che per l utente finale: un mercato aperto per coordinare contributi, ranking e capitale su subnet AI permissionless

## 19. Source reconciliation
Divergenze rilevanti

- `circulating supply`
  - fonti in conflitto: `CoinGecko 9.60M` vs `TAO.app / CoinGlass 10.82M`
  - differenza di definizione o perimetro: probabilmente `tradeable circulating` vs misura onchain piu ampia che include capitale in root / subnet / riserve
  - possibile motivo della divergenza: metodologie diverse su cosa contare come circulating effettivo
  - implicazione analitica: market cap e inflation rate cambiano in modo materiale; conviene ragionare su range, non su falso punto preciso

- `emission rate corrente`
  - fonti in conflitto: `glossary` indica `0.5 TAO` ogni `12 sec`; pagina `halving` parla di `current daily emission ~7,200 -> ~3,600 after first halving`
  - differenza di definizione o perimetro: documentazione non perfettamente sincronizzata tra pagine aggiornate in date diverse
  - possibile motivo della divergenza: alcune pagine sembrano riflettere la logica pre-halving o una formulazione non aggiornata
  - implicazione analitica: per prudenza uso il dato piu recente / coerente di `~3,600 TAO/day`, ma abbasso la confidenza sul punto

- `TVL / revenue`
  - fonti in conflitto: `DefiLlama TVL $0` e revenue piccola vs `TAO.app` che mostra molto capitale impegnato tra root e subnet
  - differenza di definizione o perimetro: `DefiLlama` misura DeFi TVL / chain fees; `TAO.app` mostra economia interna di staking e riserve del network
  - possibile motivo della divergenza: stanno misurando cose diverse
  - implicazione analitica: usare `TVL` DeFi per giudicare la scala del business di Bittensor e fuorviante

Conclusione della reconciliation
- Le divergenze non rompono la tesi, ma impediscono qualsiasi pretesa di precisione finta.
- Il punto chiave resta stabile: `TAO` e asset-base del network con accrual indiretto, supply non deflattiva e governance discount reale.

## 20. Checklist finale di investimento
3 motivi forti per essere bullish
- esiste una prova tecnica reale recente che alza la credibilita del network oltre la sola narrativa
- TAO e l asset-base che coordina staking, subnet access e discovery di capitale
- la struttura di supply appare meno tossica di molti token AI con classico overhang VC

3 motivi forti per essere cauti
- nessun cash flow diretto pulito verso gli holder di TAO
- shock di governance appena esploso e ancora non chiuso
- metriche economiche aggregate del business ancora opache e difficili da ricondurre al base token

3 segnali che confermerebbero la tesi
- aumento stabile della quota di TAO nei subnet senza nuovo deterioramento di fiducia
- piu subnet con output tecnico / economico reale oltre a Covenant-72B
- chiarimenti di governance che riducono in modo credibile il founder / Triumvirate discount

3 segnali che invaliderebbero la tesi
- altri team chiave lasciano il network o denunciano problemi simili a Covenant
- aumento degli outflow dai subnet e peggioramento persistente del Taoflow
- nessuna prova che il successo tecnico dei subnet si traduca in domanda economica meno speculativa

3 metriche da monitorare nei prossimi 90 giorni
- `% TAO in Subnets` e `% TAO on Root` su `TAO.app`
- esito / implementazione di `BIP-023` e successive proposte di governance
- prezzo, volume, `OI` e segni di normalizzazione post-shock dopo il `2026-04-10`

## 21. Conclusione netta
- business quality: `media`
- necessita di esistenza del prodotto: `media`
- token quality: `media`
- market setup: `fragile`
- verdict: `fairly priced`
- confidenza del giudizio: `media-bassa`
- orizzonte temporale implicito: `medio`
- motivo principale del giudizio in massimo 3 frasi:
  - Bittensor ha piu sostanza tecnica di molta concorrenza AI tokenizzata, ma `TAO` cattura quel valore in modo solo indiretto.
  - Il mercato ha gia reinserito un governance discount serio dopo il caso Covenant, quindi non lo vedo chiaramente sopravvalutato ai prezzi post-shock.
  - Non vedo pero neanche un edge evidente da token sottovalutato finche non migliora il legame tra successo dei subnet, governance credibile e value accrual del base asset.
