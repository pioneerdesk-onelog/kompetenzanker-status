# Kompetenzanker · Status

Statusseite für Kompetenzanker (status.kompetenzanker.de), bewusst **außerhalb** des Produktions-Clusters.

- `index.html` fragt live `https://app.kompetenzanker.de/api/status` ab (CORS freigegeben) und liest `data/history.json`.
- `.github/workflows/check.yml` prüft alle 5 Minuten Portal und Website. Bei Zustandswechsel wird `data/history.json` fortgeschrieben; bei Ausfall öffnet sich ein Issue „Störung“ (Mail an den Account), bei Erholung wird es geschlossen.
- Geplante Wartungen und Releases kommen aus der App (`src/lib/releases.ts`), nicht aus diesem Repo.
