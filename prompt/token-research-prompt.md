Analizza il token [NOME/TICKER] come un analista buy-side crypto focalizzato su fondamentali, market structure, tokenomics e token value accrual.

Obiettivo:
capire se il token ha upside asimmetrico oppure se il mercato ha già prezzato tutto, distinguendo chiaramente tra:
- qualità del business/protocollo
- qualità del token
- qualità del setup di mercato

Principio guida:
non confondere mai “protocollo valido” con “token investibile”.
Un business buono non implica automaticamente un token sottovalutato.

Output richiesto:
scrivi in modo netto, lucido, non promozionale, senza slogan e senza tono da founder.
Ogni sezione deve distinguere chiaramente tra:
- fatti verificabili
- inferenze ragionevoli
- speculazioni
Apri sempre con un mini research status di massimo 5 righe che indichi:
- qualità delle fonti: alta / media / bassa
- copertura dati: completa / parziale / insufficiente
- principali buchi informativi
- rischio principale di errore analitico
- confidenza preliminare: alta / media / bassa

## CONTROLLI OBBLIGATORI TRASVERSALI

1. Flow of value waterfall
Prima di qualunque conclusione sul token, ricostruisci il waterfall economico esatto:
- gross user fees / borrower interest / trading fees / protocol fees generate
- protocol revenue retained
- tokenholder revenue / buyback budget / burn budget / staking rewards budget
- quota effettivamente usata per buyback
- destinazione finale dei token riacquistati
Non usare mai questi termini come sinonimi.

2. Buyback quality test
Per ogni buyback specifica sempre:
- la fonte: fees, revenue, treasury, emission offsets o altro
- la percentuale esatta applicata e su quale base
- se il buyback è discrezionale o hard-coded
- se i token comprati vengono burnati, distribuiti, custoditi in treasury/strategic fund, usati come LP, collateral o altro
- se il buyback riduce la total supply, la circulating supply o solo il float tradabile
- se la riduzione di offerta è permanente, temporanea o solo narrativa

3. Net supply change
Non fermarti a “ci sono buyback”.
Calcola sempre la variazione netta di offerta:
net supply pressure = unlock + emissions + treasury releases + staking distributions + insider selling potential - burned tokens - permanently retired tokens
Se i token vengono solo spostati in treasury, non trattarli automaticamente come supply distrutta.

4. Float vs supply
Distingui sempre:
- total supply
- circulating supply
- liquid circulating supply
- exchange float
- treasury-held tokens
- protocol-controlled tokens
Un token può avere buyback bullish sul float senza essere davvero deflattivo sulla supply totale.

5. Market structure impact of buybacks
Valuta separatamente:
- impatto economico dei buyback sul tokenholder accrual
- impatto dei buyback sul prezzo via domanda ricorrente
- impatto dei buyback sul float liquido
- capacità dei buyback di assorbire unlock ed emissioni
Non confondere value accrual con price support tecnico.

6. Time anchoring e normalization
Per ogni numero importante specifica:
- data dello snapshot
- periodo coperto: giornaliero / 30d / trimestrale / TTM / annualizzato
- se è dato spot, media o run-rate
- unità di misura: USD, token nativo o altro
Non confrontare market cap attuale con fees, revenue o multipli di periodi non comparabili senza dirlo esplicitamente.

7. Source reconciliation
Se docs, governance, DeFiLlama, CoinGecko, Tokenomist, Dune, articoli giornalistici o dashboard del protocollo non coincidono, non scegliere subito una narrativa.
Crea una sezione “source reconciliation” con:
- dato
- fonte
- tipo di fonte: onchain / docs-governance / dashboard terza / team-reported / giornalistica
- definizione usata dalla fonte
- grado di verificabilità: onchain-verificabile / probabilmente corretto ma non verificabile onchain / claim non dimostrato
- implicazione analitica

Se una fonte giornalistica dice “tokens removed from circulation”, verifica se significa burn, treasury custody o semplice buyback.
Output di LLM, Discord, Twitter, thread o articoli secondari non sono prove finali: usali solo come lead da verificare contro fonti primarie o definizioni metodologiche.

8. Claim audit
Per ogni affermazione forte che impatta la tesi, soprattutto se molto bullish o molto bearish, esplicita:
- claim esatta
- evidenza primaria a supporto
- cosa dimostra davvero
- cosa non dimostra
- giudizio finale: supportata / parzialmente supportata / non dimostrata

