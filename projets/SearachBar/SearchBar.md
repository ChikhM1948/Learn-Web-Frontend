<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:ff4757,100:6366f1&amp;height=180&amp;section=header&amp;text=Search%20Bar%20%F0%9F%94%8D&amp;fontSize=40&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=35&amp;desc=Le%20mini-projet%20SearachBar%20d%C3%A9cortiqu%C3%A9&amp;descAlignY=55&amp;descSize=15"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&amp;size=20&amp;pause=1000&amp;color=FF4757&amp;center=true&amp;vCenter=true&amp;width=650&amp;lines=position%3A+fixed%3B;position%3A+absolute%3B;z-index%3A+999%3B" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&amp;logo=css3&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Projet-SearachBar-ff4757?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif de la fiche

> Ce mini-projet construit une **barre de recherche flottante** avec un bouton intégré à l'intérieur du champ de saisie. Il combine deux notions déjà vues séparément dans les guides du dépôt : `position: fixed` (garder la barre visible au scroll) et `position: absolute` (coller le bouton dans le champ), plus une nouveauté : `z-index`. On décortique ici le code du dossier `projets/SearachBar/`.

<br/>

## 📂 Fichiers du projet

| Fichier | Lien GitHub |
|---|---|
| 🌐 `z-index.html` | [projets/SearachBar/z-index.html](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/projets/SearachBar/z-index.html) |
| 🎨 `z-index.css` | [projets/SearachBar/z-index.css](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/projets/SearachBar/z-index.css) |
| 📘 Ce guide (`SearchBar.md`) | [projets/SearachBar/SearchBar.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/projets/SearachBar/SearchBar.md) |

<br/>

## 🎬 Le concept en une image

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDYwIiBoZWlnaHQ9IjI2MCIgdmlld0JveD0iMCAwIDQ2MCAyNjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iMTAiIHk9IjEwIiB3aWR0aD0iNDQwIiBoZWlnaHQ9IjI0MCIgZmlsbD0iI2Y0ZjRmNCIgc3Ryb2tlPSIjOTk5IiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1kYXNoYXJyYXk9IjUsNCIvPgogIDx0ZXh0IHg9IjI1IiB5PSIzMCIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMSIgZmlsbD0iIzY2NiI+dmlld3BvcnQgKGZlbsOqdHJlIGR1IG5hdmlnYXRldXIpPC90ZXh0PgoKICA8cmVjdCB4PSI2MCIgeT0iOTAiIHdpZHRoPSIzMDAiIGhlaWdodD0iNjAiIGZpbGw9IiNlMGUwZTAiIHJ4PSI0Ii8+CiAgPHJlY3QgeD0iOTAiIHk9IjExMCIgd2lkdGg9IjI0MCIgaGVpZ2h0PSIxNiIgZmlsbD0iI2NmY2ZjZiIgcng9IjIiLz4KICA8dGV4dCB4PSIyMTAiIHk9IjE4MCIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMSIgZmlsbD0iIzk5OSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+bGUgY29udGVudSBkw6lmaWxlIG5vcm1hbGVtZW50Li4uPC90ZXh0PgoKICA8cmVjdCB4PSIzMCIgeT0iNDAiIHdpZHRoPSIxODAiIGhlaWdodD0iNDIiIGZpbGw9IndoaXRlIiBzdHJva2U9IiNjY2MiIHN0cm9rZS13aWR0aD0iMiIgcng9IjIxIj4KICAgIDxhbmltYXRlIGF0dHJpYnV0ZU5hbWU9InkiIHZhbHVlcz0iNDA7MzY7NDAiIGR1cj0iMi41cyIgcmVwZWF0Q291bnQ9ImluZGVmaW5pdGUiLz4KICA8L3JlY3Q+CiAgPHRleHQgeD0iMTIwIiB5PSI2NSIgZm9udC1mYW1pbHk9IkFyaWFsIiBmb250LXNpemU9IjExIiBmaWxsPSIjOTk5IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5TZWFyY2guLi48L3RleHQ+CiAgPHJlY3QgeD0iMTc1IiB5PSI0NiIgd2lkdGg9IjI4IiBoZWlnaHQ9IjMwIiBmaWxsPSIjZmY0NzU3IiByeD0iMTQiLz4KICA8dGV4dCB4PSIyNDAiIHk9IjY1IiBmb250LWZhbWlseT0ibW9ub3NwYWNlIiBmb250LXNpemU9IjExIiBmaWxsPSIjZmY0NzU3IiBmb250LXdlaWdodD0iYm9sZCI+4oaQIHJlc3RlIGljaSwgdG91am91cnMgdmlzaWJsZTwvdGV4dD4KPC9zdmc+" width="480"/>
</div>

