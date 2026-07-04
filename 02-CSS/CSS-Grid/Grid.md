<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:8b5cf6,100:38bdf8&amp;height=180&amp;section=header&amp;text=CSS%20Grid%20%F0%9F%A7%B1&amp;fontSize=45&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=35&amp;desc=La%20mise%20en%20page%20en%20deux%20dimensions&amp;descAlignY=55&amp;descSize=16"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&amp;size=20&amp;pause=1000&amp;color=8B5CF6&amp;center=true&amp;vCenter=true&amp;width=650&amp;lines=display%3A+grid%3B;grid-template-columns+%E2%80%A2+gap+%E2%80%A2+fr;grid-template-areas+%E2%80%A2+minmax()+%E2%80%A2+auto-fit" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&amp;logo=css3&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-Interm%C3%A9diaire-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Cours-CSS%20Grid-8b5cf6?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif du cours

> **CSS Grid** est le seul système de mise en page CSS pensé **dès le départ pour deux dimensions à la fois** — lignes ET colonnes en même temps. Là où Flexbox excelle pour aligner des éléments **sur un seul axe**, Grid excelle pour construire **des mises en page entières** : dashboards, galeries, mise en page de magazine, formulaires complexes.

<br/>

## 📂 Fichiers liés

| Fichier | Lien GitHub |
|---|---|
| 📘 Ce cours (`Grid.md`) | [CSS/Grid/Grid.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/CSS/Grid/Grid.md) |
| 🧪 Exercices | [exercices/Grid-Master/Hint.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/exercices/Grid-Master/Hint.md) |
| 🎴 Mini-projet | [projets/Grid-Dashboard/Consigne.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/projets/Grid-Dashboard/Consigne.md) |

<br/>

## 🆚 Grid vs Flexbox — quand utiliser quoi ?

<div align="center">
<svg width="500" height="150" viewBox="0 0 500 150" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="220" height="110" fill="#38bdf8" rx="8" opacity="0.85"/>
  <text x="130" y="50" font-family="monospace" font-size="14" fill="white" text-anchor="middle">Flexbox</text>
  <text x="130" y="75" font-family="Arial" font-size="11" fill="white" text-anchor="middle">1 dimension</text>
  <text x="130" y="93" font-family="Arial" font-size="11" fill="white" text-anchor="middle">(ligne OU colonne)</text>
  <text x="130" y="115" font-family="Arial" font-size="11" fill="white" text-anchor="middle">→ navbars, cartes, listes</text>

  <rect x="260" y="20" width="220" height="110" fill="#8b5cf6" rx="8" opacity="0.85"/>
  <text x="370" y="50" font-family="monospace" font-size="14" fill="white" text-anchor="middle">Grid</text>
  <text x="370" y="75" font-family="Arial" font-size="11" fill="white" text-anchor="middle">2 dimensions</text>
  <text x="370" y="93" font-family="Arial" font-size="11" fill="white" text-anchor="middle">(lignes ET colonnes)</text>
  <text x="370" y="115" font-family="Arial" font-size="11" fill="white" text-anchor="middle">→ mise en page globale</text>
</svg>
</div>

> 💡 **En pratique, on combine souvent les deux** : Grid pour la structure globale de la page, Flexbox à l'intérieur de chaque case de la grille pour aligner son contenu.

<br/>

## 1️⃣ Activer Grid — `display: grid`

```css
.container {
  display: grid;
  grid-template-columns: 200px 200px 200px;
  gap: 16px;
}
```

<div align="center">
<svg width="480" height="140" viewBox="0 0 480 140" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="130" height="100" fill="#8b5cf6" rx="6">
    <animate attributeName="opacity" values="1;0.5;1" dur="2s" repeatCount="indefinite"/>
  </rect>
  <rect x="175" y="20" width="130" height="100" fill="#7c3aed" rx="6">
    <animate attributeName="opacity" values="1;0.5;1" dur="2s" begin="0.3s" repeatCount="indefinite"/>
  </rect>
  <rect x="330" y="20" width="130" height="100" fill="#6d28d9" rx="6">
    <animate attributeName="opacity" values="1;0.5;1" dur="2s" begin="0.6s" repeatCount="indefinite"/>
  </rect>
  <text x="240" y="135" font-family="monospace" font-size="11" fill="#555" text-anchor="middle">3 colonnes de 200px chacune, séparées de 16px (gap)</text>
</svg>
</div>

| Propriété | Rôle |
|---|---|
| `display: grid` | Transforme le conteneur en grille ; ses enfants directs deviennent des "grid items" |
| `grid-template-columns` | Définit **le nombre et la taille** des colonnes |
| `gap` | Espace entre les cellules (remplace `row-gap` + `column-gap` réunis) |

<br/>

## 2️⃣ L'unité `fr` — la vraie force de Grid

