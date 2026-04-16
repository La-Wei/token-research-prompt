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
Apri sempre con la sezione `0. Research mode e perimetro evidenze`.
Non aggiungere un mini status separato fuori struttura.

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

6A. Market snapshot anchoring
Per ogni numero di `spot price` o `market cap` che entra in valuation, scenario map o verdict finale, specifica sempre:
- fonte anchor principale
- timestamp dello snapshot
- se il dato e `live spot`, `EOD`, media o range aggregato
- se il `market cap` e same-timestamp oppure derivato da `price x circulating supply`

Per asset liquidi o major:
- non basta una dashboard aggregata se esiste una venue/API spot primaria ragionevolmente accessibile
- cross-checka sempre lo spot con almeno una venue/API primaria o fonte spot equivalente
- se `CoinGecko`, `CoinMarketCap`, `CoinGlass` o altra dashboard divergono materialmente dal live spot della venue, non quotare la dashboard come verita finale
- usa il `source reconciliation evidence log` per spiegare la divergenza

Ordine pratico consigliato per `spot price / market cap` su asset liquidi o major:
- venue/API spot primarie:
  - `Binance Spot`
  - `Kraken Spot`
  - `Coinbase Exchange`
  - `Bitget Spot`
  - altra venue spot primaria effettivamente dominante sul pair
- venue/API perp o derivati per `OI`, funding, basis, liquidazioni e positioning:
  - `Binance Futures`
  - `Bitget Futures`
  - `Hyperliquid`
  - `Kraken Perp`
  - altra venue derivata primaria effettivamente dominante
- dashboard aggregate per cross-check, venue mix, historical context e metriche secondarie:
  - `CoinMarketCap`
  - `CoinGecko`
  - `CoinGlass` soprattutto per derivati e market structure, non come verita spot finale se diverge

Regola pratica:
- usa idealmente sia `CoinMarketCap` sia `CoinGecko` come cross-check fra dashboard aggregate quando disponibili
- ma per il prezzo finale prevale sempre una venue/API spot primaria o un anchor equivalente meglio riconciliato

Non mischiare come se fossero lo stesso snapshot:
- tick live
- close `EOD`
- range `24h / 7d / 30d`
- market cap catturati in momenti diversi

7. Source reconciliation discipline
Se docs, governance, DeFiLlama, `CoinMarketCap`, CoinGecko, Tokenomist, Dune, articoli giornalistici o dashboard del protocollo non coincidono, non scegliere subito una narrativa.
Crea un blocco `source reconciliation evidence log` con:
- dato
- fonte
- tipo di fonte: onchain / docs-governance / dashboard terza / team-reported / giornalistica
- definizione usata dalla fonte
- grado di verificabilità: onchain-verificabile / probabilmente corretto ma non verificabile onchain / claim non dimostrato
- implicazione analitica

Se una fonte giornalistica dice “tokens removed from circulation”, verifica se significa burn, treasury custody o semplice buyback.
Output di LLM, Discord, Twitter, thread o articoli secondari non sono prove finali: usali solo come lead da verificare contro fonti primarie o definizioni metodologiche.

7A. Opacity compression rule
Se il protocollo e opaco, giovane, fortemente offchain o poco documentato, non riempire ogni sottosezione con varianti di `non trovato`.
Quando waterfall, supply, treasury o holder base non si possono chiudere con rigore:
- comprimi la parte in un blocco sintetico
- esplicita:
  - quali dati mancano
  - quale inferenza resta bloccata
  - perche il buco conta davvero
  - come cambia la confidenza
- privilegia l implicazione analitica rispetto alla ripetizione dell assenza del dato

7B. Research mode selector
Classifica sempre il report in una di queste due modalita:
- `full diligence`
- `opacity-compressed`

Usa `full diligence` se:
- le fonti sono almeno `medie`
- la copertura dati e almeno `parziale`
- i blocchi che decidono il fair value strutturale sono ricostruibili con rigore sufficiente, soprattutto:
  - waterfall / value accrual
  - supply / unlock
  - treasury / capital allocation
  - business scale / quality dei ricavi / valuation
