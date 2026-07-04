<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:ff4757,100:6366f1&height=180&section=header&text=CSS%20Position%20%F0%9F%93%8D&fontSize=45&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=static%20%E2%80%A2%20relative%20%E2%80%A2%20absolute%20%E2%80%A2%20fixed%20%E2%80%A2%20sticky&descAlignY=55&descSize=16"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=FF4757&center=true&vCenter=true&width=650&lines=position%3A+static%3B;position%3A+relative%3B;position%3A+absolute%3B;position%3A+fixed%3B;position%3A+sticky%3B" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-D%C3%A9butant%20%E2%86%92%20Interm%C3%A9diaire-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Fichier-position.css-blue?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif de la fiche

> La propriété `position` a **5 valeurs possibles**, et 90% des confusions des étudiants viennent du fait qu'on ne les compare jamais côte à côte. Cette fiche fait le tour complet : `static`, `relative`, `absolute`, `fixed`, `sticky` — avec pour chacune un schéma animé, un exemple, et le piège classique à éviter. On termine par le cas concret du fichier `position.css` du dépôt (le badge centré).

<br/>

## 🗺️ Vue d'ensemble — le tableau de référence

| Valeur | Reste dans le flux normal ? | Référentiel pour `top/left/right/bottom` | Bouge au scroll ? |
|---|---|---|---|
| `static` (défaut) | ✅ Oui | Aucun — `top/left` sont ignorés | Oui, comme tout le reste |
| `relative` | ✅ Oui (sa place d'origine reste réservée) | Lui-même (sa propre position d'origine) | Oui |
| `absolute` | ❌ Non — sorti du flux | Le plus proche ancêtre `relative`/`absolute`/`fixed`/`sticky` (sinon la page) | Oui, avec le contenu autour |
| `fixed` | ❌ Non — sorti du flux | La fenêtre du navigateur (`viewport`) | ❌ Non, reste figé à l'écran |
| `sticky` | ✅ Oui, jusqu'à un seuil | La fenêtre, **une fois le seuil de scroll atteint** | Hybride : suit, puis se fige |

<br/>

## 1️⃣ `position: static` — le comportement par défaut

```css
.box {
  position: static; /* valeur par défaut, rarement écrite explicitement */
}
```

<div align="center">
<svg width="460" height="160" viewBox="0 0 460 160" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="120" height="50" fill="#38bdf8" rx="6"/>
  <rect x="150" y="20" width="120" height="50" fill="#0F6E56" rx="6"/>
  <rect x="280" y="20" width="120" height="50" fill="#993556" rx="6"/>
  <text x="230" y="100" font-family="monospace" font-size="12" fill="#555" text-anchor="middle">Chaque boîte prend sa place normale, l'une après l'autre</text>
  <text x="230" y="120" font-family="monospace" font-size="12" fill="#555" text-anchor="middle">top / left / right / bottom → totalement ignorés</text>
</svg>
</div>

> 🧠 **À retenir** : `static`, c'est "je suis un élément HTML normal, je ne bouge pas par rapport à `top`/`left`". Si un étudiant écrit `top: 50px` sur un élément `static` et que rien ne se passe, c'est **normal** — ce n'est pas un bug.

<br/>

## 2️⃣ `position: relative` — se décaler par rapport à soi-même

```css
.badge {
  position: relative;
  top: 10px;
  left: 20px;
}
```

<div align="center">
<svg width="460" height="180" viewBox="0 0 460 180" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="120" height="50" fill="#ccc" rx="6" opacity="0.5"/>
  <text x="80" y="45" font-family="monospace" font-size="10" text-anchor="middle" fill="#666">place réservée</text>
  <rect x="40" y="30" width="120" height="50" fill="#38bdf8" rx="6">
    <animate attributeName="x" values="20;40;20" dur="2.5s" repeatCount="indefinite"/>
    <animate attributeName="y" values="20;30;20" dur="2.5s" repeatCount="indefinite"/>
  </rect>
  <rect x="150" y="20" width="120" height="50" fill="#0F6E56" rx="6"/>
  <text x="230" y="130" font-family="monospace" font-size="12" fill="#555" text-anchor="middle">La boîte se déplace visuellement...</text>
  <text x="230" y="150" font-family="monospace" font-size="12" fill="#555" text-anchor="middle">...mais son emplacement d'origine reste "réservé" (trou visible)</text>
