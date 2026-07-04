<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:2c3e50,100:1abc9c&amp;height=180&amp;section=header&amp;text=Navbar%20avec%20Flexbox%20%F0%9F%A7%AD&amp;fontSize=38&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=35&amp;desc=Le%20mini-projet%20Simple-Navbar%20d%C3%A9cortiqu%C3%A9&amp;descAlignY=55&amp;descSize=15"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&amp;size=20&amp;pause=1000&amp;color=1ABC9C&amp;center=true&amp;vCenter=true&amp;width=650&amp;lines=display%3A+flex%3B;justify-content%3A+space-between%3B;responsive+avec+%40media" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&amp;logo=css3&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Projet-Simple--Navbar-2c3e50?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif de la fiche

> Ce mini-projet construit une **barre de navigation** classique avec Flexbox : logo à gauche, liens à droite, et un état actif/survolé sur les liens. On décortique ici le code du dossier `projets/Simple-Navbar/`, ligne par ligne.

<br/>

## 📂 Fichiers du projet

| Fichier | Lien GitHub |
|---|---|
| 🌐 `index.html` | [projets/Simple-Navbar/index.html](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/projets/Simple-Navbar/index.html) |
| 🎨 `styles.css` | [projets/Simple-Navbar/styles.css](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/projets/Simple-Navbar/styles.css) |
| 📘 Ce guide (`Navbar.md`) | [projets/Simple-Navbar/Navbar.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/projets/Simple-Navbar/Navbar.md) |

<br/>

## 🎬 Le concept en une image

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDgwIiBoZWlnaHQ9IjEyMCIgdmlld0JveD0iMCAwIDQ4MCAxMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iMTAiIHk9IjMwIiB3aWR0aD0iNDYwIiBoZWlnaHQ9IjYwIiBmaWxsPSIjMmMzZTUwIiByeD0iNiIvPgogIDx0ZXh0IHg9IjM1IiB5PSI2NSIgZm9udC1mYW1pbHk9IkFyaWFsIiBmb250LXNpemU9IjE0IiBmaWxsPSJ3aGl0ZSIgZm9udC13ZWlnaHQ9ImJvbGQiPkxpbmdvTGFiIEFjYWRlbXk8L3RleHQ+CiAgPHRleHQgeD0iMjMwIiB5PSI2NSIgZm9udC1mYW1pbHk9IkFyaWFsIiBmb250LXNpemU9IjEyIiBmaWxsPSIjMWFiYzljIj5Ib21lPC90ZXh0PgogIDx0ZXh0IHg9IjI5MCIgeT0iNjUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMiIgZmlsbD0id2hpdGUiPkFib3V0PC90ZXh0PgogIDx0ZXh0IHg9IjM1NSIgeT0iNjUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMiIgZmlsbD0id2hpdGUiPlNlcnZpY2VzPC90ZXh0PgogIDx0ZXh0IHg9IjQzMCIgeT0iNjUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMiIgZmlsbD0id2hpdGUiPkNvbnRhY3Q8L3RleHQ+CiAgPGxpbmUgeDE9IjM1IiB5MT0iMTAwIiB4Mj0iMzUiIHkyPSIzMCIgc3Ryb2tlPSIjMzhiZGY4IiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1kYXNoYXJyYXk9IjQsMyI+CiAgICA8YW5pbWF0ZSBhdHRyaWJ1dGVOYW1lPSJ4MSIgdmFsdWVzPSIzNTszNSIgZHVyPSIxcyIvPgogIDwvbGluZT4KICA8bGluZSB4MT0iNDUwIiB5MT0iMTAwIiB4Mj0iNDUwIiB5Mj0iMzAiIHN0cm9rZT0iIzM4YmRmOCIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtZGFzaGFycmF5PSI0LDMiLz4KICA8dGV4dCB4PSIyNDAiIHk9IjExMiIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMSIgZmlsbD0iIzU1NSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+anVzdGlmeS1jb250ZW50OiBzcGFjZS1iZXR3ZWVuIOKGkiBsb2dvIMOgIGdhdWNoZSwgbGllbnMgw6AgZHJvaXRlPC90ZXh0Pgo8L3N2Zz4=" width="480"/>
</div>