- la market structure del token puo anche restare `limitata`, se non impedisce di chiudere con rigore business, token e fair value

Usa `opacity-compressed` se:
- le fonti sono `basse` o troppo indirette
- la copertura dati e `insufficiente` o troppo bucata sui blocchi che contano
- waterfall, supply, treasury o il legame business -> token non si chiudono con evidenza primaria o metodologica abbastanza seria

Regole dure:
- se sei in `opacity-compressed` per buchi critici su waterfall, supply o treasury, la `confidenza del giudizio` non puo superare `bassa`
- in `opacity-compressed`, dichiara i limiti una volta in modo ordinato e poi aggiorna solo le implicazioni che cambiano la tesi
- non usare la sola scarsita di dati di market microstructure come motivo sufficiente per forzare `opacity-compressed`, se il fair-value work resta chiudibile con rigore

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

Nota di naming:
- il prefisso `CT-` identifica controlli trasversali continui
- serve a distinguerli dalle future sezioni strutturali `12. Thesis-change synthesis` e `13. Catalizzatori`

CT-12. Recent event evidence log
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

CT-13. Narrative break e trust shock test
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

## MAPPA OBBLIGATORIA DEI CONTROLLI TRASVERSALI

Per evitare duplicazioni o omissioni, usa sempre questa mappa:
- controlli `1-5`:
  - devono emergere nelle sezioni `4`, `5`, `6`, `7`
  - e devono chiudersi esplicitamente in `7A. Token accrual e net supply verdict`
- controlli `6 / 6A. Time anchoring, normalization e market snapshot anchoring`:
  - si applica a qualunque sezione con numeri
  - soprattutto `3`, `4`, `6`, `16`, `17`, `19`, `21`
- controllo `7. Source reconciliation discipline`:
  - funziona come evidence log metodologico durante l analisi
  - la sezione finale `19. Residual source divergences` deve riportare solo divergenze residue che cambiano verdict o confidenza
- controllo `8. Claim audit`:
  - va applicato inline nei punti dove usi claim forti
  - le `1-3` claim piu importanti per la tesi devono essere richiamate in `18B. Claim audit residuale`
- controllo `9. Metric perimeter reconciliation`:
  - deve emergere soprattutto in `3. Business quality`, `16. Valuation thinking` e `19. Residual source divergences`, se resta una divergenza aperta
- controllo `10. Token accrual verdict`:
  - deve chiudersi esplicitamente in `7A. Token accrual e net supply verdict`
  - e va richiamato in `21. Conclusione netta`
- controllo `11. Necessity of existence test`:
  - si chiude in `2. Che cosa fa davvero il protocollo`
- founder / team / trust surface:
  - si chiude in `11A. Founder, team e trust surface`
  - e va richiamato in `21. Conclusione netta`
  - puo peggiorare `business quality`, `token quality` o `market setup` anche senza un nuovo evento materiale
- controlli `CT-12 / CT-13`:
  - il prefisso `CT-` li distingue dalle sezioni strutturali `12` e `13`
  - il `Recent event evidence log` serve come log metodologico dei fatti
  - `12. Thesis-change synthesis` deve sintetizzare solo gli eventi che cambiano davvero la tesi
  - `13. Catalizzatori` deve coprire solo il potenziale residuo non ancora accaduto o non ancora pienamente prezzato
  - `15. Bear case` deve usare gli eventi solo come rischio strutturale, non ricopiare il log eventi

## STRUTTURA OBBLIGATORIA

0. Research mode e perimetro evidenze
- qualità delle fonti: alta / media / bassa
- copertura dati: completa / parziale / insufficiente
- modalita: `full diligence` / `opacity-compressed`
- motivo della scelta
- copertura market structure: robusta / limitata / minima
- blocchi osservabili con rigore sufficiente
- blocchi ancora non chiudibili
- implicazione principale dei buchi dati
- rischio principale di errore analitico
- cap di confidenza, se presente
- confidenza preliminare: alta / media / bassa

