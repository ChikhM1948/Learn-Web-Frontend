<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:f59e0b,100:dc2626&amp;height=180&amp;section=header&amp;text=Float%20%E2%9A%93%EF%B8%8F&amp;fontSize=45&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=35&amp;desc=La%20technique%20historique%20de%20mise%20en%20page&amp;descAlignY=55&amp;descSize=15"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&amp;size=20&amp;pause=1000&amp;color=F59E0B&amp;center=true&amp;vCenter=true&amp;width=650&amp;lines=float%3A+left%3B;clear%3A+both%3B;aujourd'hui%3A+surtout+pour+le+texte" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&amp;logo=css3&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Cours-Float-f59e0b?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif du cours

> `float` a longtemps été **la seule technique** pour construire des mises en page à colonnes en CSS, avant Flexbox et Grid. Aujourd'hui, on l'utilise surtout pour **faire flotter du texte autour d'une image** — comme dans un article de magazine — et il reste important de le comprendre pour lire du code existant.

<br/>

## 🖼️ Le concept : le texte qui "flotte" autour

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDQwIiBoZWlnaHQ9IjE4MCIgdmlld0JveD0iMCAwIDQ0MCAxODAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iMjAiIHk9IjIwIiB3aWR0aD0iOTAiIGhlaWdodD0iOTAiIGZpbGw9IiNmNTllMGIiIHJ4PSI2Ij4KICAgIDxhbmltYXRlIGF0dHJpYnV0ZU5hbWU9IngiIHZhbHVlcz0iMjA7MjU7MjAiIGR1cj0iMi41cyIgcmVwZWF0Q291bnQ9ImluZGVmaW5pdGUiLz4KICA8L3JlY3Q+CiAgPHRleHQgeD0iNjUiIHk9IjcwIiBmb250LWZhbWlseT0ibW9ub3NwYWNlIiBmb250LXNpemU9IjExIiBmaWxsPSJ3aGl0ZSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+ZmxvYXQ6IGxlZnQ8L3RleHQ+CiAgPHJlY3QgeD0iMTI1IiB5PSIyMCIgd2lkdGg9IjI5MCIgaGVpZ2h0PSIxMCIgZmlsbD0iI2U1ZTdlYiIvPgogIDxyZWN0IHg9IjEyNSIgeT0iMzgiIHdpZHRoPSIyOTAiIGhlaWdodD0iMTAiIGZpbGw9IiNlNWU3ZWIiLz4KICA8cmVjdCB4PSIxMjUiIHk9IjU2IiB3aWR0aD0iMjkwIiBoZWlnaHQ9IjEwIiBmaWxsPSIjZTVlN2ViIi8+CiAgPHJlY3QgeD0iMTI1IiB5PSI3NCIgd2lkdGg9IjI5MCIgaGVpZ2h0PSIxMCIgZmlsbD0iI2U1ZTdlYiIvPgogIDxyZWN0IHg9IjIwIiB5PSIxMjUiIHdpZHRoPSIzOTAiIGhlaWdodD0iMTAiIGZpbGw9IiNlNWU3ZWIiLz4KICA8cmVjdCB4PSIyMCIgeT0iMTQzIiB3aWR0aD0iMzkwIiBoZWlnaHQ9IjEwIiBmaWxsPSIjZTVlN2ViIi8+CiAgPHRleHQgeD0iMjIwIiB5PSIxNjUiIGZvbnQtZmFtaWx5PSJtb25vc3BhY2UiIGZvbnQtc2l6ZT0iMTEiIGZpbGw9IiM1NTUiIHRleHQtYW5jaG9yPSJtaWRkbGUiPmxlIHRleHRlICJmbG90dGUiIGF1dG91ciBkZSBsJ8OpbMOpbWVudCBmbG90dMOpPC90ZXh0Pgo8L3N2Zz4=" width="480"/>
</div>

```css
.illustration {
  float: left;
  width: 120px;
  margin-right: 16px;
}
```

> 🧠 `float: left` sort l'image du flux normal du texte et la pousse à gauche ; **le texte qui suit remonte et s'enroule automatiquement** autour d'elle, exactement comme dans un journal papier.

<br/>

## 1️⃣ `float: left` / `float: right`

```css
.image-gauche  { float: left;  margin-right: 16px; }
.image-droite  { float: right; margin-left: 16px; }
```

| Valeur | Effet |
|---|---|
| `float: left` | Pousse l'élément à gauche, le texte suivant s'enroule à droite |
| `float: right` | Pousse l'élément à droite, le texte suivant s'enroule à gauche |
| `float: none` (défaut) | Comportement normal, pas de flottement |

<br/>

