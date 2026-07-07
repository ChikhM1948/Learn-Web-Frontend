<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:1e293b,100:38bdf8&amp;height=180&amp;section=header&amp;text=Barres%20de%20Navigation%20%F0%9F%A7%AD&amp;fontSize=36&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=35&amp;desc=Construire%20des%20navbars%20modernes&amp;descAlignY=55&amp;descSize=15"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&amp;size=20&amp;pause=1000&amp;color=38BDF8&amp;center=true&amp;vCenter=true&amp;width=650&amp;lines=nav+%E2%80%A2+ul+%E2%80%A2+li+%E2%80%A2+a;sticky+%E2%80%A2+dropdown+%E2%80%A2+responsive" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&amp;logo=css3&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-Interm%C3%A9diaire-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Cours-Navbar-1e293b?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif du cours

> Ce cours couvre les **techniques générales** pour construire des barres de navigation : structure HTML sémantique, mise en page avec Flexbox, barre qui reste visible au défilement (`sticky`), et menu déroulant. Pour une navbar déjà codée et décortiquée en détail, voir aussi **[projets/Simple-Navbar/Navbar.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/projets/Simple-Navbar/Navbar.md)**.

<br/>

## 1️⃣ La structure HTML de base

```html
<nav class="navbar">
  <div class="logo">LingoLab</div>
  <ul class="nav-links">
    <li><a href="#">Accueil</a></li>
    <li><a href="#">Formations</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

> 🧠 Toujours utiliser la balise sémantique `<nav>` (voir le guide `Semantic-Tags.md`) pour le menu principal — jamais une simple `<div>`.

<br/>

## 2️⃣ La mise en page — Flexbox

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px 32px;
  background: #1e293b;
}

.nav-links {
  display: flex;
  gap: 24px;
  list-style: none;
}
```

> Voir le guide **[Flexbox.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/CSS/Flex-Box/Flexbox.md)** pour le détail complet de `justify-content: space-between`.

<br/>

## 3️⃣ Navbar collante (`position: sticky`)

```css
.navbar {
  position: sticky;
  top: 0;
  z-index: 100;
}
```

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDIwIiBoZWlnaHQ9IjIyMCIgdmlld0JveD0iMCAwIDQyMCAyMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iMTAiIHk9IjEwIiB3aWR0aD0iNDAwIiBoZWlnaHQ9IjIwMCIgZmlsbD0iI2Y0ZjRmNCIgc3Ryb2tlPSIjOTk5IiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1kYXNoYXJyYXk9IjQsMyIvPgogIDxyZWN0IHg9IjEwIiB5PSIxMCIgd2lkdGg9IjQwMCIgaGVpZ2h0PSIzNSIgZmlsbD0iIzFlMjkzYiI+CiAgICA8YW5pbWF0ZSBhdHRyaWJ1dGVOYW1lPSJvcGFjaXR5IiB2YWx1ZXM9IjE7MC43OzEiIGR1cj0iMi41cyIgcmVwZWF0Q291bnQ9ImluZGVmaW5pdGUiLz4KICA8L3JlY3Q+CiAgPHRleHQgeD0iMjEwIiB5PSIzMiIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMiIgZmlsbD0id2hpdGUiIHRleHQtYW5jaG9yPSJtaWRkbGUiPm5hdiAocG9zaXRpb246IHN0aWNreTsgdG9wOiAwOyk8L3RleHQ+CiAgPHJlY3QgeD0iMzAiIHk9IjYwIiB3aWR0aD0iMzYwIiBoZWlnaHQ9IjE0IiBmaWxsPSIjZTVlN2ViIi8+CiAgPHJlY3QgeD0iMzAiIHk9Ijg1IiB3aWR0aD0iMzYwIiBoZWlnaHQ9IjE0IiBmaWxsPSIjZTVlN2ViIi8+CiAgPHJlY3QgeD0iMzAiIHk9IjExMCIgd2lkdGg9IjM2MCIgaGVpZ2h0PSIxNCIgZmlsbD0iI2U1ZTdlYiIvPgogIDxyZWN0IHg9IjMwIiB5PSIxMzUiIHdpZHRoPSIzNjAiIGhlaWdodD0iMTQiIGZpbGw9IiNlNWU3ZWIiLz4KICA8cmVjdCB4PSIzMCIgeT0iMTYwIiB3aWR0aD0iMzYwIiBoZWlnaHQ9IjE0IiBmaWxsPSIjZTVlN2ViIi8+CiAgPHRleHQgeD0iMjEwIiB5PSIyMDAiIGZvbnQtZmFtaWx5PSJtb25vc3BhY2UiIGZvbnQtc2l6ZT0iMTEiIGZpbGw9IiM1NTUiIHRleHQtYW5jaG9yPSJtaWRkbGUiPmxhIG5hdiByZXN0ZSBjb2xsw6llIGVuIGhhdXQgcGVuZGFudCBsZSBkw6lmaWxlbWVudDwvdGV4dD4KPC9zdmc+" width="480"/>
</div>

> 🧠 `position: sticky` (voir le guide `Position.md`) fait rester la navbar visible en haut de l'écran pendant que le reste de la page défile — le comportement attendu sur la quasi-totalité des sites modernes. Le `z-index` évite que du contenu passe devant la barre.

<br/>

## 4️⃣ Menu déroulant (dropdown) en CSS pur

```html
<li class="dropdown">
  <a href="#">Services ▾</a>
  <ul class="dropdown-menu">
    <li><a href="#">Formation A</a></li>
    <li><a href="#">Formation B</a></li>
  </ul>
</li>
```

