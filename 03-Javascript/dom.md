<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:f97316,100:ef4444&height=200&section=header&text=JavaScript%20-%20DOM%20%26%20%C3%89v%C3%A9nements&fontSize=38&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Manipuler%20le%20HTML%20avec%20JavaScript&descAlignY=55&descSize=18" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-f97316?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Module-03%2F03-ef4444?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Statut-Actif-brightgreen?style=for-the-badge" />
</p>

## 🎯 Objectifs du cours

À la fin de ce module, l'étudiant sera capable de :
- Comprendre ce qu'est le DOM (Document Object Model)
- Sélectionner des éléments HTML avec JavaScript
- Modifier le contenu, le style et les attributs d'un élément
- Réagir aux actions de l'utilisateur (clic, saisie, survol) avec des événements

---

## 🧩 1. Qu'est-ce que le DOM ?

Le **DOM** est la représentation de la page HTML sous forme d'un arbre d'éléments que JavaScript peut lire et modifier.

```
document
 └── html
      ├── head
      └── body
           ├── h1
           ├── p
           └── button
```

```js
console.log(document.title); // affiche le titre de la page
```

---

## 🧩 2. Sélectionner un élément

```html
<h1 id="titre">Bienvenue à LingoLab</h1>
<p class="description">Apprends le web pas à pas.</p>
<button class="btn">Cliquez ici</button>
```

```js
// Par id → un seul élément
let titre = document.getElementById("titre");

// Par sélecteur CSS → le premier élément trouvé
let description = document.querySelector(".description");

// Par sélecteur CSS → tous les éléments trouvés
let boutons = document.querySelectorAll(".btn");
```

| Méthode                     | Retourne                          |
|------------------------------|------------------------------------|
| `getElementById("id")`       | Un seul élément                    |
| `querySelector(".classe")`   | Le premier élément correspondant   |
| `querySelectorAll(".classe")`| Une liste de tous les éléments     |

---

## 🧩 3. Modifier un élément

```js
let titre = document.getElementById("titre");

titre.textContent = "Nouveau titre !";       // change le texte
titre.style.color = "blue";                   // change le style CSS
titre.classList.add("actif");                 // ajoute une classe
titre.classList.remove("actif");              // retire une classe
titre.setAttribute("data-niveau", "debutant"); // ajoute un attribut
```

---

## 🧩 4. Les événements

Un événement est une action déclenchée par l'utilisateur (clic, survol, saisie clavier...).

```js
let bouton = document.querySelector(".btn");

bouton.addEventListener("click", function () {
  console.log("Le bouton a été cliqué !");
});
```

### Exemple concret — compteur de clics

```html
<button id="compteurBtn">Cliquez</button>
<p id="resultat">0 clics</p>
```

```js
let compteur = 0;
let bouton = document.getElementById("compteurBtn");
let resultat = document.getElementById("resultat");

bouton.addEventListener("click", function () {
  compteur++;
  resultat.textContent = compteur + " clics";
});
```

### Événements courants

| Événement    | Déclenché quand...                       |
|--------------|--------------------------------------------|
| `click`      | l'utilisateur clique sur l'élément          |
| `mouseover`  | la souris survole l'élément                 |
| `keydown`    | une touche du clavier est enfoncée          |
| `submit`     | un formulaire est envoyé                    |
| `input`      | le contenu d'un champ change                |

---

## 🧪 Exercices

### Exercice 1 — Sélection et modification (facile)

On donne le HTML suivant. Complète le JavaScript pour changer le texte et la couleur du titre.

```html
<h1 id="titrePrincipal">Titre par défaut</h1>
```

```js
// TODO : sélectionne l'élément avec l'id "titrePrincipal"
let titre = ___;

// TODO : change son texte en "Bienvenue au cours JavaScript"
titre.___ = "Bienvenue au cours JavaScript";

// TODO : change sa couleur en "green"
titre.style.___ = "green";
```

### Exercice 2 — Événement clic (facile)

Complète le code pour afficher un message dans la console à chaque clic sur le bouton.

```html
<button id="monBouton">Clique-moi</button>
```

```js
let bouton = document.getElementById("monBouton");

bouton.addEventListener(___, function () {
  console.log(___);
});
```

### Exercice 3 — Compteur interactif (intermédiaire)

Construis un compteur qui **augmente** avec un bouton `+` et **diminue** avec un bouton `-`, sans jamais descendre en dessous de 0.

```html
<button id="moins">-</button>
<span id="valeur">0</span>
<button id="plus">+</button>
```

```js
let valeur = 0;
let affichage = document.getElementById("valeur");

document.getElementById("plus").addEventListener("click", function () {
  // TODO : incrémente "valeur" et mets à jour l'affichage
});

document.getElementById("moins").addEventListener("click", function () {
  // TODO : décrémente "valeur" (sans descendre sous 0) et mets à jour l'affichage
});
```

### Exercice 4 — Formulaire simple (avancé)

On donne un champ de saisie et un bouton. Quand l'utilisateur clique sur "Valider", le message de bienvenue doit s'afficher avec le prénom saisi — mais seulement si le champ n'est pas vide.

```html
<input type="text" id="champPrenom" placeholder="Entrez votre prénom" />
<button id="validerBtn">Valider</button>
<p id="message"></p>
```

```js
let bouton = document.getElementById("validerBtn");
let champ = document.getElementById("champPrenom");
let message = document.getElementById("message");

bouton.addEventListener("click", function () {
  let prenom = champ.___;   // TODO : récupère la valeur saisie (indice : propriété "value")

  if (prenom ___ "") {       // TODO : vérifie que le champ n'est pas vide
    message.textContent = "Bienvenue " + prenom + " 👋";
  } else {
    message.textContent = "Merci de saisir un prénom";
  }
});
```

> 📁 Les corrigés de ces exercices seront disponibles dans le dossier `corrections/03-Javascript/`.

---

<p align="center">
  <img src="https://img.shields.io/badge/LingoLab-Academy-f97316?style=for-the-badge" />
  <img src="https://img.shields.io/badge/DevLab-Solutions-ef4444?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:ef4444,100:f97316&height=120&section=footer" width="100%"/>
</p>