<br/>

## 1️⃣ Le reset et la police globale

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
```

> 🧠 Le reset classique (voir aussi le guide Flexbox) : on supprime les espacements par défaut du navigateur, on force `box-sizing: border-box`, et on fixe **une seule police pour toute la page** dès le départ — pas besoin de la répéter partout.

<br/>

## 2️⃣ Le conteneur `.navbar` — le cœur du layout

```css
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #2c3e50;
    padding: 15px 30px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}
```

| Propriété | Rôle |
|---|---|
| `display: flex` | Active Flexbox — logo et liste de liens deviennent des flex items côte à côte |
| `justify-content: space-between` | Pousse le premier élément (`logo`) tout à gauche et le dernier (`liens`) tout à droite, avec l'espace disponible entre les deux |
| `align-items: center` | Centre verticalement le logo et les liens, même s'ils ont des tailles différentes |
| `box-shadow` | Une ombre légère qui détache visuellement la navbar du contenu en dessous |

> 💡 **`space-between` est LA propriété clé de ce projet** : sans elle, il faudrait calculer manuellement des marges pour pousser les liens à droite. Avec Flexbox, une seule ligne suffit.

<br/>

## 3️⃣ Le logo — `.nav-logo`

```css
.nav-logo a {
    color: #ffffff;
    font-size: 24px;
    font-weight: bold;
    text-decoration: none;
}
```

> `text-decoration: none` retire le soulignement par défaut des liens `<a>` — indispensable dès qu'un lien sert de logo ou de bouton plutôt que de lien de texte classique.

<br/>

## 4️⃣ La liste de liens — `.nav-links`

```css
.nav-links {
    display: flex;
    list-style: none;
    gap: 20px;
}
```

> 🧠 **Point important** : `.nav-links` est **elle-même un flex container**, imbriquée dans `.navbar` qui en est un autre. C'est exactement le même principe de "Flexbox imbriqué" vu dans le guide Flexbox (`.box` à l'intérieur de `.flex-container`). `list-style: none` supprime les puces `<ul>`, et `gap: 20px` espace les liens sans avoir besoin de marges sur chaque `<li>`.

<br/>

## 5️⃣ États des liens — normal, survol, actif

```css
.nav-links a {
    color: #ffffff;
    text-decoration: none;
    font-size: 16px;
    font-weight: 500;
    transition: color 0.3s ease;
}

