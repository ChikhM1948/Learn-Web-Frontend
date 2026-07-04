<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:38bdf8,100:6366f1&height=180&section=header&text=Flexbox%20%F0%9F%A7%A9&fontSize=45&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=La%20mise%20en%20page%20flexible%20en%20CSS&descAlignY=55&descSize=16"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=38BDF8&center=true&vCenter=true&width=650&lines=display%3A+flex%3B;flex-direction+%E2%80%A2+justify-content+%E2%80%A2+align-items;gap+%E2%80%A2+flex-wrap+%E2%80%A2+box-sizing" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Fichier-Flex.css-blue?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif de la fiche

> Le **Flexbox** (`display: flex`) permet d'aligner, d'espacer et de faire réagir des éléments les uns par rapport aux autres, sans calcul de marges manuel. On va décortiquer **le fichier `Flex.css`** du dépôt, propriété par propriété.

<br/>

## 🎬 Le concept en une image (animée)

Le conteneur flex place ses enfants **sur un axe**. On peut le voir comme un train de wagons qui glisse selon la direction choisie :

<div align="center">
<svg width="520" height="140" viewBox="0 0 520 140" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="20" width="500" height="100" rx="12" fill="#f4f4f4" stroke="#bdbdbd" stroke-width="2"/>
  <g>
    <rect x="30" y="45" width="60" height="50" rx="8" fill="#185FA5">
      <animate attributeName="x" values="30;410;30" dur="4s" repeatCount="indefinite"/>
    </rect>
    <rect x="110" y="45" width="60" height="50" rx="8" fill="#0F6E56">
      <animate attributeName="x" values="110;30;110" dur="4s" repeatCount="indefinite"/>
    </rect>
    <rect x="190" y="45" width="60" height="50" rx="8" fill="#993556">
      <animate attributeName="x" values="190;110;190" dur="4s" repeatCount="indefinite"/>
    </rect>
    <rect x="270" y="45" width="60" height="50" rx="8" fill="#B5650B">
      <animate attributeName="x" values="270;190;270" dur="4s" repeatCount="indefinite"/>
    </rect>
  </g>
  <text x="260" y="15" font-family="monospace" font-size="12" fill="#555" text-anchor="middle">flex-direction: row  →  les boîtes glissent sur l'axe horizontal</text>
</svg>
</div>

<br/>

## 📦 1. Le Reset — pourquoi commencer par ça ?

```css
/* ── Reset ── */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

| Propriété | Rôle |
|---|---|
| `margin: 0; padding: 0;` | Supprime les espacements par défaut imposés par le navigateur (chaque navigateur a les siens, d'où les bugs "ça ne s'aligne pas pareil partout") |
| `box-sizing: border-box` | La largeur/hauteur déclarée inclut désormais le `padding` et la `border`. Sans ça, une boîte de `160px` devient plus large dès qu'on ajoute un `padding`. |

> 💡 **Règle d'or** : presque tous les projets CSS sérieux commencent par ce reset.

<br/>

## 🧱 2. Centrer toute la page avec Flexbox

```css
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

<div align="center">
<svg width="420" height="180" viewBox="0 0 420 180" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="10" width="400" height="160" fill="none" stroke="#333" stroke-width="2" stroke-dasharray="6,4"/>
  <rect x="160" y="65" width="100" height="50" rx="8" fill="#38bdf8">
    <animate attributeName="opacity" values="0.4;1;0.4" dur="2.5s" repeatCount="indefinite"/>
  </rect>
  <text x="210" y="95" font-family="monospace" font-size="11" fill="#fff" text-anchor="middle" dominant-baseline="middle">centré ✨</text>
  <line x1="10" y1="90" x2="410" y2="90" stroke="#999" stroke-dasharray="2,3"/>
  <line x1="210" y1="10" x2="210" y2="170" stroke="#999" stroke-dasharray="2,3"/>
</svg>
</div>

C'est le combo le plus utilisé du CSS moderne : trois lignes remplacent des dizaines de lignes de positionnement manuel.

| Propriété | Axe concerné | Effet |
|---|---|---|
| `display: flex` | — | Active Flexbox sur `body`, ses enfants directs deviennent des "flex items" |
| `justify-content: center` | Axe **principal** (horizontal par défaut) | Centre les enfants horizontalement |
| `align-items: center` | Axe **secondaire** (vertical par défaut) | Centre les enfants verticalement |
| `min-height: 100vh` | — | Le conteneur prend toute la hauteur de l'écran, sinon "centrer verticalement" n'a pas de sens |

<br/>

## 🗂️ 3. Le conteneur flex principal (`.flex-container`)

```css
.flex-container {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  justify-content: center;
  padding: 32px;
  max-width: 600px;
}
```

