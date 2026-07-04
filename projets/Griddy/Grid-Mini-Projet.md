# Mini-Projet — Tableau de bord (Dashboard) avec CSS Grid

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:6d28d9,100:8b5cf6&amp;height=150&amp;section=header&amp;text=Mini-Projet%20%3A%20Dashboard&amp;fontSize=34&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=40"/>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&amp;logo=css3&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Type-Mini--Projet-6d28d9?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Dur%C3%A9e-2%20%C3%A0%203h-blue?style=for-the-badge"/>

</div>

> 📘 Prérequis : avoir terminé le cours **[Grid.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/CSS/Grid/Grid.md)** et les **[exercices](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/exercices/Grid-Master/Hint.md)**.

<br/>

## 🎯 Contexte

> LingoLab Academy a besoin d'un **tableau de bord administrateur** pour visualiser en un coup d'œil : le nombre d'étudiants inscrits, les revenus du mois, les formations actives, et les dernières inscriptions. Votre mission : construire cette interface **entièrement avec CSS Grid**, sans utiliser une seule `<table>` HTML pour la mise en page.

<br/>

## 🗺️ Le plan attendu

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDgwIiBoZWlnaHQ9IjM2MCIgdmlld0JveD0iMCAwIDQ4MCAzNjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iMTAiIHk9IjEwIiB3aWR0aD0iNDYwIiBoZWlnaHQ9IjM0MCIgZmlsbD0iI2ZhZmFmYSIgc3Ryb2tlPSIjMzMzIiBzdHJva2Utd2lkdGg9IjIiLz4KCiAgPHJlY3QgeD0iMjAiIHk9IjIwIiB3aWR0aD0iOTAiIGhlaWdodD0iMzIwIiBmaWxsPSIjNmQyOGQ5IiByeD0iNiIvPgogIDx0ZXh0IHg9IjY1IiB5PSIxODAiIGZvbnQtZmFtaWx5PSJtb25vc3BhY2UiIGZvbnQtc2l6ZT0iMTIiIGZpbGw9IndoaXRlIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiB0cmFuc2Zvcm09InJvdGF0ZSgtOTAgNjUgMTgwKSI+c2lkZWJhciAobG9nbyArIG1lbnUpPC90ZXh0PgoKICA8cmVjdCB4PSIxMjAiIHk9IjIwIiB3aWR0aD0iMzQwIiBoZWlnaHQ9IjQ1IiBmaWxsPSIjOGI1Y2Y2IiByeD0iNiI+CiAgICA8YW5pbWF0ZSBhdHRyaWJ1dGVOYW1lPSJvcGFjaXR5IiB2YWx1ZXM9IjE7MC42OzEiIGR1cj0iMi41cyIgcmVwZWF0Q291bnQ9ImluZGVmaW5pdGUiLz4KICA8L3JlY3Q+CiAgPHRleHQgeD0iMjkwIiB5PSI0NyIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMiIgZmlsbD0id2hpdGUiIHRleHQtYW5jaG9yPSJtaWRkbGUiPnRvcGJhciAodGl0cmUgKyBwcm9maWwpPC90ZXh0PgoKICA8cmVjdCB4PSIxMjAiIHk9Ijc1IiB3aWR0aD0iNzgiIGhlaWdodD0iNzAiIGZpbGw9IiNhNzhiZmEiIHJ4PSI2Ii8+CiAgPHRleHQgeD0iMTU5IiB5PSIxMTUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMCIgZmlsbD0id2hpdGUiIHRleHQtYW5jaG9yPSJtaWRkbGUiPsOJdHVkaWFudHM8L3RleHQ+CiAgPHJlY3QgeD0iMjA2IiB5PSI3NSIgd2lkdGg9Ijc4IiBoZWlnaHQ9IjcwIiBmaWxsPSIjYTc4YmZhIiByeD0iNiIvPgogIDx0ZXh0IHg9IjI0NSIgeT0iMTE1IiBmb250LWZhbWlseT0iQXJpYWwiIGZvbnQtc2l6ZT0iMTAiIGZpbGw9IndoaXRlIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5SZXZlbnVzPC90ZXh0PgogIDxyZWN0IHg9IjI5MiIgeT0iNzUiIHdpZHRoPSI3OCIgaGVpZ2h0PSI3MCIgZmlsbD0iI2E3OGJmYSIgcng9IjYiLz4KICA8dGV4dCB4PSIzMzEiIHk9IjExNSIgZm9udC1mYW1pbHk9IkFyaWFsIiBmb250LXNpemU9IjEwIiBmaWxsPSJ3aGl0ZSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+Rm9ybWF0aW9uczwvdGV4dD4KICA8cmVjdCB4PSIzNzgiIHk9Ijc1IiB3aWR0aD0iODIiIGhlaWdodD0iNzAiIGZpbGw9IiNhNzhiZmEiIHJ4PSI2Ii8+CiAgPHRleHQgeD0iNDE5IiB5PSIxMTUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMCIgZmlsbD0id2hpdGUiIHRleHQtYW5jaG9yPSJtaWRkbGUiPlRhdXg8L3RleHQ+CgogIDxyZWN0IHg9IjEyMCIgeT0iMTU1IiB3aWR0aD0iMjAwIiBoZWlnaHQ9IjE4NSIgZmlsbD0iI2VkZTlmZSIgcng9IjYiIHN0cm9rZT0iI2M0YjVmZCIgc3Ryb2tlLXdpZHRoPSIyIi8+CiAgPHRleHQgeD0iMjIwIiB5PSIxODAiIGZvbnQtZmFtaWx5PSJtb25vc3BhY2UiIGZvbnQtc2l6ZT0iMTIiIGZpbGw9IiM0YzFkOTUiIHRleHQtYW5jaG9yPSJtaWRkbGUiPmdyYXBoaXF1ZSAvIGFjdGl2aXTDqTwvdGV4dD4KCiAgPHJlY3QgeD0iMzMwIiB5PSIxNTUiIHdpZHRoPSIxMzAiIGhlaWdodD0iMTg1IiBmaWxsPSIjZWRlOWZlIiByeD0iNiIgc3Ryb2tlPSIjYzRiNWZkIiBzdHJva2Utd2lkdGg9IjIiLz4KICA8dGV4dCB4PSIzOTUiIHk9IjE3NSIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMSIgZmlsbD0iIzRjMWQ5NSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+ZGVybmnDqHJlczwvdGV4dD4KICA8dGV4dCB4PSIzOTUiIHk9IjE5MCIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMSIgZmlsbD0iIzRjMWQ5NSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+aW5zY3JpcHRpb25zPC90ZXh0Pgo8L3N2Zz4=" width="480"/>
</div>