```css
.dropdown-menu {
  display: none;
  position: absolute;
  background: white;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

.dropdown:hover .dropdown-menu {
  display: block;
}
```

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzgwIiBoZWlnaHQ9IjE4MCIgdmlld0JveD0iMCAwIDM4MCAxODAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iMjAiIHk9IjIwIiB3aWR0aD0iMzQwIiBoZWlnaHQ9IjQwIiBmaWxsPSIjMWUyOTNiIiByeD0iNCIvPgogIDx0ZXh0IHg9IjgwIiB5PSI0NSIgZm9udC1mYW1pbHk9IkFyaWFsIiBmb250LXNpemU9IjEyIiBmaWxsPSJ3aGl0ZSI+QWNjdWVpbDwvdGV4dD4KICA8dGV4dCB4PSIxODAiIHk9IjQ1IiBmb250LWZhbWlseT0iQXJpYWwiIGZvbnQtc2l6ZT0iMTIiIGZpbGw9IiMzOGJkZjgiIGZvbnQtd2VpZ2h0PSJib2xkIj5TZXJ2aWNlcyDilr48L3RleHQ+CiAgPHRleHQgeD0iMzAwIiB5PSI0NSIgZm9udC1mYW1pbHk9IkFyaWFsIiBmb250LXNpemU9IjEyIiBmaWxsPSJ3aGl0ZSI+Q29udGFjdDwvdGV4dD4KICA8cmVjdCB4PSIxNTAiIHk9IjYwIiB3aWR0aD0iMTIwIiBoZWlnaHQ9IjgwIiBmaWxsPSJ3aGl0ZSIgc3Ryb2tlPSIjY2NjIiBzdHJva2Utd2lkdGg9IjIiIHJ4PSI0Ij4KICAgIDxhbmltYXRlIGF0dHJpYnV0ZU5hbWU9Im9wYWNpdHkiIHZhbHVlcz0iMDsxOzEiIGR1cj0iMnMiIHJlcGVhdENvdW50PSJpbmRlZmluaXRlIi8+CiAgPC9yZWN0PgogIDx0ZXh0IHg9IjE2MCIgeT0iODAiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMCIgZmlsbD0iIzMzMyI+Rm9ybWF0aW9uIEE8L3RleHQ+CiAgPHRleHQgeD0iMTYwIiB5PSIxMDAiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMCIgZmlsbD0iIzMzMyI+Rm9ybWF0aW9uIEI8L3RleHQ+CiAgPHRleHQgeD0iMTYwIiB5PSIxMjAiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMCIgZmlsbD0iIzMzMyI+Rm9ybWF0aW9uIEM8L3RleHQ+Cjwvc3ZnPg==" width="480"/>
</div>

> 🧠 **Le combo clé** : `.dropdown-menu` est caché par défaut (`display: none`) et positionné en `absolute` par rapport à son parent `.dropdown` (qui doit donc être en `position: relative`). Le sélecteur `.dropdown:hover .dropdown-menu` affiche le sous-menu **uniquement pendant le survol du parent** — aucune ligne de JavaScript nécessaire pour cette version simple.

<br/>

## 5️⃣ Responsive — menu hamburger (structure de base)

```css
.menu-toggle {
  display: none; /* caché sur desktop */
}

@media (max-width: 700px) {
  .nav-links {
    display: none; /* caché par défaut sur mobile */
    flex-direction: column;
    width: 100%;
  }

  .menu-toggle {
    display: block; /* le bouton ☰ apparaît sur mobile */
  }

  .nav-links.ouvert {
    display: flex; /* affiché quand la classe "ouvert" est ajoutée (via JS) */
  }
}
```

> 💡 La bascule d'affichage (`display: none` ↔ `flex`) via une classe `.ouvert` nécessite une petite ligne de JavaScript (`element.classList.toggle('ouvert')`) — c'est la seule étape de ce cours qui sort du pur CSS.

<br/>

## 📌 Résumé express

| Je veux... | Technique |
|---|---|
| Structurer sémantiquement une navbar | `<nav>` + `<ul>`/`<li>`/`<a>` |
| Aligner logo et liens aux extrémités | `display: flex; justify-content: space-between;` |
| Garder la navbar visible au scroll | `position: sticky; top: 0;` |
| Créer un sous-menu au survol, sans JS | `.dropdown-menu { display: none; }` + `:hover` |
| Rendre la navbar responsive avec menu ☰ | `@media` + `display: none/flex` + une classe togglée en JS |

<br/>

## 🧪 Exercices

### Exercice 1 — Navbar de base

```css
.navbar {
  display: ____;              /* (1) */
  justify-content: ____;      /* (2) logo à gauche, liens à droite */
  align-items: center;
}
```

### Exercice 2 — Rendre la navbar collante

Reprenez votre navbar de l'exercice 1 et ajoutez les propriétés nécessaires pour qu'elle reste visible en haut de l'écran pendant que vous scrollez une longue page de contenu factice.

### Exercice 3 — Dropdown au survol

Construisez un menu "Formations" qui affiche, au survol, une liste de 3 formations en dessous, en CSS pur (sans JavaScript), en réutilisant la technique de la section 4.

### 📊 Grille d'évaluation

| Critère | Points |
|---|---|
| Exercice 1 complété | 4 |
| Exercice 2 — navbar sticky fonctionnelle | 6 |
| Exercice 3 — dropdown au survol fonctionnel | 10 |
| **Total** | **20** |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>
