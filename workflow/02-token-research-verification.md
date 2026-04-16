# Workflow 02: Token Research Verification

Esegui la verifica del report fondamentale per `[PROTOCOLLO] / [TICKER]`.

Input obbligatorio:
- report da verificare: `output/[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test/token-research-[SLUG-PROGETTO]-[TICKER-LOWER]-test.md`
- prompt base di riferimento: `prompt/token-research-prompt.md`

Obiettivo operativo:
- crea `output/[SLUG-PROGETTO]-[TICKER-LOWER]-[YYYY-MM-DD]-test/token-research-[SLUG-PROGETTO]-[TICKER-LOWER]-verification.md`
- usa fonti primarie, docs ufficiali e dashboard metodologicamente chiare
- verifica claim strutturali, waterfall, supply, unlock, treasury, metriche live, eventi recenti, `token accrual verdict`, founder / team / trust surface, `source reconciliation` residua e verdetto finale
- verifica sempre che `spot price` e `market cap` del report originale siano coerenti con uno snapshot `same-day` e con almeno una fonte spot primaria per asset liquidi; se il report miscela tick live, close `EOD` e range aggregati, segnalalo come errore materiale
- se le dashboard divergono materialmente, preferisci venue/API spot primaria per il prezzo, `CoinGlass` per derivati e dashboard aggregate tipo `CoinGecko` / `CoinMarketCap` per contesto storico e venue mix
- verifica sempre, se rilevante, identita pubblica del founder / team, track record precedente, controversie reputazionali materiali, key-person risk e implicazione analitica sulla tesi
- nella verifica founder / team separa sempre:
  - `fatto verificabile`
  - `implicazione analitica`
  - `cosa resta non dimostrato`
- non usare etichette come `scammer`, `fraud`, `rugger` o equivalenti senza evidenza primaria molto forte, filing, sentenze, ammissioni o documentazione schiacciante; se il quadro e grave ma non chiuso, usa formule come `track record fortemente controverso` o `trust risk alto`
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
- se il report originale usa `full diligence` o `opacity-compressed`, verifica se quella scelta metodologica era coerente o se il report andava classificato diversamente
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
- `Verifica del perimetro metodologico`
- `Fonti usate per la verifica`
- `Eventi recenti verificati`
- `Verifica founder, team e trust surface`
- `Confermato`
- `Da correggere o aggiornare`
- `Parzialmente confermato, ma non chiuso con rigore pieno`
- `Source reconciliation residua`
- `Valutazione del giudizio finale`
- `Sintesi finale`

Parametri da sostituire:
- `[PROTOCOLLO]`
- `[TICKER]`
- `[SLUG-PROGETTO]`
- `[TICKER-LOWER]`
- `[YYYY-MM-DD]`