</svg>
</div>

> ⚠️ **Le piège classique** : `top: 10px; left: 20px;` sur un élément `relative` le déplace **par rapport à l'endroit où il aurait été normalement**, pas par rapport au parent. Et surtout : **l'espace d'origine reste vide**, ce qui peut créer un trou ou un chevauchement avec les voisins.

> 💡 **Le vrai rôle de `relative` en pratique** : on l'utilise très rarement pour déplacer un élément. Son usage n°1 (et celui du fichier `position.css`) est de **servir de référentiel** pour un enfant en `absolute` — voir section 5.

<br/>

## 3️⃣ `position: absolute` — sortir du flux et se placer précisément

```css
.tooltip {
  position: absolute;
  top: 0;
  right: 0;
}
```

<div align="center">
<svg width="460" height="200" viewBox="0 0 460 200" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="420" height="130" fill="#f0f0f0" stroke="#333" stroke-width="2" stroke-dasharray="6,4"/>
  <text x="35" y="15" font-family="monospace" font-size="11" fill="#666">ancêtre position: relative</text>

  <rect x="40" y="40" width="100" height="40" fill="#38bdf8" rx="6"/>
  <rect x="150" y="40" width="100" height="40" fill="#0F6E56" rx="6"/>

  <rect x="370" y="30" width="60" height="30" fill="#993556" rx="4">
    <animate attributeName="opacity" values="1;0.5;1" dur="2s" repeatCount="indefinite"/>
  </rect>
  <text x="400" y="50" font-family="Arial" font-size="9" fill="white" text-anchor="middle">badge</text>

  <text x="230" y="175" font-family="monospace" font-size="12" fill="#555" text-anchor="middle">Le badge est "sorti" du flux : les 2 autres boîtes ne savent même pas qu'il existe</text>
</svg>
</div>

> 🧠 **À retenir** : un élément `absolute` est **totalement retiré du flux normal**. Les autres éléments se comportent comme s'il n'existait pas — ils peuvent même passer "en-dessous" ou "derrière" lui. C'est pour ça qu'on l'utilise pour des badges, pastilles de notification, menus déroulants, tooltips.

> ⚠️ **Le piège n°1** : sans ancêtre `position: relative` (ou `absolute`/`fixed`/`sticky`) quelque part au-dessus, l'élément `absolute` se positionne par rapport à **toute la page HTML**, pas par rapport au parent visuel le plus proche. Toujours vérifier la chaîne de parents !

<br/>

## 4️⃣ `position: fixed` — figé à l'écran, ignore le scroll

```css
.back-to-top {
  position: fixed;
  bottom: 20px;
  right: 20px;
}
```

<div align="center">
<svg width="460" height="220" viewBox="0 0 460 220" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="10" width="420" height="200" fill="#fafafa" stroke="#333" stroke-width="2"/>
  <text x="230" y="30" font-family="monospace" font-size="11" fill="#999" text-anchor="middle">contenu de la page (défile)</text>
  <rect x="60" y="45" width="340" height="18" fill="#e0e0e0">
    <animate attributeName="y" values="45;-40;45" dur="4s" repeatCount="indefinite"/>
  </rect>
  <rect x="60" y="70" width="340" height="18" fill="#e0e0e0">
    <animate attributeName="y" values="70;-15;70" dur="4s" repeatCount="indefinite"/>
  </rect>
  <rect x="60" y="95" width="340" height="18" fill="#e0e0e0">
    <animate attributeName="y" values="95;10;95" dur="4s" repeatCount="indefinite"/>
  </rect>

  <circle cx="400" cy="180" r="22" fill="#6366f1"/>
  <text x="400" y="185" font-family="Arial" font-size="18" fill="white" text-anchor="middle">↑</text>
  <text x="230" y="205" font-family="monospace" font-size="11" fill="#6366f1" text-anchor="middle">le bouton "fixed" reste immobile pendant que tout défile</text>
