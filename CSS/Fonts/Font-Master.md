<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:B5432A,100:F6F1E7&height=180&section=header&text=Typographie%20CSS%20%E2%9C%92%EF%B8%8F&fontSize=40&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=L'atelier%20interactif%20de%20la%20fonderie&descAlignY=55&descSize=16"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=B5432A&center=true&vCenter=true&width=650&lines=font-family+%E2%80%A2+font-size+%E2%80%A2+line-height;letter-spacing+%E2%80%A2+font-weight+%E2%80%A2+clamp()" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-Interm%C3%A9diaire-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Fichier-fonts.css-blue?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif de la fiche

> Ce fichier n'est pas une simple feuille de style : c'est un **atelier de spécimen typographique**, inspiré des vieux catalogues de fonderie (papier crème, encre noire, un seul accent rouge "tampon"). On va comprendre comment les **variables CSS**, les **polices**, et les **contrôles interactifs** travaillent ensemble.

<br/>

## 🎨 1. Les variables CSS (`:root`) — la palette centrale

```css
:root {
  --paper:      #F6F1E7;
  --paper-alt:  #EFE8D8;
  --ink:        #201D1A;
  --ink-soft:   #6B6459;
  --stamp:      #B5432A;
  --stamp-soft: #B5432A22;
  --rule:       #201D1A22;

  --font-display: 'Fraunces', serif;
  --font-body:    'Space Grotesk', sans-serif;
  --font-mono:    'JetBrains Mono', monospace;
}
```

<div align="center">
<svg width="500" height="90" viewBox="0 0 500 90" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="20" width="60" height="50" fill="#F6F1E7" stroke="#ccc"/>
  <rect x="80" y="20" width="60" height="50" fill="#EFE8D8" stroke="#ccc"/>
  <rect x="150" y="20" width="60" height="50" fill="#201D1A"/>
  <rect x="220" y="20" width="60" height="50" fill="#6B6459"/>
  <rect x="290" y="20" width="60" height="50" fill="#B5432A">
    <animate attributeName="opacity" values="1;0.5;1" dur="2s" repeatCount="indefinite"/>
  </rect>
  <text x="250" y="15" font-family="monospace" font-size="11" fill="#555" text-anchor="middle">une seule couleur d'accent (--stamp) qui "respire"</text>
</svg>
</div>

> 💡 **Pourquoi des variables ?** Si demain on veut changer la couleur d'accent de tout le site, on modifie **une seule ligne** (`--stamp`) au lieu de chercher `#B5432A` dans tout le fichier.

| Variable | Usage typique |
|---|---|
| `--font-display` | Grands titres (`h1`), police élégante avec empattements |
| `--font-body` | Texte courant, lisible |
| `--font-mono` | Code, étiquettes techniques (`.prop`, `output`) |
| `--stamp-soft` | Le `22` à la fin du code couleur = opacité ~13%, pour un fond léger sans calculer une nouvelle couleur |

<br/>

## ♿ 2. Respect de l'accessibilité — `prefers-reduced-motion`

```css
@media (prefers-reduced-motion: reduce) {
  * { transition: none !important; animation: none !important; }
}
```