1. TL;DR iniziale
Apri con un riassunto immediato in massimo 8 righe:
- cos’è il protocollo
- perché deve esistere davvero oppure perché questo punto è debole
- perché il mercato potrebbe averlo prezzato male
- cosa rende interessante il token
- cosa preoccupa di più
- giudizio preliminare

2. Che cosa fa davvero il protocollo
- questa sezione deve spiegare il prodotto e la necessità di esistenza
- non usare questa sezione per anticipare in dettaglio metriche, multipli o market structure: quelle vivono piu avanti
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

2A. Compression branch per asset opachi
Compila questa sezione solo se la modalita e `opacity-compressed`.
- se usi questo ramo, le sezioni `3-11` vengono sostituite dal branch compresso qui sotto e non vanno compilate in forma completa, salvo dati eccezionalmente solidi su un singolo blocco
- non trattare le sezioni `3-11` come una checklist da riempire meccanicamente
- usa invece questi tre blocchi sostitutivi:
  - `2A.1 Business e unit economics compressed`
  - `2A.2 Token / supply / treasury compressed`
  - `2A.3 Market structure / holders compressed`
- per ciascun blocco compresso indica sempre:
  - cosa e verificabile
  - cosa resta bloccato
  - quale inferenza importante non puoi chiudere
  - come cambia il verdict o la confidenza
- non ripetere gli stessi buchi informativi gia dichiarati in `0. Research mode e perimetro evidenze`
- dopo il ramo `2A`, continua comunque con:
  - `7A. Token accrual e net supply verdict`
  - `11A. Founder, team e trust surface`
  - `12-21`

Template minimo:
- `2A.1 Business e unit economics compressed`
  - scala del business verificabile
  - qualità dei ricavi verificabile
  - metriche non chiudibili
  - implicazione sul fair value
- `2A.2 Token / supply / treasury compressed`
  - meccanismo di accrual verificabile
  - supply / unlock / treasury verificabili
  - punti ancora non dimostrabili
  - implicazione sul token
- `2A.3 Market structure / holders compressed`
  - ciò che si vede davvero su liquidita / holders / float
  - ciò che resta opaco
  - implicazione su fragilita e confidenza

3. Business quality: qualità reale del protocollo
Compila questa sezione solo se la modalita e `full diligence`.
- focalizzati su metriche, qualità della crescita e qualità della domanda
- non ripetere qui la spiegazione base del prodotto gia chiusa nella sezione `2`
- per le metriche piu importanti, esplicita sempre definizione e perimetro inline
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
Compila questa sezione solo se la modalita e `full diligence`.
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
Compila questa sezione solo se la modalita e `full diligence`.
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
Compila questa sezione solo se la modalita e `full diligence`.
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
Compila questa sezione solo se la modalita e `full diligence`.
- Quanto vale la treasury e in cosa è denominata.
- Quanto runway ha il progetto.
- Come viene usata: buyback, grants, incentivi, market making, investimenti, copertura operativa.
- La treasury protegge il token o lo diluisce indirettamente?
- Foundation e governance sono allineate ai token holder?
- C’è rischio di emissioni opportunistiche, spese inefficienti o governance ostile?
- I token controllati dal protocollo sono inattivi, strategici o potenziali seller futuri?

7A. Token accrual e net supply verdict
Compila sempre questa sezione, in `full diligence` o in `opacity-compressed`.
Qui devi chiudere in modo esplicito i controlli trasversali su waterfall, buyback, supply netta e token accrual.
- il token riceve valore economico: diretto / indiretto / quasi nullo
- il driver principale del bull case e: business growth / buyback mechanics / scarsita narrativa / mix
- i buyback sono materialmente rilevanti sul market cap attuale: si / no / non dimostrabile
- i buyback superano la pressione da unlock / emissioni: si / no / non dimostrabile
- i token riacquistati spariscono davvero: si / no / parzialmente / non dimostrabile
- la supply netta appare: in riduzione / stabile / in aumento / non chiudibile con rigore
- il legame business -> token e: forte / medio / debole / quasi nullo / non dimostrabile
- mini verdict finale della sezione: bullish per il token / neutro / fragile / negativo / non chiudibile con rigore

