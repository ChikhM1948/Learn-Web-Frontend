<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:0f172a,100:6366f1&amp;height=180&amp;section=header&amp;text=Background%20%F0%9F%8E%A8&amp;fontSize=42&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=35&amp;desc=Couleurs%2C%20images%20et%20d%C3%A9grad%C3%A9s&amp;descAlignY=55&amp;descSize=16"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&amp;size=20&amp;pause=1000&amp;color=6366F1&amp;center=true&amp;vCenter=true&amp;width=650&amp;lines=background-color+%E2%80%A2+background-image;background-size%3A+cover%3B;linear-gradient()" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&amp;logo=css3&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Cours-Background-0f172a?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif du cours

> La propriété `background` (et ses variantes) contrôle **tout ce qui s'affiche derrière le contenu** d'une boîte : couleur unie, image, dégradé, ou une combinaison des trois.

<br/>

## 1️⃣ `background-color` — la base

```css
.carte {
  background-color: #f4f4f4;
}
```

> La forme la plus simple : une couleur unie derrière le contenu. Fonctionne avec les codes hexadécimaux (`#f4f4f4`), `rgb()`, `rgba()` (avec transparence), ou les noms de couleurs CSS.

<br/>

## 2️⃣ `background-image` — insérer une image

```css
.hero {
  background-image: url('photo-etudiants.jpg');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
```

| Propriété | Rôle |
|---|---|
| `background-image: url(...)` | Insère l'image en arrière-plan |
| `background-repeat: no-repeat` | Empêche l'image de se répéter en mosaïque (comportement par défaut) |
| `background-position: center` | Centre l'image dans la boîte |
| `background-size` | Contrôle la taille de l'image — voir section suivante |

<br/>

## 3️⃣ `background-size: cover` vs `contain`

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDQwIiBoZWlnaHQ9IjE2MCIgdmlld0JveD0iMCAwIDQ0MCAxNjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iMjAiIHk9IjIwIiB3aWR0aD0iMTgwIiBoZWlnaHQ9IjEyMCIgZmlsbD0iIzBmMTcyYSIgc3Ryb2tlPSIjMzMzIiBzdHJva2Utd2lkdGg9IjIiLz4KICA8cmVjdCB4PSIyMCIgeT0iMjAiIHdpZHRoPSIyNjAiIGhlaWdodD0iODAiIGZpbGw9IiMzOGJkZjgiIG9wYWNpdHk9IjAuNyIvPgogIDx0ZXh0IHg9IjExMCIgeT0iMTUwIiBmb250LWZhbWlseT0ibW9ub3NwYWNlIiBmb250LXNpemU9IjExIiBmaWxsPSIjNTU1IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5jb3ZlciAoZMOpYm9yZGUsIHJlY2FkcmUpPC90ZXh0PgoKICA8cmVjdCB4PSIyNDAiIHk9IjIwIiB3aWR0aD0iMTgwIiBoZWlnaHQ9IjEyMCIgZmlsbD0iIzBmMTcyYSIgc3Ryb2tlPSIjMzMzIiBzdHJva2Utd2lkdGg9IjIiLz4KICA8cmVjdCB4PSIyNDAiIHk9IjIwIiB3aWR0aD0iMTIwIiBoZWlnaHQ9IjgwIiBmaWxsPSIjOGI1Y2Y2IiBvcGFjaXR5PSIwLjciLz4KICA8dGV4dCB4PSIzMzAiIHk9IjE1MCIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMSIgZmlsbD0iIzU1NSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+Y29udGFpbiAodGllbnQgZW50aWVyLCBib3JkcyB2aWRlcyk8L3RleHQ+Cjwvc3ZnPg==" width="480"/>
</div>

| Valeur | Comportement |
|---|---|
| `cover` | L'image **remplit toute la boîte**, quitte à être recadrée sur les bords |
| `contain` | L'image **tient entièrement** dans la boîte, quitte à laisser des bandes vides |

> 💡 **`cover` est le choix n°1** pour les bannières/héros de page (l'image remplit tout l'espace sans jamais laisser de bande vide). **`contain`** convient mieux pour un logo qui ne doit jamais être recadré.

<br/>

## 4️⃣ `background-attachment: fixed` — effet parallaxe simple

```css
.section-parallaxe {
  background-image: url('paysage.jpg');
  background-size: cover;
  background-attachment: fixed;
}
```