<div align="center">
<svg width="480" height="150" viewBox="0 0 480 150" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="10" width="460" height="130" fill="#fafafa" stroke="#ccc" stroke-width="2"/>
  <rect x="30" y="30" width="90" height="40" fill="#185FA5" rx="6"/>
  <rect x="140" y="30" width="90" height="40" fill="#0F6E56" rx="6"/>
  <rect x="250" y="30" width="90" height="40" fill="#993556" rx="6"/>
  <rect x="360" y="30" width="90" height="40" fill="#B5650B" rx="6"/>
  <rect x="30" y="90" width="90" height="40" fill="#533489" rx="6">
    <animate attributeName="y" values="90;90;30;90" dur="3s" repeatCount="indefinite"/>
  </rect>
  <text x="240" y="145" font-family="monospace" font-size="11" fill="#555" text-anchor="middle">flex-wrap: wrap → les boîtes en trop passent à la ligne</text>
</svg>
</div>

| Propriété | Explication pédagogique |
|---|---|
| `flex-wrap: wrap` | Sans ça, Flexbox force **tout sur une seule ligne** et rétrécit les boîtes pour que ça rentre. Avec `wrap`, dès que la place manque, les éléments passent à la ligne suivante. |
| `gap: 16px` | Ajoute un espace **entre** les boîtes uniquement (pas autour), sans avoir à mettre des `margin` sur chaque boîte individuellement. |
| `justify-content: center` | Centre l'ensemble des boîtes sur l'axe principal, même quand la dernière ligne est incomplète. |

<br/>

## 🎴 4. Chaque carte est elle-même un mini flex container (`.box`)

```css
.box {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 10px;
  width: 160px;
  height: 160px;
  background-color: #ffffff;
  border: 1px solid #e0e0e0;
  border-radius: 12px;
  transition: box-shadow 0.2s, border-color 0.2s;
  cursor: default;
}

.box:hover {
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
  border-color: #bdbdbd;
}
```

> 🧠 **Point clé à faire comprendre aux étudiants** : Flexbox n'est pas réservé à la page entière. **N'importe quelle boîte peut devenir un flex container**, y compris une carte à l'intérieur d'un autre flex container. C'est ce qu'on appelle imbriquer des layouts flex (*nested flexbox*).

<div align="center">
<svg width="240" height="240" viewBox="0 0 240 240" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="200" height="200" rx="16" fill="#ffffff" stroke="#e0e0e0" stroke-width="2">
    <animate attributeName="stroke" values="#e0e0e0;#bdbdbd;#e0e0e0" dur="2s" repeatCount="indefinite"/>
  </rect>
  <circle cx="120" cy="95" r="18" fill="#185FA5"/>
  <text x="120" y="145" font-family="Arial" font-size="13" font-weight="bold" fill="#222" text-anchor="middle">Titre</text>
  <text x="120" y="165" font-family="Arial" font-size="10" fill="#888" text-anchor="middle">#01</text>
</svg>
<p><em>flex-direction: column → icône, titre et numéro empilés verticalement, centrés</em></p>
</div>

| Propriété | Rôle dans la carte |
|---|---|
| `flex-direction: column` | Change l'axe principal en **vertical** : les enfants (icône, titre, numéro) s'empilent au lieu de se placer côte à côte |
| `gap: 10px` | Espace vertical entre l'icône, le titre et le numéro |
| `transition: box-shadow 0.2s, border-color 0.2s` | Anime en douceur le changement d'ombre/bordure au survol, au lieu d'un changement brutal |

<br/>

## 🎨 5. Personnalisation par carte (couleurs)

```css
.box-1 .box-icon { color: #185FA5; }
.box-2 .box-icon { color: #0F6E56; }
.box-3 .box-icon { color: #993556; }
.box-4 .box-icon { color: #B5650B; }
.box-5 .box-icon { color: #533489; }
.box-6 .box-icon { color: #A32D2D; }
```

Chaque carte a une classe unique (`.box-1`, `.box-2`...) en plus de `.box`. On combine les deux sélecteurs pour ne changer **qu'une seule propriété** (la couleur de l'icône) sans dupliquer tout le style de la carte.

<br/>

## 🧪 Exercice pour les étudiants

1. Ouvre `CSS/Flex-Box/Flex.css` et le HTML associé.
2. Change `flex-direction: column` en `flex-direction: row` sur `.box` → observe où va l'icône.
3. Remplace `justify-content: center` par `justify-content: space-between` sur `.flex-container` → décris la différence à l'écrit.
4. Réduis la largeur de la fenêtre (ou de la preview) → observe `flex-wrap: wrap` en action.

<br/>

## 📌 Résumé express

| Je veux... | Propriété à utiliser |
|---|---|
| Activer Flexbox | `display: flex` |
| Changer l'axe principal | `flex-direction: row \| column` |
| Aligner sur l'axe principal | `justify-content` |
| Aligner sur l'axe secondaire | `align-items` |
| Espacer sans marges manuelles | `gap` |
| Autoriser le retour à la ligne | `flex-wrap: wrap` |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>