# Guia de contribució

Gràcies per voler contribuir a **La Quina de Nadal**! 🎄

Totes les contribucions són benvingudes: correccions d'errors, noves funcionalitats, millores de disseny, traduccions o simplement reportar bugs.

---

## 📋 Taula de continguts

- [Codi de conducta](#codi-de-conducta)
- [Com reportar un error](#com-reportar-un-error)
- [Com suggerir una millora](#com-suggerir-una-millora)
- [Com contribuir codi](#com-contribuir-codi)
- [Estil de codi](#estil-de-codi)
- [Missatges de commit](#missatges-de-commit)

---

## Codi de conducta

Aquest projecte adopta un entorn respectuós i inclusiu. Sigues amable, constructiu i obert a altres opinions.

---

## Com proposar frases noves

Contribuir frases és la manera més senzilla de participar al projecte, **sense necessitat de saber programar**.

### Opció A — Via Issue (recomanada per a no programadors)

1. Ves a Issues → New issue → **"Proposta de frases"**
2. Omple la plantilla amb el número i les frases que proposes, seguint el format indicat
3. Un mantenidor les revisarà i les incorporarà al fitxer `frases.js`

### Opció B — Via Pull Request (per a qui sap usar Git)

1. Edita directament el fitxer [`frases.js`](frases.js)
2. Localitza el número que vols modificar (estan ordenats de l'1 al 90)
3. Afegeix les teves frases a l'array corresponent:
   ```js
   // Exemple: afegir una frase nova al número 42
   // ABANS:
   42: ["Quaranta-dos, la resposta a tot!", "El quaranta-dos!", "Quaranta-dos!"],
   // DESPRÉS:
   42: ["Quaranta-dos, la resposta a tot!", "El quaranta-dos!", "Quaranta-dos!", "Quaranta-dos, el gran número!"],
   ```
4. Obre un Pull Request amb el títol: `frases: número XX — afegir N frases`

### Criteris per acceptar frases

- ✅ En català, to festiu i familiar
- ✅ Fan referència a una tradició, dita popular, data o característica del número
- ✅ Acaben amb `!`
- ✅ Adequades per a totes les edats
- ❌ No s'accepten frases ofensives, polítiques o que facin referència a marques comercials

---

## Com reportar un error

1. Comprova que l'error no ha estat ja reportat a [Issues](../../issues)
2. Obre un nou issue amb la plantilla **Bug report**
3. Inclou:
   - Descripció clara del problema
   - Passos per reproduir-lo
   - Comportament esperat vs. comportament actual
   - Navegador i dispositiu (ex: Chrome 120 / iPhone 14)
   - Captures de pantalla si és possible

---

## Com suggerir una millora

1. Obre un issue amb la plantilla **Feature request**
2. Descriu la funcionalitat que et agradaria veure
3. Explica per què seria útil per als usuaris

---

## Com contribuir codi

### Configuració de l'entorn

El projecte no té cap dependència. Necessites:
- Un navegador modern
- Un editor de text (VS Code recomanat)
- Git

```bash
# 1. Fes fork del repositori a GitHub

# 2. Clona el teu fork
git clone https://github.com/EL-TEU-USUARI/quina-nadal.git
cd quina-nadal

# 3. Obre al navegador
open index.html
```

### Flux de treball

```bash
# Crea una branca descriptiva
git checkout -b fix/cartro-generacio-files
# o
git checkout -b feat/mode-offline

# Fes els teus canvis
# ...

# Commiteja seguint la convenció (vegeu més avall)
git commit -m "fix: garantir exactament 5 números per fila al cartró"

# Puja la branca
git push origin fix/cartro-generacio-files

# Obre un Pull Request a GitHub
```

### Abans d'obrir un Pull Request

- [ ] El codi funciona als navegadors principals (Chrome, Firefox, Safari)
- [ ] Has provat en mòbil (o simulador)
- [ ] No has afegit dependències externes
- [ ] Has actualitzat `CHANGELOG.md` si escau

---

## Estil de codi

- **JavaScript**: ES6+, sense llibreries externes
- **CSS**: variables CSS per a colors reutilitzables, BEM lleugera per a classes
- **HTML**: semàntic, accessible (atributs `aria` on calgui)
- Indentació: **2 espais**
- Cometes: **simples** en JS, **dobles** en HTML
- Funcions: camelCase en català quan sigui possible (ex: `generarCarton`, `treurNum`)

---

## Missatges de commit

Seguim [Conventional Commits](https://www.conventionalcommits.org/):

| Prefix | Quan usar-lo |
|--------|-------------|
| `feat:` | Nova funcionalitat |
| `fix:` | Correcció d'error |
| `style:` | Canvis de CSS/disseny sense afectar lògica |
| `refactor:` | Refactorització de codi |
| `docs:` | Canvis en documentació |
| `chore:` | Tasques de manteniment (CI, dependències...) |

**Exemples:**
```
feat: afegir mode offline amb service worker
fix: corregir detecció de línia quan es desmarca un número
style: millorar contrast dels badges en cartrons guanyadors
docs: actualitzar README amb URL de GitHub Pages
```

---

Gràcies de nou per la teva contribució! 🎉