## 2️⃣ Le problème du "parent qui s'effondre"

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDIwIiBoZWlnaHQ9IjE2MCIgdmlld0JveD0iMCAwIDQyMCAxNjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iMjAiIHk9IjIwIiB3aWR0aD0iMzgwIiBoZWlnaHQ9IjEwIiBmaWxsPSIjZjU5ZTBiIiByeD0iMyIvPgogIDxyZWN0IHg9IjIwIiB5PSI0MCIgd2lkdGg9IjE4MCIgaGVpZ2h0PSI2MCIgZmlsbD0iI2Y1OWUwYiIgcng9IjQiIG9wYWNpdHk9IjAuOCIvPgogIDxyZWN0IHg9IjIxMCIgeT0iNDAiIHdpZHRoPSIxODAiIGhlaWdodD0iNjAiIGZpbGw9IiNmNTllMGIiIHJ4PSI0IiBvcGFjaXR5PSIwLjgiLz4KICA8cmVjdCB4PSIxMCIgeT0iMTAiIHdpZHRoPSI0MDAiIGhlaWdodD0iMTQwIiBmaWxsPSJub25lIiBzdHJva2U9IiNkYzI2MjYiIHN0cm9rZS13aWR0aD0iMyIgc3Ryb2tlLWRhc2hhcnJheT0iNiw0Ij4KICAgIDxhbmltYXRlIGF0dHJpYnV0ZU5hbWU9ImhlaWdodCIgdmFsdWVzPSIyMDsxNDA7MjAiIGR1cj0iM3MiIHJlcGVhdENvdW50PSJpbmRlZmluaXRlIi8+CiAgPC9yZWN0PgogIDx0ZXh0IHg9IjIxMCIgeT0iMTMwIiBmb250LWZhbWlseT0ibW9ub3NwYWNlIiBmb250LXNpemU9IjExIiBmaWxsPSIjZGMyNjI2IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5zYW5zIGNsZWFyZml4LCBsZSBwYXJlbnQgInMnZWZmb25kcmUiIGF1dG91ciBkZXMgw6lsw6ltZW50cyBmbG90dMOpczwvdGV4dD4KPC9zdmc+" width="480"/>
</div>

> ⚠️ **Le piège historique n°1 de `float`** : un élément flotté **sort du flux normal**, donc son parent ne "voit" plus sa hauteur. Si toutes les cases d'un parent sont flottées, le parent peut s'effondrer à une hauteur de 0px, cassant toute la mise en page derrière lui (bordures invisibles, fond de couleur absent...).

<br/>

## 3️⃣ `clear` — reprendre le contrôle

```css
.apres-les-flottants {
  clear: both;
}
```

| Valeur | Effet |
|---|---|
| `clear: left` | L'élément descend sous tout élément flottant à gauche |
| `clear: right` | L'élément descend sous tout élément flottant à droite |
| `clear: both` | L'élément descend sous **tous** les éléments flottants |

<br/>

## 4️⃣ Le "clearfix" — la solution historique

```css
.conteneur::after {
  content: "";
  display: block;
  clear: both;
}
```

> 🧠 Cette astuce (encore visible dans beaucoup de vieux projets) ajoute un élément invisible **après** les enfants flottés, avec `clear: both`, pour forcer le parent à retrouver sa vraie hauteur. Aujourd'hui, ce problème ne se pose presque plus grâce à Flexbox/Grid — mais il reste essentiel pour comprendre du code CSS plus ancien.

<br/>

## 🆚 Float vs Flexbox/Grid — le contexte historique

| Époque | Technique de mise en page |
|---|---|
| Avant ~2015 | `float` + `clearfix` pour toutes les mises en page à colonnes |
| Aujourd'hui | `float` réservé au texte qui s'enroule autour d'une image ; Flexbox/Grid pour tout le reste |

<br/>

## 📌 Résumé express

| Je veux... | Propriété |
|---|---|
| Faire flotter un élément à gauche | `float: left` |
| Faire flotter un élément à droite | `float: right` |
| Forcer un élément à descendre sous les flottants | `clear: both` |
| Empêcher un parent de s'effondrer autour de ses enfants flottés | Le "clearfix" (`::after` + `clear: both`) |

<br/>

## 🧪 Exercices

### Exercice 1 — Texte qui s'enroule

```css
.photo-auteur {
  ____: left;      /* (1) fait flotter l'image à gauche */
  width: 100px;
  margin-right: ____px; /* (2) un espace raisonnable avec le texte */
}
```

**Consigne** : complétez pour que le texte d'un paragraphe s'enroule proprement autour d'une image de 100px flottée à gauche.

### Exercice 2 — Le parent qui s'effondre

Créez un parent contenant 3 `<div>` flottées à gauche (`float: left`), sans clearfix. Observez que le parent (avec une bordure visible) a une hauteur de 0px. Puis ajoutez le clearfix de la section 4 et observez la différence.

### Exercice 3 — Mini mise en page à l'ancienne

Construisez une mise en page à 2 colonnes **uniquement avec `float`** (une sidebar de 200px flottée à gauche, un contenu principal qui prend le reste), avec un clearfix sur le parent. Comparez ensuite mentalement avec la même mise en page en Flexbox (guide `Flexbox.md`).

### 📊 Grille d'évaluation

| Critère | Points |
|---|---|
| Exercice 1 complété | 4 |
| Exercice 2 — parent qui s'effondre puis corrigé | 8 |
| Exercice 3 — mise en page 2 colonnes fonctionnelle | 8 |
| **Total** | **20** |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>