8. Posizionamento competitivo
Compila questa sezione solo se la modalita e `full diligence`.
- confronta soprattutto vantaggio competitivo e pricing del vantaggio
- non ripetere qui la spiegazione base del prodotto gia chiusa in `2`
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
Compila questa sezione solo se la modalita e `full diligence`.
- questa sezione deve testare la difendibilita del business
- non rifare qui il confronto competitivo completo della sezione `8`
- Quanto è facile copiare il prodotto.
- Quanto dipende da una singola chain.
- Quanto dipende da partner, issuer, market makers, exchange, oracoli, bridge, fondazioni, stablecoin o regolatori.
- Esistono network effects veri?
- Esiste lock-in reale?
- Esiste vantaggio di distribuzione?
- È un business robusto o fragile travestito da protocollo?

10. Market structure del token
Compila questa sezione solo se la modalita e `full diligence`.
Questa sezione serve a giudicare la fragilita strutturale del token, non a costruire timing operativo.
Analizza il setup di mercato del token solo se hai dati sufficienti e verificabili:
- liquidità spot reale
- profondità del book
- qualità delle venue
- concentrazione della liquidità
- presenza di market makers
- open interest, solo se materialmente rilevante
- funding, solo se materialmente rilevante
- basis, solo se materialmente rilevante
- borrow cost, solo se materialmente rilevante
- short availability, solo se materialmente rilevante
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
L assenza di microstructure avanzata non deve da sola invalidare un fair-value report se business, token e valuation restano chiudibili con rigore.

11. Holder base e allineamento
Compila questa sezione solo se la modalita e `full diligence`.
- Chi possiede il token: team, fondi, foundation, community, users, whales, partner strategici, mercenari.
- Quanto è concentrata la supply.
- Gli holder sono allineati di lungo periodo o opportunisti.
- Esiste una base di holder forte o solo floating speculativo.
- I maggiori holder sono asset strategici o futuri seller.

11A. Founder, team e trust surface
Compila sempre questa sezione, in `full diligence` o in `opacity-compressed`.
Questa sezione deve restare minima e fattuale: serve a giudicare `execution credibility`, `trust risk` e `key-person risk`, non a fare gossip.

Copri solo cio che conta davvero per la tesi:
- chi sono founder, team pubblico o figure chiave realmente riconducibili al progetto
- se sono pubblici, pseudonimi consistenti o sostanzialmente opachi
- quali progetti rilevanti hanno gia costruito o guidato
- esiti sintetici del track record precedente: successi, fallimenti, shutdown, exploit, governance blow-up, controversie materiali, problemi legali o reputazionali
- se esiste dipendenza eccessiva da una singola figura
- se esistono conflitti di interesse, precedenti pattern di dilution opportunistica, treasury abuse, rug, false disclosure o altre criticita realmente documentate

Per ogni elemento importante distingui sempre:
- fatto verificabile
- implicazione analitica
- cosa resta non dimostrato

Etichette di sintesi ammesse:
- founder/team track record: `buono / neutro / misto / debole / non verificabile`
- accountability pubblica: `alta / media / bassa`
- trust risk: `basso / medio / alto / molto alto`

Regola dura:
- non usare etichette come `scammer`, `fraud`, `rugger` o equivalenti senza evidenza primaria molto forte, ammissioni, filing, sentenze o documentazione schiacciante
- se il quadro e grave ma non chiuso giuridicamente, usa formule come:
  - `controversie reputazionali rilevanti`
  - `track record fortemente controverso`
  - `trust risk alto`
  - `criticita gravi ma non definitivamente provate`

Chiudi sempre la sezione con un mini verdict:
- founder/team track record: `buono / neutro / misto / debole / non verificabile`
- accountability pubblica: `alta / media / bassa`
- trust risk: `basso / medio / alto / molto alto`
- implicazione principale sulla tesi: una frase secca