</svg>
</div>

> 🧠 **À retenir** : `fixed` se comporte comme `absolute`, mais son référentiel est **toujours la fenêtre du navigateur** (`viewport`), jamais un parent. C'est pour ça qu'un header fixe, un bouton "retour en haut", ou un chat flottant restent visibles même en scrollant tout en bas de la page.

> ⚠️ **Piège avancé** : si un ancêtre a une propriété `transform`, `filter` ou `will-change` définie, il devient (par une règle spéciale du CSS) le nouveau référentiel du `fixed`, qui perd alors son comportement "toujours par rapport à l'écran". Bug fréquent et difficile à diagnostiquer chez les développeurs confirmés eux-mêmes.

<br/>

## 5️⃣ `position: sticky` — l'hybride relative → fixed

```css
.section-title {
  position: sticky;
  top: 0;
}
```

<div align="center">
<svg width="460" height="240" viewBox="0 0 460 240" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="10" width="420" height="220" fill="#fafafa" stroke="#333" stroke-width="2"/>

  <rect x="40" y="30" width="380" height="30" fill="#6366f1" rx="4">
    <animate attributeName="y" values="30;30;10;10;30" dur="5s" repeatCount="indefinite"/>
  </rect>
  <text x="230" y="50" font-family="Arial" font-size="12" fill="white" text-anchor="middle">
    <animate attributeName="y" values="50;50;30;30;50" dur="5s" repeatCount="indefinite"/>
    Titre de section (sticky, top: 0)
  </text>

  <rect x="60" y="80" width="340" height="16" fill="#e0e0e0">
    <animate attributeName="y" values="80;40;-30;-30;80" dur="5s" repeatCount="indefinite"/>
  </rect>
  <rect x="60" y="105" width="340" height="16" fill="#e0e0e0">
    <animate attributeName="y" values="105;65;-5;-5;105" dur="5s" repeatCount="indefinite"/>
  </rect>
  <rect x="60" y="130" width="340" height="16" fill="#e0e0e0">
    <animate attributeName="y" values="130;90;20;20;130" dur="5s" repeatCount="indefinite"/>
  </rect>

  <text x="230" y="220" font-family="monospace" font-size="11" fill="#6366f1" text-anchor="middle">défile normalement, puis se colle en haut, puis repart avec sa section</text>
</svg>
</div>

> 🧠 **À retenir** : `sticky` commence par se comporter comme `relative` (dans le flux normal), **jusqu'à ce que le scroll atteigne le seuil défini** (`top: 0` = "colle-toi quand tu touches le haut de l'écran"). À partir de là, il se comporte comme `fixed`... mais **seulement tant qu'on reste à l'intérieur de son élément parent**. Dès que le parent sort de l'écran, le `sticky` repart avec lui.

| Condition requise | Pourquoi |
|---|---|
| Une valeur de seuil obligatoire (`top`, `bottom`...) | Sans `top: 0` (ou une autre valeur), `sticky` se comporte comme `static` — ne rien oublier |
| Le parent doit avoir une hauteur suffisante | Si le parent fait exactement la même hauteur que l'élément sticky, il n'y a pas de place pour "coller" — aucun effet visible |
| Pas de `overflow: hidden`/`scroll` sur un ancêtre | Un ancêtre avec `overflow` caché peut casser le comportement sticky de manière très frustrante à déboguer |

> 💡 **Cas d'usage typiques** : titres de section dans une longue page, en-têtes de colonnes dans un tableau qui scrolle, barre de filtres qui reste visible pendant qu'on parcourt une liste de résultats.

<br/>

## 🧩 Les 5 valeurs, côte à côte

