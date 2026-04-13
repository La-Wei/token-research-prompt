# Test Prompt: `token-position-setup-prompt.md`

## Input usato
- `[NOME/TICKER]`: `RaveDAO / RAVE`
- Report trade usato:
  - `token-trade-ravedao-rave-test.md`
- Data snapshot principale: `2026-04-13`
- Venue / prodotto scelto:
  - `Binance Futures`
  - `RAVEUSDT perpetual`
- Direzione derivata dal report trade:
  - `short` come lato prioritario da cercare
- Timestamp mercato usato:
  - `2026-04-13 12:02 UTC`
  - `2026-04-13 14:05 Europe/Rome`
- Fonti usate per execution setup:
  - `Binance Futures exchangeInfo`
  - `Binance Futures premiumIndex`
  - `Binance Futures openInterest`
  - `Binance Futures funding history`
  - report trade come contesto operativo prevalente

## Assunzioni prudenziali esplicite
- modalità margine assunta: `isolated`
- leva massima assunta: `2x`
- numero target assunto: `3`
- trigger signal preferito: `mark price`
- preferenza esecutiva: `ordine condizionale`, non `market now`
- collateral disponibile: `non fornito`
- rischio massimo per trade: `non fornito`

---

# Output del prompt

## 0. Execution status
- venue / prodotto: `Binance Futures / RAVEUSDT perpetual`
- tipo di prodotto: `perp`
- direzione richiesta: `short`
- eseguibile su questo venue: `si`
- setup attivo adesso: `no`
- prezzo live o snapshot usato:
  - mark `~8.80395`
  - index `~9.31723`
  - estimated settle `~9.41476`
  - funding `~-0.7148%`
  - time `2026-04-13 12:02 UTC`
- completezza input: `parziale`
- confidenza preliminare: `media`

## 1. Inherited setup
- tesi ereditata dal report trade: `RAVE` resta `sopravvalutato`, ma il chart `1W / 1D` e ancora forte e quindi non autorizza short a mercato.
- bias: `operativo neutral`, con fondamentale negativo.
- lato prioritario da cercare: `short`
- lato con edge maggiore: `nessuno adesso`
- scenario dominante con probabilita stimata: `chop / digestione alta 35%`
- livello o zona di entrata ideale: breakdown sotto `~8.80`, meglio ancora conferma sotto `~7.70`; alternativa secondaria `failed reclaim 9.60-10.00`
- invalidazione: recovery sopra `~9.60-10.00`, invalidazione maggiore sopra `12.00`
- target: `~7.70`, `~6.30`, `~6.00`
- motivo per cui il setup esiste o non esiste: il fondamentale spinge a cercare short, ma funding negativo e perp in sconto rendono sbagliato forzarlo prima del trigger

## 2. Venue logic
- `Binance Futures / RAVEUSDT` e un `USDT-margined perpetual`, quindi permette esposizione `short` diretta senza possedere il token spot.
- L ordine `SELL / SHORT` su questo prodotto apre nuova esposizione ribassista; non vende un saldo spot gia posseduto.
- `Binance Futures` supporta i tipi ordine necessari osservati in `exchangeInfo`: `LIMIT`, `MARKET`, `STOP`, `STOP_MARKET`, `TAKE_PROFIT`, `TAKE_PROFIT_MARKET`, `TRAILING_STOP_MARKET`.
- Il prodotto e `TRADING`, `PERPETUAL`, con:
  - tick size `0.00001`
  - step size `1`
  - min qty `1`
  - min notional `5 USDT`
- Per un asset cosi volatile, `isolated` e piu prudente di `cross`.

## 3. Setup classification
- setup tipo: `breakdown trigger`
- attivo adesso oppure condizionale: `condizionale`
- livello chiave che attiva il trade: `8.78000` su `mark price`
- livello che lo invalida: `9.70000`
- cosa trasformerebbe il setup in `no order`:
  - recupero stabile sopra `~9.60-10.00` prima dell attivazione
  - compressione ulteriore dello sconto perp con breakout sopra `10.00`
  - funding che resta molto negativo ma prezzo che rifiuta il breakdown

## 4. Position sizing
Poiche `rischio massimo` e `collateral` non sono stati forniti, non invento la quantity.
Lascio il sizing come formula compilabile.

- collateral disponibile: `non fornito`
- rischio massimo usato: `risk_budget_usd` non fornito
- leva scelta: `2x isolated`
- entry: `8.78000`
- stop: `9.70000`
- risk per unit:
  - `|8.78000 - 9.70000| = 0.92000 USDT per RAVE`
- quantity raw:
  - `risk_budget_usd / 0.92000`
- quantity rounded:
  - `floor(risk_budget_usd / 0.92000)` per via di `stepSize = 1`
- notional:
  - `8.78000 * floor(risk_budget_usd / 0.92000)`
- margine richiesto:
  - `notional / 2`
- loss a stop:
  - `quantity * 0.92000`

## 5. Target map
Allocazione prudenziale proposta:
- `TP1`: `40%`
- `TP2`: `35%`
- `TP3`: `25%`

Per ciascun target:

`Target 1`
- target price: `7.70000`
- reward per unit:
  - `8.78000 - 7.70000 = 1.08000`
- reward totale:
  - `quantity * 1.08000`