```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  gap: 16px;
}
```

<div align="center">
<svg width="480" height="120" viewBox="0 0 480 120" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="100" height="80" fill="#a78bfa" rx="6"/>
  <text x="70" y="65" font-family="monospace" font-size="12" fill="white" text-anchor="middle">1fr</text>
  <rect x="130" y="20" width="200" height="80" fill="#8b5cf6" rx="6"/>
  <text x="230" y="65" font-family="monospace" font-size="12" fill="white" text-anchor="middle">2fr</text>
  <rect x="340" y="20" width="100" height="80" fill="#a78bfa" rx="6"/>
  <text x="390" y="65" font-family="monospace" font-size="12" fill="white" text-anchor="middle">1fr</text>
</svg>
</div>

> 🧠 **`fr` = "fraction de l'espace disponible"**. `1fr 2fr 1fr` divise l'espace total en 4 parts égales, et donne 1 part / 2 parts / 1 part aux trois colonnes. Contrairement à `%`, `fr` prend en compte automatiquement le `gap` et le padding — pas de calcul manuel à faire.

> 💡 On peut mélanger `fr` avec des valeurs fixes : `grid-template-columns: 250px 1fr;` donne une colonne fixe de 250px (ex : menu latéral) et une colonne qui prend **tout le reste** de l'espace.

<br/>

## 3️⃣ `repeat()` — éviter de répéter le code

```css
/* Ces deux lignes sont strictement équivalentes */
grid-template-columns: 1fr 1fr 1fr 1fr;
grid-template-columns: repeat(4, 1fr);
```

```css
/* Motif répété : 200px puis 1fr, deux fois de suite */
grid-template-columns: repeat(2, 200px 1fr);
/* équivaut à : 200px 1fr 200px 1fr */
```

<br/>

## 4️⃣ `minmax()` et `auto-fit` — la grille responsive automatique

```css
.galerie {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 16px;
}
```

<div align="center">
<svg width="500" height="160" viewBox="0 0 500 160" xmlns="http://www.w3.org/2000/svg">
  <text x="130" y="20" font-family="monospace" font-size="11" fill="#555" text-anchor="middle">Écran large → plus de colonnes</text>
  <rect x="20" y="30" width="105" height="60" fill="#8b5cf6" rx="4"/>
  <rect x="135" y="30" width="105" height="60" fill="#8b5cf6" rx="4"/>
  <rect x="250" y="30" width="105" height="60" fill="#8b5cf6" rx="4"/>
  <rect x="365" y="30" width="105" height="60" fill="#8b5cf6" rx="4"/>

  <text x="130" y="115" font-family="monospace" font-size="11" fill="#555" text-anchor="middle">Écran étroit → moins de colonnes, plus larges</text>
  <rect x="20" y="125" width="220" height="25" fill="#a78bfa" rx="4"/>
  <rect x="250" y="125" width="220" height="25" fill="#a78bfa" rx="4"/>
</svg>
</div>

> 🧠 **Sans écrire une seule `@media` query**, cette ligne dit : "crée autant de colonnes d'au moins 180px que possible (`auto-fit`), et si de la place reste, répartis-la également (`1fr`)". C'est **la technique la plus utilisée** pour les galeries d'images et grilles de cartes responsives en 2026.

| Fonction | Rôle |
|---|---|
| `minmax(180px, 1fr)` | Chaque colonne fait **au minimum** 180px, et **au maximum** sa part équitable de l'espace restant |
| `auto-fit` | Crée **autant de colonnes que la largeur le permet**, et les étire pour combler l'espace vide |
| `auto-fill` | Comme `auto-fit`, mais laisse des colonnes vides invisibles plutôt que d'étirer — utile si on veut garder une taille de carte fixe |

<br/>

## 5️⃣ `grid-template-areas` — nommer sa mise en page

```css
.layout {
  display: grid;
  grid-template-columns: 220px 1fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "sidebar header"
    "sidebar main"
    "sidebar footer";
  gap: 16px;
  min-height: 100vh;
}

.header  { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main    { grid-area: main; }
.footer  { grid-area: footer; }
```

<div align="center">
<svg width="420" height="300" viewBox="0 0 420 300" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="100" height="260" fill="#7c3aed" rx="6"/>
  <text x="70" y="150" font-family="monospace" font-size="12" fill="white" text-anchor="middle" transform="rotate(-90 70 150)">sidebar</text>

  <rect x="135" y="20" width="265" height="50" fill="#8b5cf6" rx="6">
    <animate attributeName="opacity" values="1;0.6;1" dur="2.5s" repeatCount="indefinite"/>
  </rect>
  <text x="267" y="50" font-family="monospace" font-size="12" fill="white" text-anchor="middle">header</text>

  <rect x="135" y="85" width="265" height="145" fill="#a78bfa" rx="6"/>
  <text x="267" y="160" font-family="monospace" font-size="13" fill="white" text-anchor="middle">main</text>

  <rect x="135" y="245" width="265" height="35" fill="#6d28d9" rx="6"/>
  <text x="267" y="267" font-family="monospace" font-size="11" fill="white" text-anchor="middle">footer</text>