<br/>

## 1️⃣ Le conteneur — `.search-box` (relative → fixed + z-index)

```css
.search-box {
  width: 250px;
  position: relative; /* Keeps the button inside */

  position: fixed;    /* Pins it to the screen */
  top: 20px;
  left: 20px;
  z-index: 999;        /* Keeps it on top of page text */
}
```

> ⚠️ **Remarque pédagogique importante** : ce bloc déclare `position` **deux fois** — `relative` puis `fixed`. En CSS, quand une propriété est déclarée deux fois sur le même sélecteur, **c'est la dernière qui gagne**. Ici, `position: fixed` est donc la valeur réellement appliquée ; la ligne `relative` est un commentaire pédagogique volontaire pour montrer la progression, mais n'a aucun effet au final. Dans un vrai projet, on ne garderait qu'une seule des deux lignes.

| Propriété | Rôle |
|---|---|
| `position: fixed` | Épingle la barre à un endroit précis de **l'écran**, qui reste visible même en scrollant toute la page |
| `top: 20px; left: 20px;` | Positionne la barre à 20px du haut et du bord gauche de la fenêtre |
| `z-index: 999` | Force la barre à s'afficher **au-dessus** de tout le reste du contenu de la page, même si d'autres éléments la chevauchent visuellement |

> 🧠 **`z-index` en une phrase** : plus la valeur est grande, plus l'élément est "proche de l'œil" et s'affiche par-dessus les éléments avec un `z-index` plus petit. Il ne fonctionne **que** sur des éléments positionnés (`relative`, `absolute`, `fixed` ou `sticky`) — jamais sur un élément `static`.

<br/>

## 2️⃣ Le champ de saisie — `input`

```css
input {
  width: 100%;
  padding: 10px;
  border: 2px solid #ccc;
  border-radius: 20px; /* Makes the input box rounded */
  box-sizing: border-box;
  outline: none;
}
```

| Propriété | Rôle |
|---|---|
| `width: 100%` | Le champ prend toute la largeur de `.search-box` (250px), et non une largeur fixe codée en dur |
| `border-radius: 20px` | Une valeur proche de la moitié de la hauteur du champ = coins totalement arrondis (effet "pilule") |
| `box-sizing: border-box` | La bordure de 2px et le padding sont **inclus** dans les 100% de largeur, au lieu de s'ajouter par-dessus |
| `outline: none` | Supprime le contour bleu par défaut du navigateur au focus — attention, à remplacer par un style `:focus` personnalisé pour ne pas nuire à l'accessibilité |

<br/>

## 3️⃣ Le bouton — `button` (absolute imbriqué)

```css
button {
  position: absolute; /* Pulls it inside the input */
  right: 4px;
  top: 4px;
  bottom: 4px;         /* Pushes it perfectly into the right corner */

  background-color: #ff4757;
  color: white;
  border: none;
  border-radius: 15px;
  padding: 0 15px;
  cursor: pointer;
}
```

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzgwIiBoZWlnaHQ9IjE0MCIgdmlld0JveD0iMCAwIDM4MCAxNDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iMjAiIHk9IjQwIiB3aWR0aD0iMzAwIiBoZWlnaHQ9IjYwIiBmaWxsPSJ3aGl0ZSIgc3Ryb2tlPSIjY2NjIiBzdHJva2Utd2lkdGg9IjIiIHJ4PSIzMCIvPgogIDx0ZXh0IHg9IjE0MCIgeT0iNzUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMyIgZmlsbD0iIzk5OSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+U2VhcmNoLi4uPC90ZXh0PgogIDxyZWN0IHg9IjI1NSIgeT0iNDYiIHdpZHRoPSI1NSIgaGVpZ2h0PSI0OCIgZmlsbD0iI2ZmNDc1NyIgcng9IjI0Ij4KICAgIDxhbmltYXRlIGF0dHJpYnV0ZU5hbWU9Im9wYWNpdHkiIHZhbHVlcz0iMTswLjc7MSIgZHVyPSIycyIgcmVwZWF0Q291bnQ9ImluZGVmaW5pdGUiLz4KICA8L3JlY3Q+CiAgPHRleHQgeD0iMjgyIiB5PSI3NSIgZm9udC1mYW1pbHk9IkFyaWFsIiBmb250LXNpemU9IjEyIiBmaWxsPSJ3aGl0ZSIgdGV4dC1hbmNob3I9Im1pZGRsZSIgZm9udC13ZWlnaHQ9ImJvbGQiPkdvPC90ZXh0PgogIDx0ZXh0IHg9IjE5MCIgeT0iMTI1IiBmb250LWZhbWlseT0ibW9ub3NwYWNlIiBmb250LXNpemU9IjEwIiBmaWxsPSIjNTU1IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5yaWdodDogNHB4OyB0b3A6IDRweDsgYm90dG9tOiA0cHg7IOKGkiBsZSBib3V0b24gY29sbGUgYXUgYm9yZCBkcm9pdCwgYXZlYyA0cHggZGUgbWFyZ2U8L3RleHQ+Cjwvc3ZnPg==" width="480"/>
</div>

