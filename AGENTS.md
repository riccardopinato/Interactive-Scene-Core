# AGENTS — Interactive Scene Core

- Prima del lavoro: risolvi UNA volta App-Factory-Core/CURRENT.yaml, Master e Golden Index/Registry correnti; pin commit. Product Bible e Roadmap del consumer decidono lo scope.
- Il codice sorgente canonico per il renderer attuale resta in Adaptive-Landscape-Android. Questo repository NON deve duplicare versioni divergenti degli stessi file.
- Upstream BLEZZ0102/Deskland GPL-3.0 è sola reference di prodotto; non importare codice/asset senza legal/license gate. Preservare clean-room rewrite e attribuzioni appropriate.
- Test e benchmark Android reale separati da Flutter Web preview e da test unitari; non dichiarare 4K, 60fps, qualità fotorealistica, compatibilità OEM o Play senza evidenze.
- Generic scene-core puro separato da Android-specific `WallpaperService`, Kotlin EGL/GLES, Flutter UI, preferences, app icon cal.
- No accessibilità, screen recording/capture, app packages scanning o permessi sensibili per leggere posizione icone; Android wallpaper non ha API universale in tal senso.
- Il contratto scene Schema-2 upstream è autorevole. Qualunque schema JSON qui è **design adaptation** finché consumer/versioni non vengono sincronizzati da test.
- Prestazioni: riduzione animazione, stop when invisible, energy/thermal QA, CPU/GPU/RAM/FPS/battery e resume. No import di renderer acqua in Notes.
- Ogni modifica: branch/PR, provenienza, licenze e test, source SHA esatto. Device/Store restano NOT_VERIFIED finché non collaudati.
- Snapshot automatico aggiornato SOLO tramite PR da metadata GitHub, non implementa estrazione né certifica componenti.
