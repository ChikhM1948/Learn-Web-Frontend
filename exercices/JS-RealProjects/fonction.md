<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0ea5e9,100:22c55e&height=200&section=header&text=JavaScript%20-%20Fonctions%20en%20Situation%20R%C3%A9elle&fontSize=30&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Mini-projets%20pratiques%20avec%20des%20fonctions&descAlignY=55&descSize=18" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Niveau-D%C3%A9butant%20%2F%20Interm%C3%A9diaire-0ea5e9?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Module-02%2F03%20%E2%80%94%20Exercices-22c55e?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Type-Projet%20Concret-brightgreen?style=for-the-badge" />
</p>

## 🎯 Objectif

Écrire des **fonctions réutilisables** pour résoudre des besoins concrets : calcul de prix, validation de formulaire, génération de reçu, gestion de notes. Tu peux utiliser tout ce que tu connais (variables, conditions, boucles, fonctions classiques et fléchées).

> 💡 Rappel : une bonne fonction fait **une seule chose bien**, prend des paramètres clairs, et `return` un résultat plutôt que d'afficher directement avec `console.log` à l'intérieur.

---

## 🧪 Projet 1 — Calculateur de prix avec réduction (boutique en ligne)

**Contexte :** une boutique applique une réduction selon le montant total du panier.
- Moins de 5000 DA → pas de réduction
- Entre 5000 et 9999 DA → 5% de réduction
- 10000 DA ou plus → 10% de réduction

```js
function calculerPrixFinal(montant) {
  // TODO : retourne le montant final après réduction selon les règles ci-dessus
}

console.log(calculerPrixFinal(3000));  // → 3000
console.log(calculerPrixFinal(7000));  // → 6650
console.log(calculerPrixFinal(12000)); // → 10800
```

<details>
<summary>💡 Indice</summary>

Utilise `if / else if / else` à l'intérieur de la fonction, puis un seul `return` par branche.
</details>

---

## 🧪 Projet 2 — Validation de formulaire d'inscription (LingoLab Academy)

**Contexte :** avant d'enregistrer un nouvel étudiant, on doit valider ses informations.

```js
function validerInscription(nom, age, email) {
  // Règles à respecter :
  // 1. "nom" ne doit pas être vide
  // 2. "age" doit être un nombre entre 5 et 99
  // 3. "email" doit contenir le caractère "@"
  //
  // TODO : retourne "Inscription valide ✅" si tout est correct
  // TODO : sinon retourne un message précis expliquant l'erreur
}

console.log(validerInscription("", 20, "test@mail.com"));
// → "Le nom est obligatoire"

console.log(validerInscription("Yacine", 3, "yacine@mail.com"));
// → "L'âge doit être entre 5 et 99 ans"

console.log(validerInscription("Nour", 25, "nourmail.com"));
// → "L'email doit contenir un @"

console.log(validerInscription("Nour", 25, "nour@mail.com"));
// → "Inscription valide ✅"
```

> ⚠️ Attention à l'ordre des vérifications : la fonction doit s'arrêter (avec `return`) dès qu'une règle échoue, sans continuer à vérifier les suivantes.

---

## 🧪 Projet 3 — Générateur de reçu réutilisable

**Contexte :** transforme le calcul de facture du module précédent en une **fonction réutilisable**, appelable pour n'importe quel produit.

```js
function genererRecu(nomProduit, prixUnitaire, quantite, tauxTVA = 0.19) {
  // TODO : calcule sous-total, TVA, et total final
  // TODO : retourne une chaîne de texte formatée avec un template literal
}

console.log(genererRecu("Casque Bluetooth", 4500, 3));
console.log(genererRecu("Clavier mécanique", 6000, 1, 0.09)); // TVA réduite à 9%
```

**Résultat attendu (exemple) :**
```
--- Reçu ---
Produit : Casque Bluetooth
Quantité : 3
Sous-total : 13500 DA
TVA (19%) : 2565.00 DA
TOTAL : 16065.00 DA
------------
```

---

## 🧪 Projet 4 — Système de notation d'étudiants (fonctions combinées)

**Contexte :** LingoLab veut un mini-outil qui calcule la moyenne d'un étudiant et lui attribue une mention.

```js
// Fonction 1 : calcule la moyenne pondérée
function calculerMoyenne(controle, examen) {
  // TODO : (controle + examen * 2) / 3
}

// Fonction 2 : retourne la mention selon la moyenne
function obtenirMention(moyenne) {
  // TODO :
  // >= 16 → "Très bien"
  // >= 14 → "Bien"
  // >= 12 → "Assez bien"
  // >= 10 → "Passable"
  // < 10  → "Insuffisant"
}

// Fonction 3 : combine les deux pour générer un bulletin complet
function genererBulletin(nomEtudiant, controle, examen) {
  // TODO : utilise calculerMoyenne() et obtenirMention() ici
  // TODO : retourne "Nom : X, Moyenne : Y, Mention : Z"
}

console.log(genererBulletin("Sarah", 14, 16));
console.log(genererBulletin("Yacine", 8, 9));
```

> 💡 C'est le principe de la **composition de fonctions** : une fonction peut en appeler une autre. C'est comme ça qu'on construit du vrai code professionnel — de petites fonctions simples assemblées ensemble.

---

## 🚀 Défi bonus — Panier multi-produits

Utilise un tableau d'objets pour représenter un panier, et écris une fonction `calculerTotalPanier(panier)` qui additionne le prix de tous les produits (prix × quantité pour chacun).

```js
const panier = [
  { nom: "Casque Bluetooth", prix: 4500, quantite: 2 },
  { nom: "Souris sans fil", prix: 2000, quantite: 1 },
  { nom: "Tapis de souris", prix: 800, quantite: 3 },
];

function calculerTotalPanier(panier) {
  // TODO : utilise une boucle for...of pour additionner (prix * quantite) de chaque produit
}

console.log(calculerTotalPanier(panier)); // → attendu : 13400
```

> 📁 Les corrigés seront disponibles dans `corrections/03-Javascript/Fonctions-Projet-Reel/`.

---

<p align="center">
  <img src="https://img.shields.io/badge/LingoLab-Academy-0ea5e9?style=for-the-badge" />
  <img src="https://img.shields.io/badge/DevLab-Solutions-22c55e?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:22c55e,100:0ea5e9&height=120&section=footer" width="100%"/>
</p>