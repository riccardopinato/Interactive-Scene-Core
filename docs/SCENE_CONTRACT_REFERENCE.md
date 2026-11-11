# Schema-2 — riferimento dell'app originale (non implementazione core)

Fonte normativa e sempre più aggiornata: [Adaptive Landscape — SCENE_CONTRACT.md](https://github.com/riccardopinato/Adaptive-Landscape-Android/blob/main/docs/SCENE_CONTRACT.md).

## Esempio concettuale (dati sintetici)
```json
{"schema":2,"scene":"meadow","columns":5,"rows":8,"top":0.115,"span":0.765,"occupied":[0,5],"zones":[{"x":0.5,"y":0.75,"width":0.25,"height":0.1,"kind":"widget"}],"palette":"original","night":false,"motion":1,"reduceMotion":false}
```

- Coordinate normalizzate [0,1] su canvas (x orizzontale, y verso basso).
- Grid columns 3..8, rows 3..12, `top` [0..0.5], `span` [0.2..(1-top)], indices row-major; cellule centrate.
- `zones`: rettangoli centrati `x/y/width/height`; max 80 nel consumer. Kind icon/widget/dock, non identificativi packages o screenshot. Export non conserva nomi di app.
- Scene `meadow|beach`; palette `original|sunset|mint`; night boolean; motion [0..2], reduceMotion boolean.
- `reduceMotion` o motion zero disabilitano loop continuo, salvo modifiche necessarie.
- `occupied` e zones sono calibrazioni **manuali**; il wallpaper non legge in modo generale le coordinate delle icone Home.

## Invariante Beach
Mare vuoto senza marker, nessuna fascia di sabbia automatica quando `occupied`/zones sono vuoti. L'impostazione dock manuale 0/3/4 vive come zones `kind: 'dock'`.
Le equazioni gaussiane di influenza e la geometria precisa DEVONO essere lette dal file consumer e testate Dart+Kotlin sullo stesso commit; qui si preserva solo un riassunto descrittivo.

## Caveat versione
Lo schema `contracts/scene.design.schema.json` di questo repo è un esperimento di interoperabilità NON canonico e non sostituisce lo schema validato del consumer. Web GPU full framebuffer e Android physical non sono la stessa rendering evidence.