.nav-links a:hover,
.nav-links a.active {
    color: #1abc9c;
}
```

> `:hover` (survol de la souris) et `.active` (page actuelle) partagent la **même couleur turquoise**, séparées par une virgule dans le sélecteur pour éviter de dupliquer la règle. La `transition` rend le changement de couleur progressif plutôt que brutal.

<br/>

## 6️⃣ Responsive — la navbar sur mobile

```css
@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
        gap: 15px;
    }

    .nav-links li {
        margin: 0 10px;
    }
}
```

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDIwIiBoZWlnaHQ9IjIyMCIgdmlld0JveD0iMCAwIDQyMCAyMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHRleHQgeD0iMjEwIiB5PSIxOCIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMSIgZmlsbD0iIzU1NSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+ZmxleC1kaXJlY3Rpb246IGNvbHVtbiAobW9iaWxlLCBzb3VzIDYwMHB4KTwvdGV4dD4KICA8cmVjdCB4PSI5MCIgeT0iMzAiIHdpZHRoPSIyNDAiIGhlaWdodD0iMTgwIiBmaWxsPSIjMmMzZTUwIiByeD0iOCIvPgogIDx0ZXh0IHg9IjIxMCIgeT0iNjUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMyIgZmlsbD0id2hpdGUiIHRleHQtYW5jaG9yPSJtaWRkbGUiIGZvbnQtd2VpZ2h0PSJib2xkIj4KICAgIDxhbmltYXRlIGF0dHJpYnV0ZU5hbWU9Im9wYWNpdHkiIHZhbHVlcz0iMTswLjY7MSIgZHVyPSIycyIgcmVwZWF0Q291bnQ9ImluZGVmaW5pdGUiLz4KICAgIExpbmdvTGFiIEFjYWRlbXkKICA8L3RleHQ+CiAgPHRleHQgeD0iMjEwIiB5PSIxMDUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMSIgZmlsbD0iIzFhYmM5YyIgdGV4dC1hbmNob3I9Im1pZGRsZSI+SG9tZTwvdGV4dD4KICA8dGV4dCB4PSIyMTAiIHk9IjEzMCIgZm9udC1mYW1pbHk9IkFyaWFsIiBmb250LXNpemU9IjExIiBmaWxsPSJ3aGl0ZSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+QWJvdXQ8L3RleHQ+CiAgPHRleHQgeD0iMjEwIiB5PSIxNTUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMSIgZmlsbD0id2hpdGUiIHRleHQtYW5jaG9yPSJtaWRkbGUiPlNlcnZpY2VzPC90ZXh0PgogIDx0ZXh0IHg9IjIxMCIgeT0iMTgwIiBmb250LWZhbWlseT0iQXJpYWwiIGZvbnQtc2l6ZT0iMTEiIGZpbGw9IndoaXRlIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5Db250YWN0PC90ZXh0Pgo8L3N2Zz4=" width="480"/>
</div>

> 🧠 En dessous de 600px de large, `flex-direction: column` fait basculer l'axe principal de horizontal à vertical : le logo et les liens s'empilent au lieu d'être côte à côte. C'est le **seul changement nécessaire** pour rendre toute la navbar responsive.

<br/>

## 📄 Le code complet

### `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Navbar</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <nav class="navbar">
        <div class="nav-logo">
            <a href="#">LingoLab Academy</a>
        </div>
        <ul class="nav-links">
            <li><a href="#" class="active">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

</body>
</html>
```

### `styles.css`

```css
/* Reset basic styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

/* Navbar container */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #2c3e50;
    padding: 15px 30px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

/* Logo styling */
.nav-logo a {
    color: #ffffff;
    font-size: 24px;
    font-weight: bold;
    text-decoration: none;
}

/* Navigation links container */
.nav-links {
    display: flex;
    list-style: none;
    gap: 20px;
}

/* Styling for the links */
.nav-links a {
    color: #ffffff;
    text-decoration: none;
    font-size: 16px;
    font-weight: 500;
    transition: color 0.3s ease;
}

/* Hover and active states */
.nav-links a:hover,
.nav-links a.active {
    color: #1abc9c;
}

/* Simple responsive adjustment for smaller screens */
@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
        gap: 15px;
    }

    .nav-links li {
        margin: 0 10px;
    }
}
```

<br/>

## 🧪 Exercices pour les étudiants

1. Change `justify-content: space-between` en `justify-content: center` → observe où partent les liens.
2. Ajoute un 5ème lien "Blog" dans `.nav-links` sans toucher au CSS → vérifie que `gap` l'espace automatiquement.
3. Remplace la couleur `#1abc9c` par une autre couleur de ton choix, dans **une seule variable CSS** (`:root`) réutilisée à deux endroits.
4. Réduis la fenêtre sous 600px → observe le passage en `flex-direction: column`.
5. **Défi** : ajoute une icône "hamburger" (☰) visible uniquement sous 600px qui affiche/masque les liens au clic (HTML + CSS uniquement, pas besoin de JavaScript pour l'affichage simple).

<br/>

## 📌 Résumé express

| Je veux... | Propriété |
|---|---|
| Pousser deux éléments aux extrémités opposées | `justify-content: space-between` |
| Centrer verticalement des éléments de tailles différentes | `align-items: center` |
| Espacer une liste de liens sans marges manuelles | `gap` sur un `<ul>` en `display: flex` |
| Changer la couleur au survol/état actif | `:hover`, `.active` |
| Empiler la navbar sur mobile | `flex-direction: column` dans une `@media` query |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>
