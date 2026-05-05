# 🎄 La Quina de Nadal

Aplicació web per jugar a la Quina de Nadal, desenvolupada amb HTML/CSS/JS pur.

**Conversa original:** https://claude.ai/share/4aafd7e7-4b10-4fa9-8f06-045d9fcfb529

---

## 📱 Funcionalitats (v1.0)

### Menú principal
- Pantalla de benvinguda amb selecció de rol

### Mode Presentador 🎱
- Bombo virtual amb extracció aleatòria del 1 al 90
- Frases típiques catalanes per a cada número (ex: 13 → "El tretze, la mala sort!")
- Graella amb tots els 90 números i marcatge visual dels sortits
- Historial dels últims 6 números
- Marcatge/desmarcatge manual des de la graella
- Confeti quan s'acaba la partida

### Mode Participant 🎴
- Configuració de jugadors amb nom i número de cartrons (1–4 per jugador)
- Cartrons generats aleatòriament seguint les regles de la quina (3 files × 9 columnes, 5 números per fila)
- Marcatge manual fent clic sobre els números (com el joc físic)
- Detecció automàtica de Línia i Quina amb alerta i confeti
- Resum de números marcats

---

## 🚀 Full de ruta

| Fase | Descripció | Estat |
|------|-----------|-------|
| 1 | GitHub Pages (web accessible) | ✅ Llest |
| 2 | PWA instal·lable (manifest + service worker) | 🔜 Pendent |
| 3 | App nativa (Capacitor per iOS/Android, Electron/Tauri per escriptori) | 🔜 Pendent |
| 4 | Monetització (Google AdMob, compres in-app) | 🔜 Pendent |

---

## 🌐 Desplegar a GitHub Pages

1. Crea un repositori nou a GitHub (ex: `quina-nadal`)
2. Puja el fitxer `index.html` a la branca `main`
3. Ves a **Settings → Pages → Source → Deploy from branch → main / root**
4. En uns minuts l'app estarà disponible a: `https://<usuari>.github.io/quina-nadal/`

---

## 🛠️ Tecnologies

- HTML5 / CSS3 / JavaScript vanilla (sense dependències)
- Google Fonts: Playfair Display + Lato
- Compatible amb tots els navegadors moderns, mòbil i escriptori

---

## 📋 Estructura del codi

```
index.html
├── <style>          → Tots els estils (responsive, nadalenc)
├── <div class="app"> → Estructura HTML (4 pantalles)
│   ├── screen-menu          → Menú principal
│   ├── screen-presentador   → Bombo del presentador
│   ├── screen-setup-jugador → Configuració de jugadors
│   └── screen-joc-jugador   → Cartrons de joc
└── <script>         → Lògica del joc
    ├── FRASES{}     → 90 frases típiques catalanes
    ├── Presentador  → initPresentador, treurNum, togglePresManual
    └── Jugadors     → generarCarton, clickCela, comprovarGuanyador
```
