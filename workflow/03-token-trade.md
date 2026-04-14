# Workflow 03: Token Trade

Esegui `prompt/token-trade-prompt.md` per `[PROTOCOLLO] / [TICKER]`.

Input primario obbligatorio:
- report fondamentale: `output/[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test/token-research-[SLUG-PROGETTO]-[TICKER-LOWER]-test.md`
- report di verifica: `output/[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test/token-research-[SLUG-PROGETTO]-[TICKER-LOWER]-verification.md`, se disponibile
- prompt trade di riferimento: `prompt/token-trade-prompt.md`

Obiettivo operativo:
- usa il report fondamentale come contesto ereditato
- se esiste il file di verifica, trattalo come layer di controllo aggiuntivo e preferiscilo in caso di conflitti
- se il file di verifica segnala `evento materiale`, `shock di governance`, `exploit`, `delisting risk` o `structural break possibile`, portalo dentro il bias operativo prima di leggere il chart come se nulla fosse
- non rifare da zero business quality, token quality, tokenomics, unlock analysis o right-to-exist test
- fai source discovery per chart, timeframe, liquidita, OI, funding e positioning se non ti vengono forniti
- per asset liquidi o major, fai prima source discovery su venue/API primarie spot e perp e usa da li `spot anchor`, `OHLC` e microstructure
- non costruire trigger o livelli da range aggregati `7d / 30d` di dashboard se esistono `OHLC` reali ragionevolmente accessibili
- se non ottieni `OHLC` primari su `4H / 1H / 15m`, abbassa la confidenza sul timing e non fingere precisione numerica su trigger, invalidazione o microstruttura
- separa sempre:
  - `bias investment / long-term`
  - `bias 1W`
  - `bias 1D`
  - `bias operativo`
- verifica sempre se il setup attuale e guidato da:
  - price action tecnica ordinaria
  - repricing da evento recente
  - dislocazione ancora aperta e non risolta
- chiudi sempre in modo coerente:
  - `lato prioritario da cercare`
  - `lato con edge maggiore adesso`
  - `lato candidato all attivazione`
  - `stato del setup tattico: attivo / condizionale / watchlist / no-trade`
- crea `output/[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test/token-trade-[SLUG-PROGETTO]-[TICKER-LOWER]-test.md`
- segui rigorosamente la struttura obbligatoria di `prompt/token-trade-prompt.md`
- non limitarti a un riassunto in chat
- al termine rispondi solo con il path finale del file creato

Parametri da sostituire:
- `[PROTOCOLLO]`
- `[TICKER]`
- `[SLUG-PROGETTO]`
- `[TICKER-LOWER]`
- `[YYYY-MM-DD]`