12. Thesis-change synthesis
Analizza in modo obbligatorio gli ultimi `7d`, `30d` e `90d`.
Non limitarti a un recap news.
Questa sezione deve sintetizzare e aggiornare il controllo trasversale `CT-12. Recent event evidence log`, non duplicarlo meccanicamente riga per riga.
Non fare qui un secondo event log completo.
Seleziona solo gli `1-3` sviluppi che cambiano davvero tesi, pricing o confidenza.

Per ciascuno sviluppo davvero thesis-changing indica:
- data
- sviluppo o evento
- cosa e confermato
- cosa resta allegation o non dimostrato
- market reaction osservata
- cosa cambia davvero in tesi / token / pricing / confidenza
- quanto sembra gia prezzato: poco / parzialmente / molto / non valutabile
- orizzonte dell impatto residuo: giorni / settimane / trimestri

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

Regola di deduplicazione:
- non riciclare qui un fatto gia accaduto solo per allungare la tesi
- se un evento recente ha ancora una seconda gamba futura non prezzata, qui descrivi solo il potenziale residuo, non riscrivere l evento
- questa sezione guarda avanti; `12. Thesis-change synthesis` guarda prima a cio che e gia successo

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

Regola di focus:
- qui descrivi le condizioni operative e strategiche necessarie
- non ripetere la tabella numerica completa che verra tradotta in `17. Price map e scenario map`

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
- non usare multipli se il perimetro della metrica non e riconciliato con abbastanza rigore

Regola metodologica obbligatoria:
- se il token non ha un anchor pulito da `holder cash flow`, non forzare una lettura tipo equity e non usare questo come scusa per atterrare automaticamente su `fairly priced`
- in questi casi costruisci comunque una lettura di prezzo disciplinata usando:
  - storico del token in regimi diversi
  - pricing relativo vs competitor comparabili
  - ruolo monetario / collateral / reserve premium, se rilevante
  - scenario map della sezione `17`
  - stato di adozione e qualita della tesi rispetto al prezzo corrente
- l obiettivo non e ottenere un fair value finto al dollaro
- l obiettivo e capire se il prezzo corrente sta sotto, dentro o sopra il range coerente con la tesi base

Domande chiave:
- il mercato sta prezzando crescita ragionevole o euforia?
- il multiplo è giustificato dalla qualità dei ricavi?
- il token è cheap su base relativa, assoluta, o nessuna delle due?

17. Price map e scenario map
Questa sezione deve tradurre la tesi in mappe numeriche.
Non ripetere qui in dettaglio milestone narrative gia spiegate nel `Bull case`.
Calcola cosa significherebbe:
- scenario `base case` coerente con la tesi centrale, non solo bull e bear
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

Chiudi sempre la sezione con un blocco `price placement`:
- `spot anchor` usato per il placement: fonte + timestamp
- prezzo attuale / market cap attuale
- corridoio `base case` ragionevole: `lower bound / mid / upper bound`
- dove cade il prezzo attuale rispetto a quel corridoio:
  - sotto il corridoio
  - dentro la parte bassa
  - circa al centro
  - dentro la parte alta
  - sopra il corridoio
- se il prezzo sta gia prezzando:
  - solo il base case
  - parte del bull case
  - molto del bull case
  - piu del bull case ragionevole

17A. Verdict calibration bridge
Questa sezione e obbligatoria.
Serve a trasformare `16-17` in un verdetto di prezzo disciplinato invece di usare `fairly priced` come categoria di default.

Rispondi in modo secco:
- qual e il `base case` centrale che stai usando davvero
- qual e il corridoio di prezzo coerente con quel `base case`
- quanto il prezzo attuale dista da quel corridoio in modo materialmente rilevante oppure no
- se la tesi e intatta, deteriorata o gia troppo prezzata al prezzo corrente

Classificazione obbligatoria del verdetto:
- `sottovalutato` se:
  - il prezzo corrente sta in modo materialmente sotto la parte bassa del corridoio `base case`
  - e la tesi centrale non e rotta
  - e il mercato non sta solo reagendo a un `structural break` ancora aperto
- `fairly priced` se:
  - il prezzo corrente sta dentro il corridoio `base case`
  - oppure abbastanza vicino da non giustificare una chiamata direzionale strutturale forte
