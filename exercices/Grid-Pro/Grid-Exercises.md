# Consigne — S'entraîner avec CSS Grid

<div align="center">

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&amp;logo=css3&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Type-Exercices-f59e0b?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Pr%C3%A9requis-Cours%20Grid-8b5cf6?style=for-the-badge"/>

</div>

> 📘 Avant de commencer, relis le cours : **[CSS/Grid/Grid.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/CSS/Grid/Grid.md)**

<br/>

## 🎯 Objectif

Compléter progressivement 3 exercices à trous pour maîtriser `display: grid`, les colonnes en `fr`, `repeat()`, `minmax()`/`auto-fit`, `grid-template-areas` et `grid-column: span`.

---

## 🧩 Exercice 1 — Galerie de photos (bases + `fr`)

### Ce qui est fourni — HTML (ne pas modifier)

```html
<div class="galerie">
  <div class="photo">1</div>
  <div class="photo">2</div>
  <div class="photo">3</div>
  <div class="photo">4</div>
  <div class="photo">5</div>
  <div class="photo">6</div>
</div>
```

### À vous de jouer — CSS à compléter

```css
.galerie {
  display: ____;                    /* (1) active la grille */
  grid-template-columns: ____ ____ ____; /* (2) 3 colonnes égales, en unité fr */
  gap: ____;                        /* (3) espace de 12px entre les photos */
}

.photo {
  background: #8b5cf6;
  color: white;
  height: 120px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 8px;
}
```

### Consignes

1. Complétez les **3 blancs**.
2. Vérifiez que les 6 photos forment **2 lignes de 3 colonnes égales**.
3. Question écrite (2-3 phrases) : que se passe-t-il si vous ajoutez une 7ème `.photo` ? Pourquoi ?

### Bonus

- Remplacez `grid-template-columns: 1fr 1fr 1fr` par `repeat(3, 1fr)` — vérifiez que le rendu est identique.

---

## 🧩 Exercice 2 — Grille responsive automatique (`minmax` + `auto-fit`)

### Ce qui est fourni — HTML (ne pas modifier)

```html
<div class="cartes">
  <div class="carte">Carte A</div>
  <div class="carte">Carte B</div>
  <div class="carte">Carte C</div>
  <div class="carte">Carte D</div>
  <div class="carte">Carte E</div>
</div>
```

### À vous de jouer — CSS à compléter

```css
.cartes {
  display: grid;
  grid-template-columns: repeat(____, minmax(____, 1fr)); /* (1) et (2) */
  gap: 16px;
}

.carte {
  background: #f4f4f4;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 20px;
  text-align: center;
}
```

### Consignes

1. Remplacez le blanc (1) par la valeur qui permet à la grille de **s'adapter automatiquement** au nombre de colonnes possible.
2. Remplacez le blanc (2) par une largeur minimale de **200px** pour chaque carte.
3. Réduisez la largeur de votre navigateur (ou de l'aperçu) → comptez combien de colonnes s'affichent à différentes largeurs d'écran.
4. Question écrite : quelle est la différence entre `auto-fit` et `auto-fill` ? (Aidez-vous du cours.)

### Bonus

- Remplacez `auto-fit` par `auto-fill` et ajoutez une bordure en pointillé au conteneur `.cartes` pour observer les colonnes vides invisibles.

---

## 🧩 Exercice 3 — Mise en page nommée (`grid-template-areas`)

### Ce qui est fourni — HTML (ne pas modifier)

```html
<div class="page">
  <header class="entete">En-tête</header>
  <nav class="menu">Menu</nav>
  <main class="contenu">Contenu principal</main>
  <aside class="annexe">Annexe</aside>
  <footer class="pied">Pied de page</footer>
</div>
```

### À vous de jouer — CSS à compléter

```css
.page {
  display: grid;
  grid-template-columns: 180px 1fr 180px;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "____   entete  ____"     /* (1) même nom des deux côtés de "entete" */
    "menu   ____    annexe"   /* (2) nom de la zone centrale */
    "menu   pied    annexe";
  gap: 10px;
  min-height: 100vh;
}

.entete  { grid-area: entete; background: #8b5cf6; color: white; }
.menu    { grid-area: ____; background: #a78bfa; color: white; }   /* (3) */
.contenu { grid-area: contenu; background: #ede9fe; }
.annexe  { grid-area: ____; background: #a78bfa; color: white; }   /* (4) */
.pied    { grid-area: pied; background: #6d28d9; color: white; }
```

### Consignes

1. Complétez les **4 blancs** pour que le schéma `grid-template-areas` corresponde exactement aux classes utilisées dans le HTML.
2. Vérifiez que l'en-tête s'étend sur toute la largeur, le menu et l'annexe encadrent le contenu, et le pied de page s'étend aussi sur toute la largeur.
3. Question écrite : pourquoi le mot `entete` doit-il apparaître **deux fois** sur la même ligne du schéma `grid-template-areas` ?

### Bonus

- Ajoutez une media query `@media (max-width: 700px)` qui empile les 5 zones en une seule colonne (indice : redéfinissez `grid-template-columns` et `grid-template-areas` à l'intérieur).

---

## 📊 Grille d'évaluation globale

| Critère | Points |
|---|---|
| Exercice 1 complété correctement (3 blancs) | 5 |
| Exercice 2 complété correctement (2 blancs) | 5 |
| Exercice 3 complété correctement (4 blancs) | 6 |
| Réponses écrites aux 3 questions | 3 |
| Au moins un bonus réalisé | 1 |
| **Total** | **20** |

<br/>

## ➡️ Et après ?

Une fois les 3 exercices terminés, passez au **[mini-projet Dashboard](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/projets/Grid-Dashboard/Consigne.md)** pour construire une vraie mise en page complète avec CSS Grid.

<br/>

*LingoLab Academy © 2026 dr Chikh Amine*
