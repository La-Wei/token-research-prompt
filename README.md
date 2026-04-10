# Token Prompt

Repository di prompt per fare:
- ricerca fondamentale su token crypto
- analisi di tokenomics, value accrual e market structure
- valutazione operativa separata tra spot / positional / swing / no trade

File principali:
- [token-research-prompt.md]
- [token-trade-prompt.md]

## Scopo

Questo repository e pensato come strumento di ricerca e supporto analitico.
Serve a strutturare meglio il ragionamento, non a sostituire:
- verifica manuale dei dati
- judgment discrezionale
- risk management
- due diligence

L'obiettivo non e produrre verita automatiche, ma ridurre il caos analitico e costringere il modello a ragionare in modo piu disciplinato.

## Cosa Non E

Questo repository **non** e:
- consulenza finanziaria
- raccomandazione personalizzata di investimento
- gestione di portafoglio
- segnale operativo affidabile per definizione
- sostituto di ricerca primaria

Niente in questo repository deve essere interpretato come:
- `compra questo token`
- `vendi questo token`
- `shorta questo token`
- `questo salira sicuramente`
- `questo scendera sicuramente`

Anche quando un output conclude `sottovalutato`, `sopravvalutato`, `spot accumulate`, `swing long` o `swing short`, resta sempre un output probabilistico, fallibile e dipendente dai dati forniti.

## Avviso Importante

I modelli AI possono:
- allucinare
- leggere male un dato
- confondere definizioni simili
- trattare metriche non comparabili come se fossero comparabili
- esprimere conclusioni troppo sicure con dati incompleti
- dare risposte opposte partendo da un singolo input errato

Nel contesto crypto, basta anche **un solo dato letto male** per cambiare completamente il verdetto.

Esempi tipici:
- confondere `fees` con `protocol revenue`
- confondere `buyback` con `burn`
- confondere `circulating supply` con `liquid float`
- confondere `TVL` con `AUM`
- confondere `token sopravvalutato` con `buon short`
- confondere `progetto valido` con `token investibile`

Un singolo errore su:
- unlock
- treasury
- waterfall dei ricavi
- venue liquidity
- open interest
- funding
- borrow cost
- perimetro delle metriche

puo portare a una conclusione completamente diversa o addirittura opposta.

## Regola Base

Non usare mai l'output del modello come unica base per allocare capitale.

Questo materiale va usato come:
- checklist
- strumento di ricerca
- framework per stressare una tesi
- supporto alla raccolta e organizzazione delle informazioni

Non va usato come:
- motore decisionale autonomo
- sostituto della verifica delle fonti
- conferma automatica di una view gia desiderata

## Limiti Specifici Dei Prompt

### `token-research-prompt.md`

Questo prompt serve per:
- business quality
- token quality
- tokenomics
- value accrual
- mispricing strutturale

Non serve per:
- timing di entrata preciso
- execution di breve
- lettura fine dei grafici
- gestione tattica del rischio intraday

### `token-trade-prompt.md`

Questo prompt serve per:
- lettura multi-timeframe
- bias operativo
- spot / positional / swing expression
- invalidazione della tesi
- qualita di esecuzione

Non garantisce:
- interpretazione corretta del chart
- correttezza dei livelli se gli screenshot sono incompleti
- accesso a dati completi su OI, funding, borrow o liquidita

## Buone Pratiche D'Uso

Prima di fidarti di un output:
- verifica i numeri importanti su fonti primarie o almeno metodologicamente chiare
- controlla data e periodo di riferimento di ogni metrica
- ricontrolla sempre supply, unlock, treasury e waterfall dei ricavi
- controlla se TVL, AUM, deposits o volume stanno davvero misurando la stessa cosa
- controlla se il token e davvero eseguibile lato spot o derivati
- chiediti sempre quale singola assunzione, se sbagliata, ribalterebbe la tesi

Se usi il prompt trade:
- fornisci chart puliti e recenti
- includi piu timeframe
- non aspettarti precisione se mancano dati su funding, OI, liquidita o borrow
- tratta `no trade` come un output valido, non come un fallimento

## Modalita Consigliata

Workflow suggerito:
1. usa [token-research-prompt.md] per capire se il progetto e il token meritano attenzione
2. verifica manualmente le assunzioni critiche
3. solo dopo usa [token-trade-prompt.md] per capire se esiste una buona espressione operativa
4. se i dati sono incompleti, preferisci `confidenza bassa` o `no trade`

## Su Dati E Fonti

L'output dipende totalmente dalla qualita dei dati in input.

Se i dati sono:
- vecchi
- incompleti
- mal definiti
- riconciliati male
- presi da dashboard con metodologie diverse

allora anche il risultato puo essere:
- fuorviante
- fragile
- internamente coerente ma sbagliato
- opposto alla realta economica del token

## Su Bias E Overconfidence

Un LLM puo sembrare molto convincente anche quando sbaglia.

Questo e particolarmente pericoloso quando:
- il testo e ben scritto
- la narrativa e forte
- il token e popolare
- il mercato e in trend
- l'utente cerca conferma e non confutazione

Per questo motivo, il repo va usato per:
- rompere la tesi
- evidenziare buchi informativi
- aumentare la disciplina

non per:
- giustificare una posizione gia presa
- trasformare storytelling in ricerca

## Nessuna Garanzia

Non ci sono garanzie su:
- accuratezza
- completezza
- aggiornamento
- correttezza metodologica
- idoneita per un caso specifico

Chi usa questi prompt si assume la responsabilita di:
- verificare i dati
- valutare i rischi
- decidere autonomamente se e come agire

## Disclaimer Finale

Questo repository e solo a scopo informativo, educativo e di ricerca.

Non costituisce consulenza finanziaria, investimento consigliato, offerta, sollecitazione o raccomandazione personalizzata.

Le risposte generate da modelli AI possono contenere errori, omissioni, semplificazioni e allucinazioni.

Anche un singolo dato sbagliato, letto male o definito in modo ambiguo puo produrre conclusioni completamente sbagliate o opposte.

Usa questi prompt come supporto alla ricerca, non come sostituto della ricerca.