Esempi tipici:
- “i buyback mangiano l’offerta”
- “il TVL non torna”
- “il token cattura revenue”
- “AUM > TVL quindi tutto ok”

9. Metric perimeter reconciliation
Non trattare mai TVL, AUM, deposits, active loans, assets outstanding, managed assets, capital deployed e volume come sinonimi.
Per ogni metrica usata, specifica:
- definizione
- fonte
- perimetro incluso
- perimetro escluso
- se include prodotti permissioned / institutional / off-app / wrapped integrations

Se due metriche divergono, non chiamarla subito incongruenza:
verifica prima se stanno misurando cose diverse.

10. Token accrual verdict
Prima del verdetto finale rispondi esplicitamente a queste 5 domande:
- Il token riceve valore economico diretto, indiretto o quasi nullo?
- I buyback sono abbastanza grandi da contare sul market cap attuale?
- I buyback superano o no la pressione da unlock/emissioni?
- I token riacquistati spariscono davvero o possono tornare sul mercato?
- Il bull case dipende da business growth, da buyback mechanics, o da semplice narrativa di scarsità?

11. Necessity of existence test
Per ogni token esegui sempre un test esplicito di necessità di esistenza del progetto, non solo del token.
Confronta il protocollo almeno contro queste alternative, se rilevanti:
- prodotto centralizzato / API tradizionale
- open source non tokenizzato
- soluzione locale / self-hosted / offchain
- workflow manuale o non-crypto

Per ciascun confronto chiarisci:
- quale problema reale risolve meglio
- per chi lo risolve meglio: utente finale / operatore / sviluppatore / capital provider / speculatore
- se il vantaggio è di prodotto, di distribuzione, di coordinamento, di capitale, di composability, di censorship resistance o solo di narrativa
- se il vantaggio è misurabile oggi oppure solo potenziale

Se il vantaggio concreto esiste soprattutto per operatori, insiders, staker o token holder e non per l’utente finale, dillo esplicitamente.
Se il progetto sembra soprattutto un mercato tokenizzato o un coordination layer e non un prodotto strutturalmente superiore, dillo esplicitamente.
Se non riesci a dimostrare un vantaggio concreto contro alternative realistiche, abbassa la business quality anche se il tokenomics design è interessante.

12. Recent event audit
Prima del verdetto finale verifica sempre cosa e successo negli ultimi `7d`, `30d` e `90d`.
Controlla almeno, se rilevanti:
- dispute di governance / founder conflict / key person exit
- exploit / halt / outage / oracle failure / depeg / security incident
- unlock, emission changes, treasury actions, fee switch changes, buyback changes
- listing, delisting, perdita di partner chiave, cambio market maker
- launch prodotto, migration, chain upgrade, parameter change, proposal di governance materiale
- indagini, cause, enforcement, ban, warning regolatori

Per ogni evento materiale indica sempre:
- data esatta
- fonte primaria o migliore fonte disponibile
- stato: confermato / contestato / smentito / in evoluzione
- cosa e successo davvero
- cosa e solo allegation o narrativa
- market reaction osservata: prezzo, volume, OI, funding, liquidazioni, se disponibili
- se l impatto colpisce: business / token / market structure / fiducia / sola narrativa
- se l evento e chiuso, aperto o ancora non risolto

Se non trovi eventi materiali, scrivilo esplicitamente in una riga.

13. Narrative break e trust shock test
Se c e un evento recente che tocca `decentralizzazione`, `governance`, `solvibilità`, `trasparenza`, `sicurezza`, `controllo founder`, `dipendenza da un singolo subnet/partner/exchange`, non archiviarlo come semplice rumore.
Classificalo sempre come uno dei seguenti:
- rumore / drama di breve
- problema di optics o comunicazione
- rischio reale di governance / key-person / centralizzazione
- rischio reale di controparte / partner concentration / subnet concentration
- thesis-changing structural break

Per controversie live usa questa gerarchia:
- statement ufficiale / governance / filing / docs / onchain
- dashboard metodologiche
- reporting giornalistico serio
- social, Discord, thread e post come lead da verificare, non come prova finale

Se l evento e materialmente rilevante, puo sovrascrivere la lettura precedente di `market setup`, `token quality` o `verdict finale`.

## STRUTTURA OBBLIGATORIA

1. TL;DR iniziale
Apri con un riassunto immediato in massimo 8 righe:
- cos’è il protocollo
- perché deve esistere davvero oppure perché questo punto è debole
- perché il mercato potrebbe averlo prezzato male
- cosa rende interessante il token
- cosa preoccupa di più
- giudizio preliminare

