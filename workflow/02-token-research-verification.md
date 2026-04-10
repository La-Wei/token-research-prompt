# Workflow 02: Token Research Verification

Esegui la verifica del report fondamentale per `[PROTOCOLLO] / [TICKER]`.

Input obbligatorio:
- report da verificare: `[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test/token-research-[SLUG-PROGETTO]-[TICKER-LOWER]-test.md`
- prompt base di riferimento: `prompt/token-research-prompt.md`

Obiettivo operativo:
- crea `[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test/token-research-[SLUG-PROGETTO]-[TICKER-LOWER]-verification.md`
- usa fonti primarie, docs ufficiali e dashboard metodologicamente chiare
- verifica claim strutturali, waterfall, supply, unlock, treasury, metriche live, eventi recenti e verdetto finale
- verifica sempre gli ultimi `7d`, `30d` e `90d`, se rilevanti, per:
  - governance dispute
  - founder / team departure
  - exploit / halt / outage / security incident
  - listing / delisting / partner loss
  - emission, tokenomics, treasury o parameter changes
- separa sempre:
  - `evento confermato`
  - `allegation o claim non dimostrato`
  - `risposta del team / fonte primaria`
  - `market reaction osservata`
- se un evento materiale cambia `market setup`, `token quality` o `verdetto finale`, dichiaralo esplicitamente
- separa sempre:
  - `confermato`
  - `da correggere o aggiornare`
  - `parzialmente confermato ma non chiuso con rigore pieno`
- se trovi errori materiali, indica con precisione quali punti del report originale vanno corretti
- non riscrivere il report fondamentale originale salvo richiesta esplicita
- non limitarti a un riassunto in chat
- al termine rispondi solo con il path finale del file creato

Struttura minima richiesta del file di verifica:
- `Verification Audit`
- `Data di verifica`
- `Esito sintetico`
- `Fonti usate per la verifica`
- `Eventi recenti verificati`
- `Confermato`
- `Da correggere o aggiornare`
- `Parzialmente confermato, ma non chiuso con rigore pieno`
- `Valutazione del giudizio finale`
- `Sintesi finale`

Parametri da sostituire:
- `[PROTOCOLLO]`
- `[TICKER]`
- `[SLUG-PROGETTO]`
- `[TICKER-LOWER]`
- `[YYYY-MM-DD]`