<div align="center">
<svg width="500" height="130" viewBox="0 0 500 130" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="20" width="90" height="70" fill="#ccc" rx="6"/>
  <text x="55" y="105" font-family="monospace" font-size="11" text-anchor="middle">static</text>

  <rect x="110" y="20" width="90" height="70" fill="#38bdf8" rx="6"/>
  <text x="155" y="105" font-family="monospace" font-size="11" text-anchor="middle">relative</text>

  <rect x="210" y="20" width="90" height="70" fill="#993556" rx="6">
    <animate attributeName="opacity" values="1;0.6;1" dur="2s" repeatCount="indefinite"/>
  </rect>
  <text x="255" y="105" font-family="monospace" font-size="11" text-anchor="middle">absolute</text>

  <rect x="310" y="20" width="90" height="70" fill="#6366f1" rx="6"/>
  <text x="355" y="105" font-family="monospace" font-size="11" text-anchor="middle">fixed</text>

  <rect x="410" y="20" width="90" height="70" fill="#0F6E56" rx="6">
    <animate attributeName="y" values="20;10;20" dur="2s" repeatCount="indefinite"/>
  </rect>
  <text x="455" y="105" font-family="monospace" font-size="11" text-anchor="middle">sticky</text>
</svg>
</div>

<br/>

## 🎴 Le cas concret du dépôt — `position.css` (badge centré)

Dans le fichier du dépôt, on combine **`relative` + `absolute`** : c'est le duo n°1 du positionnement CSS, utilisé pour ancrer un badge/pastille précisément à l'intérieur d'un conteneur.

### Le parent — créer le point de repère

```css
.parent {
  width: 300px;
  height: 300px;
  background-color: #f0f0f0;
  border: 4px dashed #333;
  position: relative;
}
```

> 🧠 `position: relative` sur `.parent`, **sans aucun décalage** (`top`/`left` non utilisés ici), ne bouge visuellement rien. Son seul rôle est de devenir **le référentiel de positionnement** pour l'enfant `.child` en `absolute`.

Si on oublie `position: relative` sur `.parent`, l'enfant `.child` en `absolute` ira se positionner par rapport à **toute la page**, pas par rapport à la boîte grise. C'est l'erreur n°1 des débutants — directement liée au piège de la section 3.

<div align="center">
<svg width="500" height="180" viewBox="0 0 500 180" xmlns="http://www.w3.org/2000/svg">
  <text x="130" y="20" font-family="monospace" font-size="12" fill="#0F6E56" text-anchor="middle">✅ avec position: relative</text>
  <rect x="30" y="30" width="200" height="140" fill="#f0f0f0" stroke="#333" stroke-width="3" stroke-dasharray="6,4"/>
  <rect x="105" y="80" width="50" height="50" fill="#ff4757" rx="4"/>

  <text x="380" y="20" font-family="monospace" font-size="12" fill="#993556" text-anchor="middle">❌ sans position: relative</text>
  <rect x="280" y="30" width="200" height="140" fill="#f0f0f0" stroke="#333" stroke-width="3" stroke-dasharray="6,4"/>
  <rect x="465" y="5" width="50" height="50" fill="#993556" rx="4" opacity="0.7"/>
</svg>
</div>

### L'enfant — se positionner précisément

```css
.child {
  width: 100px;
  height: 100px;
  background-color: #ff4757;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
```

### La technique du "centrage parfait" — décortiquée en 2 étapes

