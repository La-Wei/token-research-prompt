# Workflow

Questa cartella contiene prompt workflow neutri e riusabili.

File disponibili:
1. [`01-token-research.md`](01-token-research.md)
2. [`02-token-research-verification.md`](02-token-research-verification.md)
3. [`03-token-trade.md`](03-token-trade.md)

Convenzione output:
- cartella: `[slug-progetto]-[ticker-lower]-[YYYY-MM-DD]-test`
- fondamentale: `token-research-[slug-progetto]-[ticker-lower]-test.md`
- verifica: `token-research-[slug-progetto]-[ticker-lower]-verification.md`
- trade: `token-trade-[slug-progetto]-[ticker-lower]-test.md`

I file sono scritti per essere richiamati direttamente come prompt di workflow.
Sostituisci solo i placeholder operativi del token che vuoi analizzare.

## Ordine Consigliato

1. esegui [`01-token-research.md`](01-token-research.md)
2. esegui [`02-token-research-verification.md`](02-token-research-verification.md)
3. esegui [`03-token-trade.md`](03-token-trade.md)

## Cosa Fa Ogni Workflow

### 01 - Token Research
- crea o riusa la cartella output del token
- produce il report fondamentale completo
- segue la metodologia di `prompt/token-research-prompt.md`

### 02 - Token Research Verification
- verifica il report fondamentale con fonti primarie e dashboard metodologicamente chiare
- controlla anche eventi recenti, dispute di governance, shock di mercato e thesis-change events
- non riscrive il fondamentale salvo richiesta esplicita

### 03 - Token Trade
- eredita il contesto dal fondamentale
- preferisce il report di verifica se esiste e se corregge punti materiali
- trasforma la tesi strutturale in una market expression operativa

## Guida Rapida

Per un token `[PROTOCOLLO] / [TICKER]`:
1. sostituisci i placeholder nel workflow scelto
2. usa naming coerente per:
   - `[SLUG-PROGETTO]`
   - `[TICKER-LOWER]`
   - `[YYYY-MM-DD]`
3. mantieni tutti i file dello stesso token nella stessa cartella output

Esempio:
- cartella: `bittensor-tao-2026-04-10-test`
- fondamentale: `token-research-bittensor-tao-test.md`
- verifica: `token-research-bittensor-tao-verification.md`
- trade: `token-trade-bittensor-tao-test.md`