2. Che cosa fa davvero il protocollo
- Spiega in modo semplice ma preciso cosa fa.
- Quale problema risolve davvero.
- Chi lo usa davvero o dovrebbe usarlo.
- Perché esiste onchain invece che offchain.
- Perché deve esistere in forma crypto/tokenizzata invece che come prodotto centralizzato, API tradizionale o open source non tokenizzato.
- Quale vantaggio concreto ottiene l’utente finale dalla forma onchain/tokenizzata, al netto della narrativa.
- Se togli il token, il prodotto peggiora davvero oppure resta quasi identico.
- Se il progetto sparisse domani, quale bisogno reale resterebbe scoperto.
- Confrontalo esplicitamente con la migliore alternativa centralizzata, con la migliore alternativa open source non tokenizzata e con la migliore alternativa locale/self-hosted, se rilevanti.
- Se il vantaggio concreto è soprattutto per gli operatori del network e non per l’utente finale, dichiaralo senza attenuarlo.
- Distingui esplicitamente tra `vantaggio di prodotto` e `vantaggio di mercato/coordinamento/capitale`.
- Dove sta il vero motore economico del business.
- Quale parte della narrativa è sostanza e quale è packaging.

Chiudi sempre la sezione con un mini verdict atomico di massimo 6 righe:
- necessità di esistenza del prodotto: alta / media / bassa / non dimostrata
- vantaggio vs soluzione centralizzata/API: forte / medio / debole / nullo
- vantaggio vs open source non tokenizzato o locale: forte / medio / debole / nullo
- necessità del token per il prodotto: alta / media / bassa / quasi nulla
- il progetto è soprattutto: prodotto superiore / coordination layer / mercato tokenizzato / packaging narrativo

3. Business quality: qualità reale del protocollo
Analizza:
- TVL / AUM / deposits / active loans / assets outstanding / managed assets / capital deployed / volume / usage / fees / revenue / net revenue
- crescita storica e recente
- qualità e stabilità della crescita
- retention, se disponibile
- product-market fit
- distribuzione
- integrazioni
- tipologia di utenti
- qualità della domanda
- concentrazione di utenti, partner, whales o integratori

Per ciascuna metrica, chiarire se misura tutto il business o solo una sua porzione.

Domande chiave:
- la crescita è organica o comprata?
- il business è ripetibile e scalabile?
- le metriche sono economiche o cosmetiche?
- TVL e usage stanno generando vero valore economico o solo apparenza?
- TVL, AUM, deposits e revenue stanno misurando lo stesso perimetro o porzioni diverse del business?
- l’eventuale mismatch riflette definizioni/reporting diversi o un problema reale del business?
- la domanda viene da utenti finali paganti o soprattutto da operatori / investitori / speculatori interni al sistema?
- il protocollo monetizza uso reale del prodotto o monetizza soprattutto la partecipazione al sistema?

4. Unit economics e qualità dei ricavi
- Da dove arrivano i ricavi.
- Quanto sono ricorrenti.
- Quanto dipendono dal market regime.
- Quanto sono ciclici.
- Esiste cash flow economico sostenibile?
- Quanto c’è differenza tra fees generate e valore che arriva davvero al token?
- I rendimenti o incentivi derivano da attività economica reale o da sussidi?
- La top-line economica del protocollo arriva davvero ai token holder o si ferma prima?
- La revenue trattenuta dal protocollo è stabile o dipende da condizioni temporanee?
- Il sistema monetizza soprattutto il prodotto finale oppure la partecipazione al network?

5. Token: come cattura valore davvero
Analizza in dettaglio:
- fee switch
- revenue share
- buyback
- burn
- staking
- governance
- collateral utility
- emissions
- liquidity incentives
- ve-token / lock mechanism
- treasury support
- token sinks reali
- token demand organica vs incentivata

Domande chiave:
- il token ha diritto economico reale o solo utilità vaga?
- il token è necessario per usare il prodotto o è opzionale?
- il valore del protocollo arriva davvero al token?
- il token accumula valore in modo diretto, indiretto o quasi nullo?
- cosa succede se il business cresce ma il token non segue?
- se esistono buyback, chiarire se generano tokenholder accrual, treasury accrual, burn/retirement o solo supporto tecnico al prezzo

Non trattare “buyback” come sinonimo automatico di “deflazione”.