- RR:
  - `1.08000 / 0.92000 = 1.17`
- percentuale di size assegnata: `40%`

`Target 2`
- target price: `6.30000`
- reward per unit:
  - `8.78000 - 6.30000 = 2.48000`
- reward totale:
  - `quantity * 2.48000`
- RR:
  - `2.48000 / 0.92000 = 2.70`
- percentuale di size assegnata: `35%`

`Target 3`
- target price: `6.00000`
- reward per unit:
  - `8.78000 - 6.00000 = 2.78000`
- reward totale:
  - `quantity * 2.78000`
- RR:
  - `2.78000 / 0.92000 = 3.02`
- percentuale di size assegnata: `25%`

## 6. Order ticket
Ticket primario proposto: `ordine condizionale short su breakdown`

- `Direzione`: `sell / short`
- `Venue / Product`: `Binance Futures / RAVEUSDT perpetual`
- `Margin mode`: `isolated`
- `Leverage`: `2x`
- `Order type`: `STOP_MARKET`
- `Entry`: `trigger short sotto breakdown`
- `Trigger`: `8.78000`
- `Limit`: `n.a.` perche `STOP_MARKET`
- `Quantity`: `da compilare = floor(risk_budget_usd / 0.92000)`
- `Reduce-only`: `no`
- `Post-only`: `no`
- `Trigger signal`: `mark`
- `Time in force`: `GTC`

## 7. Protective orders
Questi ordini vanno applicati alla `posizione intera` dopo il fill dell ordine primario, per evitare ambiguita di bracket su una posizione ancora non aperta.

- `Stop loss`
  - tipo ordine: `STOP_MARKET`
  - trigger: `9.70000`
  - trigger signal: `mark`
  - market o limit: `market`
  - reduce-only: `yes`

- `Take profit 1`
  - tipo ordine: `TAKE_PROFIT_MARKET`
  - trigger: `7.70000`
  - trigger signal: `mark`
  - market o limit: `market`
  - reduce-only: `yes`
  - size allocata: `40%`

- `Take profit 2`
  - tipo ordine: `TAKE_PROFIT_MARKET`
  - trigger: `6.30000`
  - trigger signal: `mark`
  - market o limit: `market`
  - reduce-only: `yes`
  - size allocata: `35%`

- `Take profit 3`
  - tipo ordine: `TAKE_PROFIT_MARKET`
  - trigger: `6.00000`
  - trigger signal: `mark`
  - market o limit: `market`
  - reduce-only: `yes`
  - size allocata: `25%`

## 8. Multi-ticket plan
Se basta un ordine singolo, scrivilo esplicitamente.

- ordine singolo sufficiente: `si`
- piano principale:
  - `Ticket A`: `breakdown trigger short` sotto `8.78000`
- alternativa watchlist non primaria:
  - se il prezzo prima rimbalza in `9.60000-10.00000` e viene respinto, il setup puo essere riclassificato come `failed reclaim`
  - in quel caso il ticket va riscritto con entry piu alta e stop diverso; non lo attivo ora per non sovrapporre due bracket sulla stessa idea

## 9. Execution notes
- cosa controllare prima di confermare:
  - che il trigger resti coerente con la struttura `4H`
  - che il perp non chiuda lo sconto troppo in fretta mentre il prezzo recupera `9.60-10.00`
  - che il `mark price` sia il segnale usato per evitare wick sporchi
- quale errore evitare:
  - shortare a mercato solo perche il token e `sopravvalutato`
- quando cancellare l ordine non eseguito:
  - se il mercato recupera e accetta sopra `10.00000`
  - se cambia il regime e lo short non e piu il lato prioritario da cercare
- quando spostare a breakeven, se ha senso:
  - dopo esecuzione di `TP1` o dopo accelerazione pulita sotto `7.70000`
- quando non toccare nulla:
  - se l ordine non si attiva e il mercato resta in chop `8.80-10.00`
  - se il fill avviene ma il prezzo scende in modo ordinato verso i target

## 10. No-order test
- la venue e sbagliata? `no`
- il setup non e attivo? `si`
- il rischio e troppo alto? `non valutabile senza risk budget, ma per struttura si tratta di asset ad alta volatilita`
- la leva e troppo alta? `no, 2x isolated e prudente`
- il book e troppo sottile? `non ideale ma ancora tradabile per size piccole / medie`
- conviene aspettare? `si`

## 11. Decisione finale
- verdict: `ordine condizionale`
- venue corretta: `si`
- tipo ordine corretto: `si`
- size corretta: `no, manca il risk budget`
- leverage appropriata: `si`
- invalidation: `recovery e acceptance sopra 9.70000`, con deterioramento chiaro della tesi short sopra `10.00000`
- target logic: `7.70000 -> 6.30000 -> 6.00000`, coerente con il breakdown scenario del report trade
- motivo principale del verdetto in massimo 3 frasi:
  - Il lato prioritario da cercare resta `short`, ma il report trade non autorizza un ingresso immediato.
  - Su `Binance Futures` il modo corretto di tradurlo e un `breakdown trigger short` condizionale, non uno short a mercato.
  - La quantity non va inventata: appena definisci `risk_budget_usd`, il ticket e gia strutturato e compilabile.
