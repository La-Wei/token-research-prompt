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

## STRUTTURA OBBLIGATORIA

1. TL;DR iniziale
Apri con un riassunto immediato in massimo 8 righe:
- cos’è il protocollo
- perché il mercato potrebbe averlo prezzato male
- cosa rende interessante il token
- cosa preoccupa di più
- giudizio preliminare

2. Che cosa fa davvero il protocollo
- Spiega in modo semplice ma preciso cosa fa.
- Quale problema risolve davvero.
- Chi lo usa davvero o dovrebbe usarlo.
- Perché esiste onchain invece che offchain.
- Dove sta il vero motore economico del business.
- Quale parte della narrativa è sostanza e quale è packaging.

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
Analizza il setup di mercato del token:
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

11. Holder base e allineamento
- Chi possiede il token: team, fondi, foundation, community, users, whales, partner strategici, mercenari.
- Quanto è concentrata la supply.
- Gli holder sono allineati di lungo periodo o opportunisti.
- Esiste una base di holder forte o solo floating speculativo.
- I maggiori holder sono asset strategici o futuri seller.

12. Catalizzatori
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

13. Bull case
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

14. Bear case
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

15. Valuation thinking
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

16. Price map e scenario map
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

17. Mispricing test
Rispondi in modo secco:
- cosa sta sottovalutando il mercato?
- cosa sta sopravvalutando il mercato?
- qual è la variabile più importante che quasi tutti stanno ignorando?
- dove sta il vero edge dell’analisi?
- cosa sto rischiando di capire male io come analista?

18. Source reconciliation
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

19. Checklist finale di investimento
Concludi con:
- 3 motivi forti per essere bullish
- 3 motivi forti per essere cauti
- 3 segnali che confermerebbero la tesi
- 3 segnali che invaliderebbero la tesi
- 3 metriche da monitorare nei prossimi 90 giorni

20. Conclusione netta
Chiudi sempre con:
- business quality: alta / media / bassa
- token quality: alta / media / bassa
- market setup: favorevole / neutro / fragile
- verdict: sottovalutato / fairly priced / sopravvalutato
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
- Distingui sempre tra business quality, token quality e setup di mercato.
- Distingui chiaramente fatti, inferenze e speculazioni.
- Quando citi un numero importante, indica sempre data/snapshot e periodo di riferimento.
- Se i numeri non bastano, dillo.
- Se manca trasparenza su supply, unlock o treasury, consideralo un rischio.
- Ragiona prima sul business, poi sul token, poi sul prezzo.
- Cerca di distruggere la tesi prima di confermarla.
- Evita bias da narrativa, bull market, brand e community.
- Sii severo con i token che hanno unlock pesanti, utility vaga o value accrual indiretto.
- Se il token non ha value accrual reale, dillo chiaramente.
- Se gli unlock sono un problema, dillo chiaramente.
- Se la market structure è fragile, dillo chiaramente.
- Meglio un “non lo so” onesto che una conclusione finta.
- Non confondere mai fees, protocol revenue, holders revenue, buyback budget, burn, treasury custody e riduzione del float.
- Se non puoi dimostrare il meccanismo, non usare parole come “deflattivo”, “supply shock”, “mangiano l’offerta” o equivalenti.
- Se una metrica diverge da un’altra, verifica prima definizioni e perimetro, poi concludi.
- Non confrontare market cap, FDV e multipli attuali con metriche economiche di periodi incompatibili senza normalizzazione o nota esplicita.
- Per ogni claim forte, chiarisci sempre cosa è dimostrato, cosa è solo suggerito e cosa resta non dimostrato.

## STILE DI RISPOSTA
- Scrivi come se stessi decidendo se allocare capitale tuo.
- Tono freddo, lucido, non promozionale.
- Ogni conclusione deve poggiare su una catena logica esplicita.
- Non proteggere la tesi: prova prima a romperla.
