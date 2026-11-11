# Inventario reale del consumer Adaptive Landscape — 11/11/2026

Tree public `main` letto e non troncato al momento della ricognizione. Le path qui sono **presenti nel consumer**, NON copiate in questo repository.

| Path nel consumer | Responsabilità candidata | Decisione |
|---|---|---|
| `docs/SCENE_CONTRACT.md` | Schema-2 normative | SOURCE, preservare |
| `lib/core/landscape_config.dart` | Scene config | ANALYZE/EXTRACT_CANDIDATE |
| `lib/core/icon_field.dart` | Influenza posizioni/griglia | ANALYZE/EXTRACT_CANDIDATE |
| `lib/core/animation_timing.dart` | Animazione/performance | ANALYZE/EXTRACT_CANDIDATE |
| `lib/core/beach_coast.dart` | Linea di costa | OPT-IN EFFECT |
| `lib/core/beach_mask.dart` | Mask influenza | OPT-IN EFFECT |
| `lib/core/ocean_tone_atlas.dart` | Palette/acqua | OPT-IN EFFECT, visual QA pending |
| `lib/core/profile_store.dart` | Persistenza profili | CONSUMER-SPECIFIC |
| `lib/platform/wallpaper_channel.dart` | Flutter↔Android | CONSUMER-SPECIFIC |
| `lib/ui/scene_painter.dart` | Flutter Canvas | POSSIBLE RENDER ADAPTER |
| `lib/ui/beach_surface.dart` | Canvas water | OPTIONAL, cannot assume visual ready |
| `lib/ui/beach_gpu_surface.dart` | GPU surface | OPTIONAL, cannot assume device parity |
| `shaders/beach_ocean.frag` | GPU water shader | OPTIONAL, user visual acceptance pending |
| `android/app/src/main/kotlin/it/riccardopinato/adaptivelandscape/AdaptiveWallpaperService.kt` | Lifecycle | ANDROID SPECIALIZED |
| `android/app/src/main/kotlin/it/riccardopinato/adaptivelandscape/CoastalBeachRenderer.kt` | Native renderer | ANDROID SPECIALIZED |
| `android/app/src/main/kotlin/it/riccardopinato/adaptivelandscape/WallpaperState.kt` | Native config | ANDROID SPECIALIZED |
| `android/app/src/main/kotlin/it/riccardopinato/adaptivelandscape/MainActivity.kt` | Channel/UI wrapper | NOT GENERIC |

**Non importare tutto**. Verificare dipendenze di import, vendored code e asset licensing per file, source commit, benchmark e regressione. Una semplice copia non è Golden/Donor.