<div align="center">
<svg width="500" height="200" viewBox="0 0 500 200" xmlns="http://www.w3.org/2000/svg">
  <text x="130" y="20" font-family="monospace" font-size="12" fill="#555" text-anchor="middle">Étape 1 : left/top: 50%</text>
  <rect x="30" y="30" width="200" height="150" fill="#f0f0f0" stroke="#333" stroke-dasharray="5,3"/>
  <rect x="130" y="105" width="60" height="60" fill="#ff4757" rx="4" opacity="0.85"/>
  <circle cx="130" cy="105" r="3" fill="#201D1A"/>
  <text x="140" y="100" font-family="monospace" font-size="10" fill="#201D1A">coin</text>

  <text x="380" y="20" font-family="monospace" font-size="12" fill="#0F6E56" text-anchor="middle">Étape 2 : translate(-50%, -50%)</text>
  <rect x="280" y="30" width="200" height="150" fill="#f0f0f0" stroke="#333" stroke-dasharray="5,3"/>
  <rect x="350" y="75" width="60" height="60" fill="#ff4757" rx="4">
    <animate attributeName="x" values="380;350;380" dur="2.5s" repeatCount="indefinite"/>
    <animate attributeName="y" values="105;75;105" dur="2.5s" repeatCount="indefinite"/>
  </rect>
  <circle cx="380" cy="105" r="3" fill="#201D1A"/>
</svg>
</div>

| Étape | Propriété | Ce qu'elle fait | Le piège si on l'oublie |
|---|---|---|---|
| 1 | `left: 50%; top: 50%;` | Place le **coin supérieur gauche** de `.child` au centre exact du parent | Le carré paraît décalé vers le bas-droite (car c'est son coin, pas son centre, qui est au milieu) |
| 2 | `transform: translate(-50%, -50%)` | Recule la boîte de **50% de sa propre largeur/hauteur** pour que ce soit son **centre** qui tombe pile au milieu | Sans ça, le centrage n'est jamais parfait — c'est l'étape que les débutants oublient |

> 💡 **Pourquoi pas `margin-left: -50px`, `margin-top: -50px` à la place ?** Ça marcherait, mais seulement si on connaît la taille exacte de la boîte (`100px`). Avec `translate(-50%, -50%)`, le centrage reste parfait **même si on change la taille de `.child` plus tard**, sans rien recalculer.

### Centrer le contenu à l'intérieur du badge (Flexbox imbriqué)

```css
.child {
  display: flex;
  align-items: center;
  justify-content: center;
}
```

> Une fois le `.child` positionné au centre du parent (avec `position: absolute`), on utilise **Flexbox à l'intérieur** pour centrer le texte à l'intérieur du carré rouge lui-même. Les deux techniques (position + flex) travaillent ensemble, à deux niveaux différents.

<br/>

## 🧪 Exercices pour les étudiants

**Sur `position.css` :**
1. Retire temporairement `position: relative` du `.parent` → observe où part le badge rouge.
2. Change `left: 50%; top: 50%` en `left: 0; top: 0` → à quel endroit se retrouve le coin du badge ?
3. Retire uniquement `transform: translate(-50%, -50%)` → mesure de combien de pixels le centrage est faux.
4. Remplace `position: absolute` par `position: fixed` sur `.child` → scrolle la page et observe la différence.

**Pour comparer les 5 valeurs :**
5. Crée 5 boîtes identiques dans une page longue (avec beaucoup de contenu au-dessus et en dessous), applique une valeur de `position` différente à chacune, et scrolle : note à l'écrit ce que fait chacune.
6. Sur la boîte en `sticky`, supprime la valeur `top` → observe qu'elle redevient identique à `static`.
7. Sur la boîte en `absolute`, retire tout ancêtre `relative` → observe qu'elle se positionne par rapport à toute la page.

<br/>

## 📌 Résumé express

| Je veux... | Valeur de `position` |
|---|---|
| Comportement HTML normal, aucun décalage possible | `static` (par défaut) |
| Décaler légèrement un élément sans casser la mise en page | `relative` + `top`/`left` |
| Créer un référentiel pour un enfant positionné | `relative` sur le parent (sans décalage) |
| Sortir un élément du flux et le placer précisément dans un parent | `absolute` + `top`/`left`/`right`/`bottom` |
| Centrer parfaitement un élément positionné | `left: 50%; top: 50%;` + `transform: translate(-50%, -50%)` |
| Garder un élément visible même en scrollant toute la page | `fixed` |
| Un titre/en-tête qui se colle en haut puis repart avec sa section | `sticky` + `top: 0` |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>