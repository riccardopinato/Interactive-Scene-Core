# Matrice consumer e strategia di riuso

| Consumer | Funzione pertinente | Stato | Rischio |
|---|---|---|---|
| [Adaptive Landscape](https://github.com/riccardopinato/Adaptive-Landscape-Android) | scenes, beach/shader, wallpaper, manual occupancy | codice in repository originario; estrazione NOT_STARTED | High: Android lifecycle / visual acceptance |
| [Notes-Ecosistema](https://github.com/riccardopinato/Notes-Ecosistema) | canvas drag/pan/zoom, oggetti/z-order, vision board | proposta/da confrontare con motori canvas già presenti | Medium: evitare duplicazione |
| Anna's Diary | eventuali visualizzazioni personali leggere | nessuna integrazione approvata | Low relevance: mantenere leggerezza |
| Giochi leggeri/ambienti 2D | scene/animations/objects | candidate | Medium: non reinventare un engine game |
| Launcher Android autonomo | interactive wallpaper scenes | prodotto diverso, non autorizzato | High: permissions, UX e Play policy |
| App educative | interazioni oggetti | candidate | Low-to-medium |

Regola: richiedere Product Bible/roadmap consentite e analisi delta. Se un consumer ha già un'implementazione migliore, **non importare il core**. Il motore effetti acqua non è requisito per UI Notes.