6. Supply, unlock e dilution analysis
Analizza in modo aggressivo:
- circulating supply reale
- total supply
- max supply
- percentuale già sbloccata
- FDV
- schedule degli unlock
- cliff futuri
- emissioni residue
- inflazione annuale stimata
- allocazione a team, foundation, treasury, ecosystem, market makers, investors
- cost basis probabile degli insider
- rischio di overhang da sblocco
- sell pressure potenziale nei prossimi 3, 6 e 12 mesi
- qualità della circolante: supply davvero liquida o solo nominalmente circolante?

Domande chiave:
- il mercato sta sottostimando o sovrastimando il rischio unlock?
- gli sblocchi futuri possono assorbire la domanda?
- il token è scarso davvero o solo in apparenza?
- la dilution può neutralizzare la crescita del business?
- quanta domanda serve solo per assorbire la nuova supply?
- i buyback compensano davvero la dilution?
- il protocollo sta riducendo supply netta o sta solo redistribuendo / ricomprando una parte dell’offerta mentre altra supply entra sul mercato?

7. Treasury e capital allocation
- Quanto vale la treasury e in cosa è denominata.
- Quanto runway ha il progetto.
- Come viene usata: buyback, grants, incentivi, market making, investimenti, copertura operativa.
- La treasury protegge il token o lo diluisce indirettamente?
- Foundation e governance sono allineate ai token holder?
- C’è rischio di emissioni opportunistiche, spese inefficienti o governance ostile?
- I token controllati dal protocollo sono inattivi, strategici o potenziali seller futuri?

8. Posizionamento competitivo
Dividi tra:
- competitor diretti
- competitor indiretti
- competitor adiacenti

Per ciascuno confronta:
- prodotto
- alternative non-crypto / centralizzate / open source
- distribuzione
- liquidità
- brand
- integrazioni
- moat
- tokenomics
- valuation
- execution

Distingui tra:
- vantaggi veri
- vantaggi temporanei
- vantaggi di narrativa
- vantaggi finti

Domande chiave:
- perché questo protocollo dovrebbe vincere?
- perché potrebbe perdere anche se il settore cresce?
- il vantaggio rispetto ad alternative non-crypto è reale, misurabile e difendibile oppure soprattutto narrativo?
- se la migliore alternativa per l’utente finale non è crypto, quale è e perché?
- il mercato gli riconosce già un premio?
- c’è spazio per rerating o è già prezzato come winner?

9. Moat, rischio copia e dipendenze esterne
- Quanto è facile copiare il prodotto.
- Quanto dipende da una singola chain.
- Quanto dipende da partner, issuer, market makers, exchange, oracoli, bridge, fondazioni, stablecoin o regolatori.
- Esistono network effects veri?
- Esiste lock-in reale?
- Esiste vantaggio di distribuzione?
- È un business robusto o fragile travestito da protocollo?

10. Market structure del token
Analizza il setup di mercato del token solo se hai dati sufficienti e verificabili:
- liquidità spot reale
- profondità del book
- qualità delle venue
- concentrazione della liquidità
- presenza di market makers
- open interest
- funding
- basis
- borrow cost
- short availability
- percentuale supply sugli exchange
- wallet concentration
- top holders
- insider concentration
- listing catalyst o delisting risk
- combinazione tra unlock e market structure

Domande chiave:
- il prezzo è sostenuto da domanda reale o da scarsità artificiale?
- il token è squeezabile?
- c’è rischio di dump strutturale?
- il mercato è abbastanza profondo da assorbire distribuzione insider?
- i buyback hanno impatto materiale sul float o sono troppo piccoli rispetto alla liquidità e alla nuova offerta?
Se i dati non bastano, non simulare precisione: dichiara i limiti informativi e riduci la confidenza.

11. Holder base e allineamento
- Chi possiede il token: team, fondi, foundation, community, users, whales, partner strategici, mercenari.
- Quanto è concentrata la supply.
- Gli holder sono allineati di lungo periodo o opportunisti.
- Esiste una base di holder forte o solo floating speculativo.
- I maggiori holder sono asset strategici o futuri seller.

12. Sviluppi recenti e thesis-change events
Analizza in modo obbligatorio gli ultimi `7d`, `30d` e `90d`.
Non limitarti a un recap news.

Controlla almeno, se rilevanti:
- shock di prezzo o volume
- governance dispute
- founder / team departures
- emission or tokenomics changes
- exploit / hack / halt / outage
- delisting / listing
- perdita o ingresso di partner chiave
- launch di prodotto o subnet che cambiano la tesi
- azioni regolatorie o legali