> 🧠 `background-attachment: fixed` fige l'image d'arrière-plan **par rapport à la fenêtre** (comme `position: fixed` — voir le guide `Position.md`), pendant que le contenu défile par-dessus. C'est la technique la plus simple pour un effet "parallaxe" léger, sans JavaScript.

<br/>

## 5️⃣ Dégradés — `linear-gradient()`

```css
.banniere {
  background: linear-gradient(to right, #6366f1, #38bdf8);
}
```

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDIwIiBoZWlnaHQ9IjE0MCIgdmlld0JveD0iMCAwIDQyMCAxNDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPGRlZnM+CiAgICA8bGluZWFyR3JhZGllbnQgaWQ9ImcxIiB4MT0iMCUiIHkxPSIwJSIgeDI9IjEwMCUiIHkyPSIwJSI+CiAgICAgIDxzdG9wIG9mZnNldD0iMCUiIHN0b3AtY29sb3I9IiM2MzY2ZjEiLz4KICAgICAgPHN0b3Agb2Zmc2V0PSIxMDAlIiBzdG9wLWNvbG9yPSIjMzhiZGY4Ii8+CiAgICA8L2xpbmVhckdyYWRpZW50PgogIDwvZGVmcz4KICA8cmVjdCB4PSIyMCIgeT0iMjAiIHdpZHRoPSIzODAiIGhlaWdodD0iMTAwIiBmaWxsPSJ1cmwoI2cxKSIgcng9IjgiLz4KICA8dGV4dCB4PSIyMTAiIHk9Ijc1IiBmb250LWZhbWlseT0ibW9ub3NwYWNlIiBmb250LXNpemU9IjEzIiBmaWxsPSJ3aGl0ZSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+bGluZWFyLWdyYWRpZW50KHRvIHJpZ2h0LCAjNjM2NmYxLCAjMzhiZGY4KTwvdGV4dD4KPC9zdmc+" width="480"/>
</div>

```css
/* Dégradé diagonal à 3 couleurs */
.banniere-2 {
  background: linear-gradient(135deg, #f59e0b, #dc2626, #6366f1);
}

/* Dégradé radial (depuis le centre) */
.spot {
  background: radial-gradient(circle, #ffffff, #cbd5e1);
}
```

> 🧠 `linear-gradient(direction, couleur1, couleur2, ...)` — la direction peut être `to right`, `to bottom`, ou un angle précis (`135deg`). On peut combiner autant de couleurs qu'on veut, séparées par des virgules.

<br/>

## 6️⃣ La propriété raccourcie `background`

```css
.element {
  background: #1e293b url('texture.png') no-repeat center / cover;
}
```

> ⚠️ **Ordre à respecter** dans le raccourci : couleur, puis image, puis répétition, puis position, puis (après un `/`) la taille. On peut omettre les valeurs non utilisées, mais l'ordre relatif reste important.

<br/>

## 📌 Résumé express

| Je veux... | Propriété |
|---|---|
| Une couleur de fond unie | `background-color` |
| Insérer une image de fond | `background-image: url(...)` |
| Empêcher la répétition en mosaïque | `background-repeat: no-repeat` |
| Faire remplir toute la boîte à l'image | `background-size: cover` |
| Garder l'image entière visible | `background-size: contain` |
| Un effet parallaxe simple | `background-attachment: fixed` |
| Un dégradé de couleurs | `linear-gradient()` / `radial-gradient()` |

<br/>

## 🧪 Exercices

### Exercice 1 — Bannière avec dégradé

```css
.banniere {
  background: ____(to right, #6366f1, #38bdf8); /* complétez la fonction */
  height: 200px;
}
```

### Exercice 2 — Image de fond bien cadrée

Ajoutez une image de fond à une section de 300px de hauteur, en veillant à ce qu'elle **remplisse tout l'espace sans se répéter et sans se déformer**, quelle que soit la largeur de l'écran.

### Exercice 3 — Section parallaxe

Construisez une section de 400px de hauteur avec une image de fond en `background-attachment: fixed`, précédée et suivie de blocs de texte assez longs pour pouvoir scroller et observer l'effet.

### 📊 Grille d'évaluation

| Critère | Points |
|---|---|
| Exercice 1 complété | 4 |
| Exercice 2 — image bien cadrée en `cover` | 8 |
| Exercice 3 — effet parallaxe observable | 8 |
| **Total** | **20** |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>
