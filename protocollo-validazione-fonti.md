# Protocollo di Validazione delle Fonti

> Protocollo personale e riutilizzabile per validare le fonti usate in qualsiasi
> report di ricerca di questo repository. Versione 1.0 — 18 giugno 2026.

## 1. Scopo

Stabilire un metodo ripetibile e tracciabile per decidere **quanto fidarsi** di
ogni affermazione (claim) presente in un report, in base alla qualità e
all'indipendenza delle fonti che la sostengono.

## 2. Principi guida

1. **Primarietà prima di tutto**: una fonte primaria (documento ufficiale, dato
   originale) vale più di mille rilanci.
2. **Corroborazione indipendente**: un claim è solido solo se confermato da
   **≥2 fonti indipendenti** tra loro (che non si copino a vicenda).
3. **Le discrepanze si dichiarano, non si nascondono**: se le fonti divergono,
   il report deve riportarlo esplicitamente.
4. **Tracciabilità**: ogni claim deve essere collegabile alla/e fonte/i che lo
   sostiene/sostengono.
5. **Trasparenza dei limiti**: se una fonte non è accessibile (es. paywall, 403),
   lo si annota e si cerca corroborazione alternativa.

## 3. Gerarchia (tier) delle fonti

| Tier | Tipo | Esempi | Peso |
|------|------|--------|------|
| **T1 — Primaria** | Documento originale ufficiale | Deposito SEC (8-K/10-Q), comunicato Investor Relations, trascrizione earnings call, sito ufficiale dell'azienda | Massimo |
| **T2 — Secondaria autorevole** | Testata giornalistica/finanziaria affidabile con redazione | CNBC, Reuters, Bloomberg, TechCrunch, Financial Times | Alto |
| **T3 — Aggregatore / analisi** | Riepiloghi, blog finanziari, aggregatori dati | StockAnalysis, StockTitan, TIKR, Seeking Alpha, Benzinga | Medio |
| **T4 — Debole** | Fonte anonima, promozionale, SEO, social non verificato | Siti di "trading tips", post social, contenuti senza autore | Basso / solo indizio |

## 4. Checklist per singola fonte (8 controlli)

Per ogni fonte si verifica:

1. **Provenienza** — chi pubblica? È identificabile e affidabile?
2. **Primarietà** — è originale (T1) o un rilancio (T3/T4)?
3. **Data/Attualità** — è recente e pertinente al periodo del claim?
4. **Indipendenza** — è davvero distinta dalle altre fonti citate, o le ricopia?
5. **Corroborazione** — esistono ≥2 fonti indipendenti che concordano?
6. **Verificabilità** — il dato è risalibile a un documento primario?
7. **Conflitto di interesse** — la fonte ha interesse a far salire/scendere il titolo?
8. **Accessibilità** — la fonte è consultabile? Se no, è annotato e sostituito?

## 5. Scala di confidenza (esito)

| Livello | Criterio |
|---------|----------|
| 🟢 **ALTA** | Confermato da ≥1 fonte T1, **oppure** ≥2 fonti T2 indipendenti e concordi. Nessuna discrepanza rilevante. |
| 🟡 **MEDIA** | Sostenuto da fonti T2/T3 ma senza primaria, oppure corroborazione parziale. Da trattare come "plausibile". |
| 🔴 **BASSA** | Una sola fonte T3/T4, oppure fonti in **contraddizione** tra loro. Da segnalare come incerto / da verificare. |

## 6. Regole decisionali

- **Claim numerico/finanziario** (ricavi, utenti, prezzi, target): richiede almeno
  **una fonte T1** o, in mancanza, **due fonti T2 indipendenti**. Altrimenti → 🟡/🔴.
- **Dato di mercato volatile** (prezzo azione, % giornaliera, target price): da
  **verificare in tempo reale**; nel report si indica come indicativo.
- **Discrepanza tra fonti**: l'affermazione scende automaticamente a 🔴 sul punto
  specifico in conflitto, e la divergenza va **scritta** nel report.
- **Fonte non accessibile** (403/paywall): non squalifica il claim, ma impone di
  cercare **corroborazione alternativa**; se non trovata → declassa di un livello.
- **Conflitto di interesse evidente** (es. fonte promozionale): declassa di un livello.

## 7. Output atteso

L'applicazione del protocollo produce una **tabella di validazione** che, per ogni
claim chiave, riporta: fonte/i, tier, esito di confidenza e note (incluse le
discrepanze). Vedi esempio applicato in `validazione-fonti-snap.md`.
