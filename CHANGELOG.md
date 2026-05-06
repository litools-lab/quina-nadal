# Changelog

Tots els canvis notables d'aquest projecte es documenten en aquest fitxer.

El format segueix [Keep a Changelog](https://keepachangelog.com/ca/1.0.0/),
i el projecte segueix [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0-beta] - 2024-12-XX

### ✨ Afegit
- Mode Presentador amb bombo virtual (números 1–90)
- 90 frases típiques catalanes per a cada número
- Graella visual dels 90 números amb marcatge dels sortits
- Historial dels últims 6 números extrets
- Mode Participant amb generació de cartrons aleatoris
- Suport per a 1–4 cartrons per jugador
- Detecció automàtica de Línia i Quina
- Modal de Nova Partida: opció de reutilitzar cartrons o generar-ne de nous
- Confeti en aconseguir Quina i en acabar el bombo
- Disseny responsive adaptat a mòbil, tauleta i escriptori
- Tema nadalenc amb animacions (estrelles, flocs de neu)

### 🔧 Corregit
- Substitució de `confirm()` natiu (bloquejat en mòbils) per modal propi
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