> 🧠 **La technique clé de ce fichier** : `top: 4px; bottom: 4px;` **en même temps** sur un élément `absolute` force sa hauteur à s'ajuster automatiquement pour occuper tout l'espace entre le haut et le bas de son référentiel, moins 4px de chaque côté. Pas besoin de calculer une `height` fixe : le bouton s'adapte toujours parfaitement à la hauteur du champ `input`, même si elle change.

| Propriété | Rôle |
|---|---|
| `position: absolute` | Sort le bouton du flux normal pour le placer précisément **par rapport à `.search-box`** (voir le piège classique : `.search-box` doit être positionné pour que ça marche — ici c'est le cas via `fixed`) |
| `right: 4px` | Colle le bouton à 4px du bord droit |
| `top: 4px; bottom: 4px;` | Étire verticalement le bouton pour remplir la hauteur disponible, avec 4px de marge en haut et en bas |
| `cursor: pointer` | Change le curseur en "main cliquable" au survol — un détail qui améliore l'expérience utilisateur |

<br/>

## 🔗 Le lien avec les guides `Position.md`

Ce mini-projet est une application directe de deux notions du guide **[Position.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/CSS/Position/Position.md)** :

| Notion du cours | Usage ici |
|---|---|
| `position: fixed` | Garder la barre de recherche visible même en scrollant |
| `position: absolute` + référentiel positionné | Ancrer le bouton précisément à l'intérieur du champ de recherche |
| *(nouveau)* `z-index` | Gérer l'ordre d'empilement quand plusieurs éléments positionnés se chevauchent |

<br/>

## 📄 Le code complet

### `z-index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="z-index.css">
</head>
<body>
<div class="search-box">
  <input type="text" placeholder="Search...">
  <button>Go</button>
</div>

</body>
</html>
```

### `z-index.css`

```css
/* 1. THE CONTAINER (Relative + Fixed + Z-Index) */
.search-box {
  width: 250px;
  position: relative; /* Keeps the button inside */

  position: fixed;    /* Pins it to the screen */
  top: 20px;
  left: 20px;
  z-index: 999;       /* Keeps it on top of page text */
}

/* 2. THE INPUT (With rounded corners) */
input {
  width: 100%;
  padding: 10px;
  border: 2px solid #ccc;
  border-radius: 20px; /* Makes the input box rounded */
  box-sizing: border-box;
  outline: none;
}

/* 3. THE RED BUTTON (Absolute + Styled) */
button {
  position: absolute; /* Pulls it inside the input */
  right: 4px;
  top: 4px;
  bottom: 4px;        /* Pushes it perfectly into the right corner */

  background-color: #ff4757; /* The Red Color */
  color: white;
  border: none;
  border-radius: 15px;       /* Makes the button match the rounded input */
  padding: 0 15px;
  cursor: pointer;
}
```

<br/>

## 🧪 Exercices pour les étudiants

1. Supprime la ligne `z-index: 999;` et ajoute du texte long dans la page avec un `z-index` supérieur ailleurs → observe ce qui passe devant la barre de recherche.
2. Change `position: fixed` en `position: absolute` sur `.search-box` → scrolle la page et observe la différence de comportement.
3. Retire `bottom: 4px;` du bouton et ajoute `height: 100%;` à la place → compare le résultat.
4. Ajoute un deuxième élément `position: fixed` ailleurs sur la page avec un `z-index` plus grand que 999 → vérifie qu'il passe devant la barre de recherche.
5. **Défi** : transforme cette barre de recherche flottante en barre **collante** (`position: sticky`) qui ne reste visible que dans une section précise de la page, au lieu de toute la page (voir le guide Position.md, section `sticky`).

<br/>

## 📌 Résumé express

| Je veux... | Propriété |
|---|---|
| Garder un élément visible même en scrollant toute la page | `position: fixed` |
| Ancrer un élément précisément à l'intérieur d'un parent | `position: absolute` (parent positionné) |
| Étirer un élément absolute sur toute la hauteur disponible | `top` + `bottom` définis en même temps, sans `height` |
| Gérer quel élément s'affiche par-dessus un autre | `z-index` (uniquement sur éléments positionnés) |
| Arrondir complètement les coins d'un bouton/champ | `border-radius` proche de la moitié de la hauteur |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>
