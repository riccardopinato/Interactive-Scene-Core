# Architettura proposta — reference e boundaries

```text
Pure scene definitions (Dart or language-neutral JSON schema, TBD)
 ├── scene geometry/viewport/zones/transforms
 ├── deterministic influence algorithms
 └── serialization and validation
           |
           +--> Flutter UI / canvas adapter (optional)
           |       +--> interactive preview & effects (optional)
           |
           +--> Kotlin Android adapter (optional)
                   +--> WallpaperService lifecycle + GL renderer
                   +--> battery/reduced-motion/visibility
```

## Compatibilità
- Lo schema di origine è `docs/SCENE_CONTRACT.md` del consumer, Schema-2.
- `scene-model` non assume posizioni icon package Android, immagini di altre app, permessi.
- `renderer` e `interaction` sono interfacce separabili per dimensione APK, qualità e hardware.
- Kotlin/native e Flutter mantengono test di parità sugli stessi fixtures, non soltanto compile pass.
- Il cambio del grid dimension resetta celle selezionate intenzionalmente nel consumer; la compatibilità migrazioni non va falsificata.

## API future (non implementate)
Scene.validate(); Scene.serialize(); Scene.effectInfluenceAt(x,y); Viewport.transform(); Gesture.hitTest(); Renderer.start/stopOnVisibility(); QualityPreset.selectWithBatteryBudget().
Non documentare queste API come già presenti; sono nomi di design.

## Dati e determinismo
No network/sync requirement; local prefs e import/export JSON solo se i singoli consumer lo richiedono. Gesture e rendering real-time non dovrebbero possedere business state persistito, né imporre un database condiviso.
