# Roadmap — INT-2026-001
Stato: CANDIDATE EXTRACTION. Nessuno dei cinque maxi-step del core è completo.

## Maxi-step 1 — Audit di provenienza e mappa dipendenze (P0)
- [ ] Pin esatto commit Adaptive Landscape e rileva code owner per ciascun modulo.
- [ ] Analizza contratti Dart/Kotlin, SPDX/licenze per file e asset; distinguere original code vs GPL concept.
- [ ] Registra bug visivi noti e divergenze Web/Android, senza considerare lo stato CI prova fisica.
Gate: source map, license ledger, no GPL contamination.

## Maxi-step 2 — Pure Scene Contract (P0)
- [ ] Estrarre modello puro di viewport/objects/occupancy/serialization con contract tests.
- [ ] Garantire Schema-2 backward compatibility e migrazione dati; niente interruzioni del consumer.
- [ ] Testare invarianti: empty sea-only, zones bounds, normalized coords, no NaN, reduced-motion.
Gate: stessi fixtures in core e Adaptive, senza dipendenza Flutter UI/Android.

## Maxi-step 3 — Rendering and Interaction Adapters (P1)
- [ ] Misurare separatamente Dart Canvas/fragment shader, Kotlin GLES/WallpaperService e fallback.
- [ ] Estrarre solo adattatori con utilizzo comprovato; nessun shader in pure scene-model.
- [ ] Definire gesture/selection library idonea a Notes Vision Board, senza introdurre tracking.
Gate: benchmark prima/dopo, no peso/perms extra a consumer non grafici.

## Maxi-step 4 — Physical QA and visual acceptance (P1)
- [ ] Validare Android su device reali (display/resolution/DPI, FPS, CPU/GPU, RAM, batteria).
- [ ] Regressione visiva acqua/shoreline e Android vs Web; user acceptance per i criteri di realismo.
- [ ] Validare pause/resume, background, adaptive power saving, update/downgrade.
Gate: device evidence per APK/hash e UI baseline; non fingere 4K.

## Maxi-step 5 — Consumer indipendente & Golden admission (P2)
- [ ] Integrare core in app realmente utile (es. Notes canvas) con Product Bible approval.
- [ ] Verificare versionamento pacchetto/semver, consumer build, backwards compatibility.
- [ ] Registrare Donor/Golden con provenance SHA licenza test se soddisfa E3/E5.
Gate: riuso indipendente verificato; nessuna promozione automatica.

## Priorità per estrazione
Partire da scene/interaction math, NON dagli effetti acqua: questi ultimi restano un problema visivo aperto in Adaptive. Nessun cambiamento immediato al codice di produzione consumer.