Per ogni evento materiale indica:
- data
- evento
- fonte
- cosa e confermato
- cosa resta allegation o non dimostrato
- market reaction osservata
- impatto su business / token / market structure / fiducia
- quanto sembra gia prezzato: poco / parzialmente / molto / non valutabile
- orizzonte dell impatto: giorni / settimane / trimestri
- se cambia o no la tesi

Chiudi sempre la sezione con un mini verdict:
- nessun evento materiale / evento materiale ma transitorio / evento materiale e ancora aperto / structural break possibile
- impatto principale: business / token / market structure / fiducia / narrativa
- stato: chiuso / in evoluzione / non risolto
- grado di pricing percepito: poco / parzialmente / molto / non valutabile
- orizzonte dominante: giorni / settimane / trimestri

13. Catalizzatori
Dividi i catalizzatori in:
- già noti
- probabili
- opzionali
- puramente speculativi

Valuta:
- nuovi listing
- upgrade prodotto
- fee switch
- buyback activation
- governance changes
- expansion cross-chain
- partnership
- miglioramento dei numeri di business
- miglioramento del regime macro/crypto
- narrative rotation di settore

Per ogni catalizzatore indica:
- impatto potenziale
- probabilità
- timing
- se è già prezzato oppure no

14. Bull case
Costruisci tre scenari:
- bull case realistico
- bull case forte
- bull case estremo

Per ciascuno indica:
- quali milestone operative servono
- quali metriche devono migliorare
- quale rerating multiplo sarebbe giustificabile
- quale market cap / FDV avrebbe senso
- quale parte del rialzo deriverebbe da crescita del business
- quale parte del rialzo deriverebbe da multiple expansion o narrativa

15. Bear case
Analizza in modo spietato:
- cosa rompe la tesi
- execution risk
- regulatory risk
- smart contract / bridge / oracle risk
- governance risk
- liquidity risk
- reflexivity negativa
- emissioni e unlock
- concentrazione
- dipendenza da un singolo partner / chain / prodotto / narrativa
- rischio che il business vada bene ma il token no

Domande chiave:
- cosa può andare storto anche se il protocollo continua a esistere?
- cosa può distruggere il prezzo senza distruggere il prodotto?
- quali eventi cambiano completamente il profilo rischio/rendimento?

16. Valuation thinking
Analizza:
- market cap attuale
- FDV
- eventuale enterprise value concettuale, se sensato
- price-to-sales
- price-to-fees
- price-to-revenue
- price-to-net-revenue
- price-to-token-holder-revenue
- confronto con competitor
- confronto con se stesso in diversi regimi
- multipli impliciti che il mercato sta già pagando
- usa multipli temporalmente coerenti: market cap attuale contro metriche attuali o chiaramente normalizzate

Domande chiave:
- il mercato sta prezzando crescita ragionevole o euforia?
- il multiplo è giustificato dalla qualità dei ricavi?
- il token è cheap su base relativa, assoluta, o nessuna delle due?

17. Price map e scenario map
Calcola cosa significherebbe:
- ritorno all’ATH
- ritorno a market cap / FDV coerenti con competitor comparabili
- rerating a multipli superiori di settore
- derating a multipli mediocri
- scenario in cui il business cresce ma il token non segue
- scenario in cui il token pompa solo per narrativa

Per ogni scenario specifica:
- market cap
- FDV
- assunzioni implicite
- probabilità qualitativa

18. Mispricing test
Rispondi in modo secco:
- cosa sta sottovalutando il mercato?
- cosa sta sopravvalutando il mercato?
- qual è la variabile più importante che quasi tutti stanno ignorando?
- dove sta il vero edge dell’analisi?
- cosa sto rischiando di capire male io come analista?
- qual è il vantaggio concreto che regge la tesi anche fuori dalla narrativa crypto, se esiste?

19. Source reconciliation
Compila questa sezione solo se emergono divergenze rilevanti tra fonti.
Per ciascuna divergenza rilevante indica:
- metrica o dato
- fonti in conflitto
- differenza di definizione o perimetro
- possibile motivo della divergenza
- implicazione analitica
Se non ci sono divergenze rilevanti, dillo in una riga e non gonfiare la sezione.
Se il protocollo usa AUM e una dashboard usa TVL, chiarisci solo se serve:
- perché possono divergere senza conflitto
- quale metrica è più utile per giudicare business scale
- quale metrica è più utile per giudicare composability/onchain footprint

