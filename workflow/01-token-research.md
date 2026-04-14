# Workflow 01: Token Research

Esegui `prompt/token-research-prompt.md` per `[PROTOCOLLO] / [TICKER]`.

Obiettivo operativo:
- crea o riusa la cartella `output/[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test`
- salva l output in `output/[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test/token-research-[SLUG-PROGETTO]-[TICKER-LOWER]-test.md`
- raccogli autonomamente le fonti necessarie
- per asset liquidi o major, riconcilia sempre `spot price` e `market cap` con uno snapshot `same-day` e timestamp esplicito; non usare come anchor finale un singolo widget live o un range aggregato se diverge da venue/API primarie
- se `CoinGecko`, `CoinMarketCap`, `CoinGlass` o altre dashboard divergono materialmente sullo spot, trattalo come `source reconciliation` e preferisci per il prezzo una venue/API spot primaria; usa le dashboard aggregate soprattutto per contesto storico, venue mix o metriche secondarie
- se il prompt richiede `source discovery`, `claim audit`, `metric perimeter reconciliation`, `recent event evidence log` o `source reconciliation`, eseguili davvero e non lasciarli impliciti
- se l asset e troppo opaco per il ramo completo, applica il ramo `opacity-compressed` del prompt invece di riempire il report con pseudo-precisione
- compila il report completo seguendo rigorosamente `prompt/token-research-prompt.md`
- non limitarti a un riassunto in chat
- al termine rispondi solo con il path finale del file creato

Parametri da sostituire:
- `[PROTOCOLLO]`
- `[TICKER]`
- `[SLUG-PROGETTO]`
- `[TICKER-LOWER]`
- `[YYYY-MM-DD]`