- `sopravvalutato` se:
  - il prezzo corrente sta in modo materialmente sopra la parte alta del corridoio `base case`
  - oppure sta gia prezzando una parte troppo ampia del bull case
- `non analizzabile con rigore sufficiente` se:
  - non riesci a costruire un corridoio minimamente serio per buchi di dati o tesi troppo opaca

Regole dure:
- non richiedere per forza una cheapness da `DCF / equity` per usare `sottovalutato`
- non usare `fairly priced` come sinonimo di:
  - `asset di alta qualita`
  - `mi piace ma non so fare timing`
  - `accumulerei solo piu in basso`
- `fairly priced` significa solo:
  - prezzo attuale dentro il range centrale coerente con la tesi base allo snapshot usato
- usa tolleranza di buon senso coerente con volatilita e confidenza:
  - non promuovere o declassare il verdetto per scarti banali di pochi punti percentuali
- se il prezzo sta nella parte bassa del corridoio ma non abbastanza da chiamarlo `sottovalutato`, dillo esplicitamente:
  - `fairly priced, ma vicino alla parte bassa del range`
- se il prezzo sta nella parte alta del corridoio ma non abbastanza da chiamarlo `sopravvalutato`, dillo esplicitamente:
  - `fairly priced, ma vicino alla parte alta del range`

18. Mispricing test
Questa sezione deve essere una sintesi secca dell errore di pricing.
Non rifare qui il bull case, il bear case o la tabella scenario numerica.
Rispondi in modo secco:
- cosa sta sottovalutando il mercato?
- cosa sta sopravvalutando il mercato?
- qual è la variabile più importante che quasi tutti stanno ignorando?
- dove sta il vero edge dell’analisi?
- cosa sto rischiando di capire male io come analista?
- qual è il vantaggio concreto che regge la tesi anche fuori dalla narrativa crypto, se esiste?

18A. Strongest countercase
Prima di passare alla source reconciliation, stressa la tua tesi con il miglior caso contrario in massimo 6 righe.
Rispondi in modo secco:
- qual è la lettura più forte contro il mio verdict finale?
- quale assunzione del mio framework potrebbe essere sbagliata, incompleta o troppo severa?
- quale singolo sviluppo o dato nei prossimi 90 giorni farebbe apparire questa analisi troppo prudente o troppo aggressiva?
Questo blocco non deve ribaltare artificialmente la tesi: deve testarne la robustezza.

18B. Claim audit residuale
Compila solo per le `1-3` claim piu importanti che muovono davvero la tesi.
Per ciascuna claim indica:
- claim
- evidenza migliore disponibile
- cosa dimostra davvero
- giudizio: supportata / parzialmente supportata / non dimostrata
- implicazione sulla confidenza o sul verdict

19. Residual source divergences
Compila questa sezione solo se emergono divergenze rilevanti tra fonti.
Non ripetere il controllo trasversale `7. Source reconciliation discipline`: qui riporta solo le divergenze residue che cambiano davvero la tesi o la confidenza.
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
- Questa sezione non introduce nuove claim o nuove inferenze: comprime il lavoro gia chiuso nelle sezioni precedenti.
- Mappa minima di derivazione:
  - `business quality` <- `3`
  - `necessità di esistenza del prodotto` <- `2`
  - `necessità del token per il prodotto` <- `4`, `5`
  - `token quality` <- `6`, `7`
  - `token accrual verdict` <- `7A`
  - `founder / team / trust surface` <- `11A`, `CT-13`
  - `market setup` <- `12`, `16`, `17`
  - `regime eventi recente` <- `CT-12`
  - `verdict` <- `16`, `17`, `17A`, `18`, `18A`, `19`
  - `divergenze residue di fonti` <- `19`
