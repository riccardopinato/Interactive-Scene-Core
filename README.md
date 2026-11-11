# Interactive Scene Core — riuso grafico Android/Flutter

**ID:** INT-2026-001 · **Stato:** CANDIDATE / EXTRACTION NOT STARTED · **Data:** 11/11/2026.

Questo repository è il futuro modulo grafico riutilizzabile per scene 2D, layout interattivi, gesture, animazioni e (come adattatore opzionale) rendering Android GPU/WallpaperService. **Non è un secondo launcher Deskland e non contiene ancora il renderer estratto dall'app originale**: il prodotto effettivamente sviluppato resta [Adaptive-Landscape-Android](https://github.com/riccardopinato/Adaptive-Landscape-Android).

## Navigazione
- [Product Bible](PRODUCT_BIBLE.md), [Roadmap](ROADMAP.md), [Architecture](docs/ARCHITECTURE.md)
- [Inventario dei file sorgente candidati](docs/EXTRACTION_MAP.md) — path reali del consumer Flutter e Kotlin
- [Scene schema-2 reference](docs/SCENE_CONTRACT_REFERENCE.md) — adattamento descrittivo del contratto esistente, non implementazione
- [Licenze e provenienza](docs/LICENSES_AND_ORIGINS.md) — Deskland GPL-3.0 *reference only*
- [Qualità e test hardware](docs/QUALITY_AND_DEVICE_TEST_MATRIX.md), [Matrice consumer](docs/CONSUMER_MATRIX.md)
- [Evidence](evidence/README.md), [Provenance](docs/PROVENANCE.md), [Auto-update policy](docs/AUTO_UPDATE_POLICY.md)

## Che cosa riutilizzeremo, se validato
Pure scene models (viewport, objects, palette, zones), gesture/pan/zoom/drag interactions, render adapters, lifecycle/quality configuration, performance harness. L'acqua/Beach GPU è un modulo OPTIONAL: niente shader obbligatori in Notes, Anna's Diary o applicazioni non grafiche.

## Provenienza fondamentale
- [Adaptive Landscape](https://github.com/riccardopinato/Adaptive-Landscape-Android) è il code owner del prodotto Flutter + Kotlin Android. Il suo `docs/SCENE_CONTRACT.md` schema-2 è il riferimento normativo prima di ogni estrazione.
- [Deskland originale](https://github.com/BLEZZ0102/Deskland) @ `9818b577402ff476e1b59da07970c56472713126` è GPL-3.0: qui è **soltanto** riferimento di design/UX. NON importare codice/asset originali in questo core destinato a possibili prodotti proprietari, salvo nuova decisione consapevole su licenze e architettura.
- Factory [CURRENT.yaml](https://github.com/riccardopinato/App-Factory-Core/blob/main/CURRENT.yaml); baseline osservata 11/11/2026 `ee72dbb1b0de2cd71bc4aac42c350853c6915159` (Master 27/Golden Index 29).

## Verità di stato
Il Web editor e l'app Android consumer esistono, ma i test visivi/fisici Android sono distinti dalla compilazione CI. Un utente ha respinto la resa dell'acqua e l'identificazione universale delle posizioni Home non esiste nell'API standard WallpaperService; calibrazione manuale. Il core standalone qui è **proposto**, non estratto/testato. Nessun donor E3 o Golden nuovo è certificato.