> 🧠 Certaines personnes activent un réglage système "réduire les animations" (vertiges, troubles de l'attention...). Cette règle **coupe toutes les animations** du site pour elles, automatiquement. Un réflexe pro à prendre tôt.

<br/>

## 🅰️ 3. Le titre principal — `font-display` fluide avec `clamp()`

```css
.site-header h1 {
  font-family: var(--font-display);
  font-weight: 600;
  font-size: clamp(2.6rem, 6vw, 5rem);
  line-height: 0.95;
  margin: 0 0 12px;
  letter-spacing: -0.01em;
}
```

<div align="center">
<svg width="480" height="130" viewBox="0 0 480 130" xmlns="http://www.w3.org/2000/svg">
  <text x="240" y="60" font-family="Georgia, serif" font-size="30" font-weight="600" fill="#201D1A" text-anchor="middle">
    <animate attributeName="font-size" values="20;46;20" dur="4s" repeatCount="indefinite"/>
    Aa Titre
  </text>
  <text x="240" y="100" font-family="monospace" font-size="11" fill="#555" text-anchor="middle">clamp(min, préféré, max) → la taille suit la largeur d'écran, entre 2 bornes</text>
</svg>
</div>

`clamp(2.6rem, 6vw, 5rem)` se lit ainsi :
- **jamais en dessous de** `2.6rem` (même sur très petit écran)
- **idéalement** `6vw` (6% de la largeur de la fenêtre → responsive automatique)
- **jamais au-dessus de** `5rem` (même sur très grand écran)

> ✨ C'est **une seule ligne qui remplace plusieurs `@media` queries** pour la taille de police responsive.

<br/>

## 🏷️ 4. L'étiquette "eyebrow" — micro-détail de design

```css
.eyebrow {
  display: inline-block;
  font-family: var(--font-mono);
  font-size: 12px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: var(--stamp);
  border: 1px solid var(--stamp);
  padding: 4px 10px;
  border-radius: 100px;
  margin-bottom: 18px;
}
```

| Propriété | Effet visuel |
|---|---|
| `text-transform: uppercase` | Force les MAJUSCULES, peu importe comment le texte est écrit en HTML |
| `letter-spacing: 1.5px` | Espace les lettres — donne un effet "étiquette officielle" |
| `border-radius: 100px` | Une valeur énorme sur une petite boîte = coins totalement arrondis (pilule) |

<br/>

## 🔴 5. Le curseur d'édition en direct (`#preview-text`)

```css
#preview-text {
  margin: 0;
  width: 100%;
  outline: none;
  transition: font-size 0.15s ease, letter-spacing 0.15s ease, line-height 0.15s ease;
}

#preview-text:focus {
  outline: 2px dashed var(--stamp);
  outline-offset: 8px;
}
```

<div align="center">
<svg width="400" height="120" viewBox="0 0 400 120" xmlns="http://www.w3.org/2000/svg">
  <rect x="60" y="30" width="280" height="60" fill="none" stroke="#B5432A" stroke-width="2" stroke-dasharray="6,4" rx="4">
    <animate attributeName="stroke-dashoffset" values="0;20" dur="1s" repeatCount="indefinite"/>
  </rect>
  <text x="200" y="65" font-family="Georgia" font-size="16" fill="#201D1A" text-anchor="middle">Texte modifiable</text>
</svg>
</div>

C'est ce pointillé rouge en pointillés qui apparaît **uniquement quand l'élément est sélectionné/focus** (`:focus`), avec `outline-offset` qui décale le trait vers l'extérieur pour ne pas coller au texte. La `transition` rend fluide tout changement de taille/espacement pendant qu'on tape.

<br/>

## 🎛️ 6. Les contrôles personnalisés (select, range, boutons segmentés)

```css
input[type="range"] {
  -webkit-appearance: none;
  height: 4px;
  background: var(--ink);
  border-radius: 2px;
}
input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
  width: 16px;
  height: 16px;
  border-radius: 50%;
  background: var(--stamp);
  border: 2px solid var(--paper);
  cursor: pointer;
  margin-top: -6px;
}
```

> 🧠 **Point technique important** : `-webkit-appearance: none` supprime le style natif moche du navigateur pour un `<input type="range">`. Ensuite, `::-webkit-slider-thumb` est un **pseudo-élément spécial** qui cible uniquement le petit rond (le "thumb") qu'on fait glisser — on doit le redessiner à la main, pixel par pixel.

Les boutons segmentés utilisent le même principe de "reconstruction" :

```css
.segmented {
  display: flex;
  border: 1.5px solid var(--ink);
  border-radius: 3px;
  overflow: hidden;
}

.seg-btn.active {
  background: var(--stamp);
  color: var(--paper);
}
```

`overflow: hidden` + `border-radius` sur le parent = les coins arrondis "coupent" proprement les boutons enfants, même si eux n'ont pas de `border-radius`.

<br/>

## 📱 7. Responsive — la fiche s'adapte au mobile

```css
@media (max-width: 760px) {
  .layout { grid-template-columns: 1fr; }
  .preview-box { padding: 36px 24px; }
  .site-header h1 { font-size: 12vw; }
}
```

En dessous de 760px de large (tablette/mobile), la grille à 2 colonnes devient 1 seule colonne, et le titre passe à une taille basée uniquement sur la largeur de l'écran (`vw`).

<br/>

## 🧪 Exercice pour les étudiants

1. Change `--stamp` en une autre couleur (ex: `#2563EB`) → observe combien d'éléments changent automatiquement.
2. Modifie le `clamp()` du `h1` pour tester des bornes plus extrêmes (`clamp(1rem, 10vw, 8rem)`).
3. Retire `-webkit-appearance: none` du slider → compare le rendu avant/après.
4. Réduis la fenêtre sous 760px → vérifie que la mise en page passe bien en 1 colonne.

<br/>

## 📌 Résumé express

| Je veux... | Propriété / technique |
|---|---|
| Centraliser mes couleurs/polices | Variables CSS dans `:root` |
| Une taille de texte responsive sans `@media` | `clamp(min, préféré, max)` |
| Respecter les utilisateurs sensibles au mouvement | `@media (prefers-reduced-motion: reduce)` |
| Styliser un `<input type="range">` | `-webkit-appearance: none` + `::-webkit-slider-thumb` |
| Adapter la mise en page au mobile | `@media (max-width: ...)` |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>