- Il `motivo principale del giudizio` deve isolare il tradeoff decisivo che spiega il `verdict`, non ricopiare in miniatura bull case, bear case e scenario map.
- research mode: full diligence / opacity-compressed
- business quality: alta / media / bassa
- necessità di esistenza del prodotto: alta / media / bassa / non dimostrata
- necessità del token per il prodotto: alta / media / bassa / quasi nulla
- token quality: alta / media / bassa
- token accrual verdict: forte / medio / debole / quasi nullo / non dimostrabile
- founder / team / trust surface: buono / neutro / misto / debole / non verificabile
- market setup: favorevole / neutro / fragile
- regime eventi recente: pulito / evento materiale ma transitorio / evento ancora aperto / structural break possibile
- verdict: sottovalutato / fairly priced / sopravvalutato / non analizzabile con rigore sufficiente
- divergenze residue di fonti: nessuna materiale / basse / medie / alte
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
- Nella sezione founder/team, usa solo fatti rilevanti per execution credibility, trust risk o key-person risk.
- Nella sezione founder/team, non fare character judgement gratuito e non usare accuse non dimostrate come scorciatoia analitica.
- Se un dato chiave manca, dillo esplicitamente, spiega perché conta e abbassa la confidenza.
- Se i numeri non bastano, dillo.
- Se manca trasparenza su supply, unlock o treasury, consideralo un rischio.
- Se l asset e troppo opaco per chiudere con rigore waterfall, supply o treasury, comprimi la sezione e alza il rischio analitico invece di moltiplicare `non trovato`.
- Se sei in modalita `opacity-compressed` per buchi critici su waterfall, supply o treasury, non assegnare `confidenza media` o `alta` senza una spiegazione eccezionale e verificabile.
- Se sei in modalita `opacity-compressed`, usa il ramo `2A` come sostitutivo delle sezioni `3-11`; non compilare entrambe le versioni in parallelo.
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
- Per asset liquidi o major, non usare un range aggregato o uno snippet di dashboard come anchor spot finale se una venue/API primaria dice altro in modo materiale.
- Se il prezzo usato in `17. Price map e scenario map` contraddice i range citati nello stesso report, il dato non e riconciliato e va corretto prima del verdict.
- Non usare `fairly priced` come categoria rifugio solo perche il token non ha cash flow holder-level pulito.
- Se il prezzo sta materialmente sotto il tuo `base case corridor` e la tesi resta intatta, devi essere disposto a dire `sottovalutato`.
- Se il prezzo sta materialmente sopra il tuo `base case corridor` o prezza gia troppo bull case, devi essere disposto a dire `sopravvalutato`.
- Non usare il verdetto di prezzo per esprimere il timing operativo di oggi: quel lavoro spetta al prompt trade.
- Per ogni claim forte, chiarisci sempre cosa è dimostrato, cosa è solo suggerito e cosa resta non dimostrato.
- Se mancano fonti primarie o dati sufficienti per una conclusione seria, dichiara il token non analizzabile con rigore sufficiente.
- Se esistono eventi materiali negli ultimi `30d`, dedica sempre loro una sezione separata e non nasconderli dentro `catalizzatori` o `bear case`.
- Non trasformare `Catalizzatori` in una copia di `12. Thesis-change synthesis`.
- Non trasformare `19. Residual source divergences` in una copia del `source reconciliation evidence log`.
- Per eventi recenti usa sempre date assolute, non solo `oggi`, `ieri`, `pochi giorni fa`.
- Distingui sempre tra `evento confermato`, `allegation`, `risposta del team`, `impatto di mercato osservato`.
- Un governance shock, exploit, halt, delisting, key-person exit o rottura con un partner chiave può peggiorare il `market setup` anche se il business di lungo periodo non è ancora rotto.
- L assenza di dati di microstructure avanzata non deve da sola degradare un report a `opacity-compressed` se business, token e valuation restano analizzabili con rigore.
- Questo prompt produce un giudizio di ricerca e fair value strutturale, non un setup operativo di trading multi-timeframe.


## STILE DI RISPOSTA
- Scrivi come se stessi decidendo se allocare capitale tuo.
- Tono freddo, lucido, non promozionale.
- Ogni conclusione deve poggiare su una catena logica esplicita.
- Non proteggere la tesi: prova prima a romperla.
