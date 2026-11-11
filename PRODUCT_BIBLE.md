# Product Bible — Interactive Scene Core
Design v0.1 — 11/11/2026

## Obiettivo
Fornire componenti ottimizzati e portabili per scene 2D interattive in app Android/Flutter senza ricostruire ogni volta viewport, transforms, geometry, gesture handling e performance controls.

## Target & consumer
1. **Adaptive Landscape Android** — consumer originario che ha codice già esistente; mantenere source compatibilita e debug.
2. **Notes Ecosistema / Vision Board** — possibile consumer di selezione/drag/resize/pan/zoom, senza rendering WallpaperService o acqua.
3. **Giochi leggeri/piccoli mondi** — possibile game adaptation; usare engine specializzato se più adatto, non forzare scene-core.
4. **Interfacce educative e launcher** — eventuali consumer successivi, con permessi Android trattati a parte.

## Moduli proposti
- `scene-model`: entities, viewport, transforms, normalized coordinates, z-order, state serialization.
- `interaction`: pan/zoom/drag/touch feedback, snapping e selection in API portabile.
- `renderer-adapter`: Flutter Canvas/CustomPainter/fragment shader opzionale.
- `android-native-adapter`: Kotlin GLES/WallpaperService solo per prodotti che lo richiedono.
- `effects`: particles/water/ambient animation opzionali, non parte del core minimo.
- `benchmarking`: standard GPU/frame pacing/thermal/battery & reduced-motion.

## Principi
No second App, no copy-paste fork, no architettura cross-platform improvvisata. Pattern riutilizzabile deve ridurre duplicazione in consumer reale, non aumentare dimensioni/perms in tutti gli APK.
Portabilità e qualità visiva sono obiettivi da verificare, non attributi già ottenuti.

## Esclusioni e sicurezza
Non automatizzare il rilevamento Home icons attraverso API non esistenti o permessi invasivi; nessuna cattura dello schermo, tracking di altre app, Accessibility/overlay senza specifica futura approvata. Non replicare asset/codice GPL di Deskland in progetti chiusi.