<br/>

## 📋 Cahier des charges

### 1. Structure générale (`grid-template-areas`)

| Zone | Contenu attendu |
|---|---|
| `sidebar` | Logo LingoLab + menu vertical (Accueil, Étudiants, Formations, Paramètres) |
| `topbar` | Titre de la page + zone profil (nom + avatar) |
| `stats` | 4 cartes statistiques côte à côte (Étudiants, Revenus, Formations actives, Taux de complétion) |
| `activite` | Une grande carte (graphique factice ou liste d'activité récente) |
| `inscriptions` | Une carte listant les 5 dernières inscriptions (nom + date) |

### 2. Contraintes techniques obligatoires

- [ ] Utiliser `display: grid` sur le conteneur principal avec `grid-template-areas`
- [ ] Utiliser `repeat(4, 1fr)` (ou équivalent) pour les 4 cartes statistiques
- [ ] Utiliser `grid-column: span 2` (ou équivalent) pour que la carte "activité" soit plus large que la carte "inscriptions"
- [ ] La `sidebar` doit avoir une largeur fixe, le reste doit s'adapter avec `1fr`
- [ ] Ajouter **au moins une** `@media` query pour empiler la mise en page sur mobile (sidebar en haut, une seule colonne)
- [ ] Aucune balise `<table>` utilisée pour la mise en page globale

### 3. Contenu minimum

- 4 cartes statistiques avec un chiffre + un libellé (ex : "1 240 — Étudiants inscrits")
- Une carte "activité" avec au moins 3 lignes de contenu factice
- Une liste d'au moins 5 inscriptions récentes (nom + date, utilisez `<time datetime="...">`)

<br/>

## 🧱 Squelette de départ (optionnel, pour démarrer plus vite)

```html
<div class="dashboard">
  <aside class="sidebar">Sidebar</aside>
  <header class="topbar">Topbar</header>

  <section class="stats">
    <div class="carte-stat">1 240<br><span>Étudiants</span></div>
    <div class="carte-stat">85 000 DA<br><span>Revenus</span></div>
    <div class="carte-stat">6<br><span>Formations</span></div>
    <div class="carte-stat">78%<br><span>Taux</span></div>
  </section>

  <section class="activite">Activité récente...</section>
  <section class="inscriptions">Dernières inscriptions...</section>
</div>
```

```css
.dashboard {
  display: grid;
  grid-template-columns: 220px 1fr;
  grid-template-rows: auto auto 1fr;
  grid-template-areas:
    "sidebar topbar"
    "sidebar stats"
    "sidebar main";
  min-height: 100vh;
  gap: 16px;
}

.sidebar { grid-area: sidebar; }
.topbar  { grid-area: topbar; }
.stats   {
  grid-area: stats;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
}
/* À vous de continuer : intégrez .activite et .inscriptions
   dans une zone "main" avec grid-template-areas + grid-column: span */
```

<br/>

## 📤 Livrables

1. Un fichier `index.html` + un fichier `style.css` (ou un seul fichier HTML avec `<style>`).
2. Le dashboard doit s'afficher correctement sur un écran large (desktop) **et** sur un écran étroit (mobile, via votre media query).
3. Un court paragraphe (5-6 lignes) expliquant vos choix de `grid-template-areas` et pourquoi vous avez choisi cette organisation.

<br/>

## 📊 Grille d'évaluation

| Critère | Points |
|---|---|
| Structure générale correcte avec `grid-template-areas` | 5 |
| 4 cartes statistiques alignées avec `repeat(4, 1fr)` | 3 |
| Carte "activité" plus large via `grid-column: span` | 3 |
| Responsive mobile fonctionnel (`@media`) | 4 |
| Contenu minimum présent (stats, activité, inscriptions) | 3 |
| Explication écrite des choix de mise en page | 2 |
| **Total** | **20** |

<br/>

## 💡 Idées d'amélioration (facultatif, non noté)

- Ajouter un effet `:hover` sur les cartes statistiques
- Utiliser `auto-fit`/`minmax()` pour que les cartes statistiques se réorganisent automatiquement au lieu de rester figées à 4 colonnes
- Ajouter une vraie mini-visualisation de données avec des `<div>` en barres (mini bar chart en pur CSS)

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>