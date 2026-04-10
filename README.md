# Token Prompt

Repository di prompt per fare:
- ricerca fondamentale su token crypto
- analisi di tokenomics, value accrual e market structure
- valutazione operativa separata tra spot / positional / swing / no trade

File principali:
- [prompt/token-research-prompt.md](prompt/token-research-prompt.md)
- [prompt/token-trade-prompt.md](prompt/token-trade-prompt.md)
- [workflow/README.md](workflow/README.md)
- [workflow/01-token-research.md](workflow/01-token-research.md)
- [workflow/02-token-research-verification.md](workflow/02-token-research-verification.md)
- [workflow/03-token-trade.md](workflow/03-token-trade.md)

## Struttura Del Repo

Il repo ora e diviso in due livelli:
- prompt base nella cartella `prompt/`:
  - `prompt/token-research-prompt.md`
  - `prompt/token-trade-prompt.md`
- workflow pronti all uso:
  - `workflow/01-token-research.md`
  - `workflow/02-token-research-verification.md`
  - `workflow/03-token-trade.md`

I prompt base definiscono la metodologia.
I workflow sono gli entrypoint consigliati quando vuoi eseguire il processo in modo ripetibile su un token specifico.

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

### `prompt/token-research-prompt.md`

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

### `prompt/token-trade-prompt.md`

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
1. usa [workflow/01-token-research.md](workflow/01-token-research.md) per creare il report fondamentale completo su un token
2. usa [workflow/02-token-research-verification.md](workflow/02-token-research-verification.md) per verificare il report con fonti primarie, metriche live e audit degli eventi recenti
3. solo dopo usa [workflow/03-token-trade.md](workflow/03-token-trade.md) per derivare la migliore espressione operativa
4. se i dati sono incompleti o un evento materiale e ancora aperto, preferisci `confidenza bassa` o `no trade`

Se vuoi lavorare direttamente sui prompt metodologici, puoi ancora usare:
- [prompt/token-research-prompt.md](prompt/token-research-prompt.md)
- [prompt/token-trade-prompt.md](prompt/token-trade-prompt.md)

Ma la modalita consigliata e usare i file nella cartella `workflow`.

## Guida Rapida D Uso

Sequenza consigliata per un token `[PROTOCOLLO] / [TICKER]`:
1. esegui `workflow/01-token-research.md`
2. ottieni una cartella output nel formato:
   - `[slug-progetto]-[ticker-lower]-[YYYY-MM-DD]-test`
3. esegui `workflow/02-token-research-verification.md` sulla stessa cartella
4. esegui `workflow/03-token-trade.md` usando il report fondamentale e, se presente, il report di verifica

Convenzione output:
- cartella: `[slug-progetto]-[ticker-lower]-[YYYY-MM-DD]-test`
- fondamentale: `token-research-[slug-progetto]-[ticker-lower]-test.md`
- verifica: `token-research-[slug-progetto]-[ticker-lower]-verification.md`
- trade: `token-trade-[slug-progetto]-[ticker-lower]-test.md`

Esempio:
- cartella: `bittensor-tao-2026-04-10-test`
- fondamentale: `bittensor-tao-2026-04-10-test/token-research-bittensor-tao-test.md`
- verifica: `bittensor-tao-2026-04-10-test/token-research-bittensor-tao-verification.md`
- trade: `bittensor-tao-2026-04-10-test/token-trade-bittensor-tao-test.md`

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
