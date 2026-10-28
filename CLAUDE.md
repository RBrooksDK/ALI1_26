# ALI1_26 – Applied Linear Algebra

Kursusside (engelsk) for ALI1, et af minimumskurserne for at søge ind på AU's kandidatuddannelse.

## Struktur

- Sessioner `01_Introduction_to_Linear_Algebra` til `12_Recap_and_Conclusion`; sessionerne 10 og 11 deler emnet Symmetric Matrices, SVD and PCA.
- Hver session er én `README.md` med `## Session Material` (links til Recap and Exercises og Session Notes på Google Drive, Session Material på SharePoint), `### Session Recording`, `## Session Description`, `### Key Concepts` og `## Exercises`.
- Ingen Tutorial-filer eller notebooks pr. session. `pages/recordings.md` samler optagelserne.

## Konfiguration, der afviger fra den globale opsætning

- `site_dir: ../site`, dvs. `C:\GitHub\site`, som deles med MSU1_26 og STA_26. Byg til en anden mappe (`mkdocs build --strict -d <mappe>`), hvis flere sites bygges efter hinanden.
- Ingen `mkdocs-jupyter`.
- Ingen `.gitignore`. Pas på ikke at committe `.venv/` eller byggeoutput.
- Den lokale `.venv` er i stykker (dens launcher peger på `OneDrive - ViaUC\Arbejde\GitHub\ALI1_25\.venv`). Byg med den globale `mkdocs`, indtil den er genskabt.
