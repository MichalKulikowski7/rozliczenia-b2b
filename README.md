# Rozliczenia JDG — backup aplikacji

- `rozliczenia-jdg.html` — źródło strony opublikowanej jako artefakt na claude.ai (Rozliczenia JDG). Każda publikacja = jeden commit.
- `data-export.json` — eksport bazy artefaktu (settings, invoices, payments, checklists) z chwili commitu.
- Plik HTML otwarty lokalnie pokaże pustą aplikację: dane żyją w bazie artefaktu (`claude.use("db")`), poza przeglądarką claude.ai niedostępnej.
- Token API Fakturowni nigdy nie jest w tym repo — jest tylko w localStorage przeglądarki.

Odtworzenie: opublikować `rozliczenia-jdg.html` jako artefakt z capabilities `{db:{}, user:{}}`, a dane wgrać z `data-export.json` przez ArtifactData (set per dokument).
