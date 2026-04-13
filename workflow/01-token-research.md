# Workflow 01: Token Research

Esegui `prompt/token-research-prompt.md` per `[PROTOCOLLO] / [TICKER]`.

Obiettivo operativo:
- crea o riusa la cartella `output/[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test`
- salva l output in `output/[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test/token-research-[SLUG-PROGETTO]-[TICKER-LOWER]-test.md`
- raccogli autonomamente le fonti necessarie
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