</svg>
</div>

> ✨ **C'est la fonctionnalité la plus lisible de tout le CSS moderne** : le schéma `grid-template-areas` dessine littéralement la mise en page avec du texte, dans le CSS lui-même. Un point (`.`) dans le schéma représente une cellule vide.

<br/>

## 6️⃣ `grid-column` / `grid-row` — faire s'étendre un élément

```css
.grille {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: 100px;
  gap: 12px;
}

.grande-carte {
  grid-column: span 2;  /* occupe 2 colonnes */
  grid-row: span 2;     /* occupe 2 lignes */
}
```

<div align="center">
<svg width="400" height="220" viewBox="0 0 400 220" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="170" height="170" fill="#8b5cf6" rx="6">
    <animate attributeName="opacity" values="1;0.6;1" dur="2.5s" repeatCount="indefinite"/>
  </rect>
  <text x="105" y="110" font-family="monospace" font-size="12" fill="white" text-anchor="middle">span 2 / span 2</text>

  <rect x="200" y="20" width="80" height="80" fill="#c4b5fd" rx="4"/>
  <rect x="290" y="20" width="80" height="80" fill="#c4b5fd" rx="4"/>
  <rect x="200" y="110" width="80" height="80" fill="#c4b5fd" rx="4"/>
  <rect x="290" y="110" width="80" height="80" fill="#c4b5fd" rx="4"/>
</svg>
</div>

> 🧠 `grid-column: span 2` dit "cet élément occupe 2 colonnes à partir d'ici", sans avoir à calculer sur quelle colonne exacte il commence. C'est la technique utilisée pour mettre en avant un article, une image, ou une carte "vedette" dans une grille.

<br/>

## 7️⃣ Alignement — `justify-items` / `align-items` / `justify-content` / `align-content`

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 100px);
  justify-content: center; /* centre TOUTE la grille horizontalement */
  align-items: center;     /* centre CHAQUE élément dans sa cellule, verticalement */
}
```

| Propriété | Agit sur | Axe |
|---|---|---|
| `justify-items` | Chaque élément **dans sa cellule** | Horizontal |
| `align-items` | Chaque élément **dans sa cellule** | Vertical |
| `justify-content` | **La grille entière** dans son conteneur | Horizontal |
| `align-content` | **La grille entière** dans son conteneur | Vertical |

> 💡 **Astuce mnémotechnique** : `-items` agit à l'intérieur de chaque case, `-content` agit sur la grille comme un tout — exactement la même logique qu'en Flexbox.

<br/>

## 📄 Exemple complet — dashboard responsive

```html
<div class="layout">
  <header class="header">Header</header>
  <nav class="sidebar">Menu</nav>
  <main class="main">Contenu principal</main>
  <footer class="footer">Footer</footer>
</div>
```

```css
.layout {
  display: grid;
  grid-template-columns: 220px 1fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "sidebar header"
    "sidebar main"
    "sidebar footer";
  min-height: 100vh;
  gap: 12px;
}

.header  { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main    { grid-area: main; }
.footer  { grid-area: footer; }

/* Sur mobile : sidebar au-dessus, une seule colonne */
@media (max-width: 700px) {
  .layout {
    grid-template-columns: 1fr;
    grid-template-areas:
      "header"
      "sidebar"
      "main"
      "footer";
  }
}
```

<br/>

## 📌 Résumé express

| Je veux... | Propriété / fonction |
|---|---|
| Activer une grille | `display: grid` |
| Définir des colonnes proportionnelles | `grid-template-columns: 1fr 2fr ...` |
| Répéter un motif de colonnes | `repeat(n, valeur)` |
| Colonnes responsives sans `@media` | `repeat(auto-fit, minmax(min, 1fr))` |
| Dessiner la mise en page nommée | `grid-template-areas` + `grid-area` |
| Étendre un élément sur plusieurs cellules | `grid-column: span n` / `grid-row: span n` |
| Centrer chaque élément dans sa cellule | `justify-items` / `align-items` |
| Centrer la grille entière | `justify-content` / `align-content` |

<br/>

## ➡️ Et maintenant ?

- 🧪 Passe aux **[exercices guidés](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/exercices/Grid-Master/Hint.md)** pour manipuler chaque propriété.
- 🎴 Termine avec le **[mini-projet dashboard](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/projets/Grid-Dashboard/Consigne.md)** pour tout mettre en pratique.

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>
