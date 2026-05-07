# Changelog

Tots els canvis notables d'aquest projecte es documenten en aquest fitxer.

El format segueix [Keep a Changelog](https://keepachangelog.com/ca/1.0.0/),
i el projecte segueix [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] - 2026-05-07

### ✨ Afegit

**Mode Presentador**
- Bombo virtual amb extracció aleatòria del 1 al 90
- 90 frases típiques catalanes per a cada número
- Graella visual dels 90 números amb marcatge dels sortits
- Historial dels últims 6 números extrets
- Mode correcció manual activable amb triple clic (desactivat per defecte)
- Confeti en acabar la partida

**Mode Participant**
- Generació de cartrons aleatoris (sense límit de cartrons)
- Generació de cartrons per codi únic (PRNG determinista mulberry32 + hash FNV-1a)
- Suport per a múltiples codis en una mateixa partida
- Escàner QR via BarcodeDetector API nativa del navegador
- Cartrons seguint les regles oficials: 3 files × 9 columnes, 5 números per fila, màx 2 per columna, ordenats de menor a major
- Caselles buides amb trama decorativa (com els cartrons físics)
- Detecció automàtica de Línia i Quina amb alerta i confeti
- Modal de Nova Partida: mateixos cartrons o cartrons nous

**General**
- Disseny responsive adaptat a mòbil, tauleta i escriptori
- Tema nadalenc amb animacions (estrelles, flocs de neu)
- Modal de confirmació propi (substitueix `confirm()` natiu, bloquejat en mòbils)
- Footer LiTools

### 🔧 Corregit
- `frases.js` carregat al `<head>` per evitar errors de race condition
- Generació de cartrons: garantia estricta de 5 números per fila
- Números de cada columna ordenats de menor a major (com els cartrons físics)
- Gestió segura del confeti (evita errors si l'element ja no existeix al DOM)
- Reset correcte de l'estat visual en tornar al setup de participants
- Historial del presentador s'actualitza també en desmarcaments manuals
- Les cel·les queden bloquejades correctament després d'aconseguir Quina
- El joc continua sense frases si `frases.js` no es pot carregar

---

## [Pròximes versions]

### [1.1.0] - Planificada
- PWA instal·lable (manifest + service worker)
- Mode offline complet

### [2.0.0] - Planificada
- Sincronització en temps real entre presentador i participants
- Sala de joc compartida per URL
