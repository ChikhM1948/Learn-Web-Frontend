<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:22c55e,100:0ea5e9&height=200&section=header&text=JavaScript%20-%20Structures%20de%20Contr%C3%B4le&fontSize=38&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Conditions%20%E2%80%A2%20Boucles%20%E2%80%A2%20Fonctions&descAlignY=55&descSize=18" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-22c55e?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Module-02%2F03-0ea5e9?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Statut-Actif-brightgreen?style=for-the-badge" />
</p>

## 🎯 Objectifs du cours

À la fin de ce module, l'étudiant sera capable de :
- Écrire des conditions avec `if / else / else if` et `switch`
- Répéter des actions avec les boucles `for`, `while`, `for...of`
- Créer et utiliser des fonctions (classiques et fléchées)
- Comprendre la notion de paramètres, arguments et valeur de retour

---

## 🧩 1. Les conditions

### `if / else`

```js
let note = 12;

if (note >= 10) {
  console.log("Admis ✅");
} else {
  console.log("Non admis ❌");
}
```

### `else if` — plusieurs cas

```js
let note = 15;

if (note >= 16) {
  console.log("Très bien");
} else if (note >= 14) {
  console.log("Bien");
} else if (note >= 10) {
  console.log("Passable");
} else {
  console.log("Insuffisant");
}
```

### `switch` — pour une valeur avec plusieurs choix précis

```js
let jour = "Lundi";

switch (jour) {
  case "Samedi":
  case "Dimanche":
    console.log("Week-end 🎉");
    break;
  default:
    console.log("Jour de cours 📘");
}
```

> ⚠️ Ne pas oublier `break` sinon le code continue d'exécuter les cas suivants.

---

## 🧩 2. Les boucles

### `for` — quand on connaît le nombre de répétitions

```js
for (let i = 1; i <= 5; i++) {
  console.log("Séance n°" + i);
}
```

### `while` — tant qu'une condition est vraie

```js
let essais = 0;
while (essais < 3) {
  console.log("Essai n°" + (essais + 1));
  essais++;
}
```

### `for...of` — pour parcourir un tableau

```js
let etudiants = ["Sarah", "Yacine", "Nour"];

for (let nom of etudiants) {
  console.log("Bonjour " + nom);
}
```

| Boucle    | Utilisation typique                          |
|-----------|-----------------------------------------------|
| `for`     | Nombre d'itérations connu à l'avance          |
| `while`   | Répéter tant qu'une condition reste vraie      |
| `for...of`| Parcourir les éléments d'un tableau            |

---

## 🧩 3. Les fonctions

Une fonction regroupe un bloc de code réutilisable.

### Fonction classique

```js
function saluer(nom) {
  return "Bonjour " + nom + " !";
}

console.log(saluer("Amine")); // Bonjour Amine !
```

### Fonction fléchée (arrow function)

```js
const additionner = (a, b) => a + b;

console.log(additionner(4, 6)); // 10
```

### Paramètres avec valeur par défaut

```js
function calculerMoyenne(controle, examen = 10) {
  return (controle + examen * 2) / 3;
}

console.log(calculerMoyenne(14)); // examen prend 10 par défaut
console.log(calculerMoyenne(14, 16));
```

> 💡 Une fonction sans `return` renvoie `undefined` par défaut.

---

## 🧪 Exercices

### Exercice 1 — Conditions (facile)

Complète la fonction pour qu'elle affiche si un nombre est pair ou impair.

```js
function verifierParite(nombre) {
  if (___) {
    console.log(nombre + " est pair");
  } else {
    console.log(nombre + " est impair");
  }
}

verifierParite(7);
verifierParite(10);
```

### Exercice 2 — Boucle `for` (facile)

Affiche la table de multiplication de 7, de 1 à 10, en complétant la boucle.

```js
for (let i = ___; i <= ___; i++) {
  console.log("7 x " + i + " = " + (7 * i));
}
```

### Exercice 3 — Boucle + tableau (intermédiaire)

On donne un tableau de notes. Calcule et affiche la moyenne de la classe.

```js
let notes = [12, 8, 15, 17, 9, 14];
let somme = 0;

// TODO : parcours le tableau "notes" et additionne chaque valeur à "somme"
for (___) {
  somme += ___;
}

// TODO : calcule la moyenne (somme / nombre de notes)
let moyenneClasse = ___;

console.log("Moyenne de la classe :", moyenneClasse);
```

### Exercice 4 — Fonctions (intermédiaire)

Écris une fonction `estMajeur(age)` qui retourne `true` si l'âge est supérieur ou égal à 18, sinon `false`.

```js
function estMajeur(age) {
  // TODO : complète le corps de la fonction
}

console.log(estMajeur(16)); // false
console.log(estMajeur(20)); // true
```

### Exercice 5 — Mini-défi combiné (avancé)

Écris une fonction `classerEtudiants(notes)` qui prend un tableau de notes et retourne un objet contenant le nombre d'étudiants **admis** (note ≥ 10) et **non admis**.

```js
function classerEtudiants(notes) {
  let admis = 0;
  let nonAdmis = 0;

  // TODO : parcours le tableau "notes" avec une boucle
  // TODO : incrémente "admis" ou "nonAdmis" selon la note

  return { admis, nonAdmis };
}

let resultat = classerEtudiants([8, 12, 15, 6, 10, 17, 4]);
console.log(resultat); // attendu : { admis: 4, nonAdmis: 3 }
```

> 📁 Les corrigés de ces exercices seront disponibles dans le dossier `corrections/03-Javascript/`.

---

<p align="center">
  <img src="https://img.shields.io/badge/LingoLab-Academy-22c55e?style=for-the-badge" />
  <img src="https://img.shields.io/badge/DevLab-Solutions-0ea5e9?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0ea5e9,100:22c55e&height=120&section=footer" width="100%"/>
</p>