# Pianeta 3D

Esperienza WebGL in Three.js con pianeta stilizzato, isole luminose e controlli di navigazione.

## Tecnologie
- HTML/CSS per la struttura e lo stile dell'interfaccia.
- JavaScript + [Three.js](https://threejs.org/) (renderer WebGL, shader custom, controlli orbitali).
- Node.js HTTP server semplice (`server.js`) per servire i file statici in locale.

## Avvio locale
1. Installa Node.js (>= 16).
2. Da questa cartella: `node server.js`
3. Apri `http://localhost:8000` nel browser.

## Funzionamento
- Render: `index.html` crea un renderer WebGL, scena, camera e controlli `OrbitControls`.
- Pianeta: mesh sferica con `ShaderMaterial`; uniform custom definiscono isole procedurali e profili poligonali (Home, Islanda, SudAmerica).
- Atmosfera: sfera più grande con shader additivo per alone.
- Stelle: punti distribuiti casualmente attorno alla scena.
- UI: overlay con testo e pulsanti per resettare la vista e mettere in pausa/riavviare la rotazione.
- Responsivo: media query per tablet e mobile, controlli centrati su schermi piccoli.
- Asset: librerie in `libs/` (Three.js, OrbitControls), favicon in `favicon.svg` e `favicon.png`.

## Note
- Se non vedi la favicon, fai un hard refresh (Cmd/Ctrl+Shift+R).
- Aggiungi `.gitignore` con `.DS_Store` prima del push, se lavori su macOS.
