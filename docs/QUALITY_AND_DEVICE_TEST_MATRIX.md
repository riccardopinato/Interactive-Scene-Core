# Quality, performance e collaudo fisico

## Stato al 11/11/2026
L'app consumer Adaptive Landscape presenta lavori Web e APK CI riportati nei documenti, ma la v0.4 Android ha ricevuto **feedback fisico negativo** su acqua artificiale/pixelata, foam, animazione e interazione rispetto alle icone Home; l'assenza di coordinate reali automatiche è un limite strutturale. Il successivo lavoro GPU sperimentale di PR #13 necessita verifica dello stato di merge/HEAD e nuovo test. La PR #30 è solo documentale.
Non attribuire qui PASS visivo, Android 4K nativo, risparmio batteria certificato, release Play o Donor/Golden.

## Matrice di prova da completare
| Test | Ambiente | Evidence richiesta | Stato |
|---|---|---|---|
| Schema-2 serializzazione e invalid JSON | Dart/Kotlin | fixtures e CI exact SHA | TODO |
| Influenza zero occupazione → sea-only | Dart/Kotlin | pixel/logic tests | TODO |
| Widget/dock bounds & gesture | Flutter editor | widget tests e immagini | TODO |
| Flutter canvas vs shader fallback | Web GPU + fallback | screenshot visual diff | TODO |
| Renderer GLES/fps/frame pacing | Android device | FPS/CPU/GPU e build hash | TODO |
| Screen density, 4K rendering claim | Device reale | framebuffer/trace | TODO |
| Thermal/power saver/visibility | Android OEM | minuti/energia/crash logs | TODO |
| Long-run lifecycle/pause/resume | Android OEM | riproducibilità | TODO |
| Design visual acceptance | Utente | feedback e screenshot riferiti all'APK | TODO |
| Notes/consumer #2 | Flutter prodotto distinto | test integrazione e UX | TODO |

Ogni QA registra source SHA, APK/artifact SHA256, dispositivo e versione OS se autorizzato, scenario, risultato, limiti.