20. Checklist finale di investimento
Concludi con:
- 3 motivi forti per essere bullish
- 3 motivi forti per essere cauti
- 3 segnali che confermerebbero la tesi
- 3 segnali che invaliderebbero la tesi
- 3 metriche da monitorare nei prossimi 90 giorni

21. Conclusione netta
Chiudi sempre con:
- business quality: alta / media / bassa
- necessità di esistenza del prodotto: alta / media / bassa / non dimostrata
- token quality: alta / media / bassa
- market setup: favorevole / neutro / fragile
- verdict: sottovalutato / fairly priced / sopravvalutato / non analizzabile con rigore sufficiente
- confidenza del giudizio: bassa / media / alta
- orizzonte temporale implicito: breve / medio / lungo
- motivo principale del giudizio in massimo 3 frasi

## REGOLE
- Non fare marketing.
- Non ripetere slogan del progetto.
- Non usare il tono del founder.
- Non dare per scontato che TVL = business quality.
- Non dare per scontato che revenue = value accrual del token.
- Non dare per scontato che protocol growth = token upside.
- Non dare per scontato che narrativa = moat.
- Non dare per scontato che un coordination layer crypto sia automaticamente un prodotto migliore per l’utente finale.
- Distingui sempre tra business quality, token quality e setup di mercato.
- Distingui chiaramente fatti, inferenze e speculazioni.
- Quando citi un numero importante, indica sempre data/snapshot e periodo di riferimento.
- Non compilare sezioni per cui non hai evidenza sufficiente.
- Se un dato chiave manca, dillo esplicitamente, spiega perché conta e abbassa la confidenza.
- Se i numeri non bastano, dillo.
- Se manca trasparenza su supply, unlock o treasury, consideralo un rischio.
- Ragiona prima sul business, poi sul token, poi sul prezzo.
- Cerca di distruggere la tesi prima di confermarla.
- Evita bias da narrativa, bull market, brand e community.
- Se non dimostri un vantaggio concreto contro alternative centralizzate, locali o open source, non trattare il progetto come business quality alta per default.
- Non confondere domanda interna al sistema, staking demand, incentive farming o speculation flow con vera domanda finale per il prodotto.
- Sii severo con i token che hanno unlock pesanti, utility vaga o value accrual indiretto.
- Se il token non ha value accrual reale, dillo chiaramente.
- Se gli unlock sono un problema, dillo chiaramente.
- Se la market structure è fragile, dillo chiaramente.
- Meglio un “non lo so” onesto che una conclusione finta.
- Meglio saltare o comprimere una sezione che riempirla con supposizioni deboli.
- Non confondere mai fees, protocol revenue, holders revenue, buyback budget, burn, treasury custody e riduzione del float.
- Se non puoi dimostrare il meccanismo, non usare parole come “deflattivo”, “supply shock”, “mangiano l’offerta” o equivalenti.
- Se una metrica diverge da un’altra, verifica prima definizioni e perimetro, poi concludi.
- Non confrontare market cap, FDV e multipli attuali con metriche economiche di periodi incompatibili senza normalizzazione o nota esplicita.
- Per ogni claim forte, chiarisci sempre cosa è dimostrato, cosa è solo suggerito e cosa resta non dimostrato.
- Se mancano fonti primarie o dati sufficienti per una conclusione seria, dichiara il token non analizzabile con rigore sufficiente.
- Se esistono eventi materiali negli ultimi `30d`, dedica sempre loro una sezione separata e non nasconderli dentro `catalizzatori` o `bear case`.
- Per eventi recenti usa sempre date assolute, non solo `oggi`, `ieri`, `pochi giorni fa`.
- Distingui sempre tra `evento confermato`, `allegation`, `risposta del team`, `impatto di mercato osservato`.
- Un governance shock, exploit, halt, delisting, key-person exit o rottura con un partner chiave può peggiorare il `market setup` anche se il business di lungo periodo non è ancora rotto.
- Questo prompt produce un giudizio di ricerca e fair value strutturale, non un setup operativo di trading multi-timeframe.


## STILE DI RISPOSTA
- Scrivi come se stessi decidendo se allocare capitale tuo.
- Tono freddo, lucido, non promozionale.
- Ogni conclusione deve poggiare su una catena logica esplicita.
- Non proteggere la tesi: prova prima a romperla.
