<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:38bdf8,100:6366f1&height=200&section=header&text=JavaScript%20-%20Les%20Bases&fontSize=45&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Variables%20%E2%80%A2%20Types%20%E2%80%A2%20Op%C3%A9rateurs%20%E2%80%A2%20Console&descAlignY=55&descSize=18" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-38bdf8?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Module-01%2F03-6366f1?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Statut-Actif-brightgreen?style=for-the-badge" />
</p>

## 🎯 Objectifs du cours

À la fin de ce module, l'étudiant sera capable de :
- Comprendre le rôle de JavaScript dans une page web
- Déclarer et utiliser des variables (`let`, `const`, `var`)
- Identifier les types de données de base
- Utiliser les opérateurs arithmétiques, de comparaison et logiques
- Afficher des résultats dans la console du navigateur

---

## 🧩 1. Qu'est-ce que JavaScript ?

JavaScript est le langage de **programmation** qui rend une page web **interactive**. Si HTML construit le squelette et CSS l'habille, **JavaScript donne vie** à la page : clics, animations, calculs, validations de formulaires, etc.

```html
<!-- On lie un fichier JS à une page HTML -->
<script src="script.js"></script>
```

> 💡 On peut aussi écrire du JS directement dans la console du navigateur (F12 → onglet *Console*) pour tester rapidement du code.

---

## 🧩 2. Les variables

Une variable est une **boîte nommée** qui contient une valeur.

```js
let prenom = "Amine";     // peut changer plus tard
const anneeNaissance = 1995; // ne change jamais
var ville = "Relizane";   // ancienne syntaxe, à éviter
```

| Mot-clé | Modifiable ? | Portée      | Recommandation           |
|---------|--------------|-------------|---------------------------|
| `let`   | ✅ Oui       | Bloc `{ }`  | Utiliser par défaut        |
| `const` | ❌ Non       | Bloc `{ }`  | Utiliser si la valeur fixe |
| `var`   | ✅ Oui       | Fonction    | ⚠️ À éviter (legacy)        |

### Règles de nommage

```js
let nomEtudiant = "Sarah";  // camelCase ✅
let 2eme_note = 15;          // ❌ interdit (commence par un chiffre)
let const = 5;               // ❌ interdit (mot réservé)
```

---

## 🧩 3. Les types de données

```js
let age = 22;                 // number
let nom = "Chikh";            // string
let estEtudiant = true;       // boolean
let notes = [12, 15, 18];     // array (tableau)
let profil = { nom: "Amine", age: 22 }; // object
let rien = null;              // null (vide intentionnellement)
let inconnu;                  // undefined (pas encore défini)
```

Pour vérifier le type d'une valeur, on utilise `typeof` :

```js
console.log(typeof age);        // "number"
console.log(typeof nom);        // "string"
console.log(typeof estEtudiant);// "boolean"
```

---

## 🧩 4. Les opérateurs

### Arithmétiques

```js
let a = 10, b = 3;
console.log(a + b); // 13  addition
console.log(a - b); // 7   soustraction
console.log(a * b); // 30  multiplication
console.log(a / b); // 3.33 division
console.log(a % b); // 1   reste (modulo)
console.log(a ** b);// 1000 puissance
```

### Comparaison

```js
console.log(5 == "5");   // true  (compare la valeur seulement)
console.log(5 === "5");  // false (compare valeur ET type) ✅ recommandé
console.log(5 !== "5");  // true
console.log(5 > 3);      // true
```

### Logiques

```js
let majeur = true, algerien = true;
console.log(majeur && algerien); // ET → true si les deux sont vrais
console.log(majeur || algerien); // OU → true si au moins un est vrai
console.log(!majeur);            // NON → inverse la valeur
```

---

## 🧩 5. Afficher dans la console

```js
console.log("Bonjour LingoLab !");
console.log("Résultat :", 5 + 3);
console.error("Ceci est une erreur");
console.warn("Ceci est un avertissement");
```

> 🔎 Ouvre la console de ton navigateur (clic droit → *Inspecter* → *Console*) pour voir ces messages en direct.

---

## 🧪 Exercices

### Exercice 1 — Déclaration (facile)

Complète le code pour déclarer les variables suivantes puis affiche-les dans la console.

```js
// TODO : déclare une variable "prenom" (string) avec ton prénom
___ prenom = ___;

// TODO : déclare une constante "anneeCours" avec la valeur 2026
___ anneeCours = ___;

// TODO : affiche les deux variables dans la console
console.log(___);
```

### Exercice 2 — Types de données (facile)

Pour chaque variable, écris en commentaire son type (`number`, `string`, `boolean`, `array`, `object`) sans utiliser `typeof` — puis vérifie ta réponse avec `typeof`.

```js
let x1 = 42;              // type : ___
let x2 = "LingoLab";       // type : ___
let x3 = false;            // type : ___
let x4 = [1, 2, 3];         // type : ___
let x5 = { ville: "Oran" }; // type : ___

// Vérifie tes réponses :
console.log(typeof x1, typeof x2, typeof x3, typeof x4, typeof x5);
```

### Exercice 3 — Opérateurs (intermédiaire)

Un étudiant a obtenu **14** en contrôle continu et **16** à l'examen. La moyenne finale se calcule ainsi : `(controle + examen * 2) / 3`.

```js
let controle = 14;
let examen = 16;

// TODO : calcule la moyenne avec la formule ci-dessus
let moyenne = ___;

// TODO : affiche "Moyenne : X" dans la console
console.log(___);

// TODO : vérifie si la moyenne est supérieure ou égale à 10 (admis)
let admis = ___;
console.log("Admis :", admis);
```

### Exercice 4 — Mini-défi (avancé)

Sans regarder la correction, prédis ce qu'affiche ce code, puis exécute-le pour vérifier :

```js
let a = "5";
let b = 5;

console.log(a == b);   // ta prédiction : ___
console.log(a === b);  // ta prédiction : ___
console.log(a + b);    // ta prédiction : ___ (attention au piège !)
console.log(Number(a) + b); // ta prédiction : ___
```

> 📁 Les corrigés de ces exercices seront disponibles dans le dossier `corrections/03-Javascript/`.

---

<p align="center">
  <img src="https://img.shields.io/badge/LingoLab-Academy-38bdf8?style=for-the-badge" />
  <img src="https://img.shields.io/badge/DevLab-Solutions-6366f1?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:6366f1,100:38bdf8&height=120&section=footer" width="100%"/>
</p><p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:38bdf8,100:6366f1&height=200&section=header&text=JavaScript%20-%20Les%20Bases&fontSize=45&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Variables%20%E2%80%A2%20Types%20%E2%80%A2%20Op%C3%A9rateurs%20%E2%80%A2%20Console&descAlignY=55&descSize=18" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-38bdf8?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Module-01%2F03-6366f1?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Statut-Actif-brightgreen?style=for-the-badge" />
</p>

## 🎯 Objectifs du cours

À la fin de ce module, l'étudiant sera capable de :
- Comprendre le rôle de JavaScript dans une page web
- Déclarer et utiliser des variables (`let`, `const`, `var`)
- Identifier les types de données de base
- Utiliser les opérateurs arithmétiques, de comparaison et logiques
- Afficher des résultats dans la console du navigateur

---

## 🧩 1. Qu'est-ce que JavaScript ?

JavaScript est le langage de **programmation** qui rend une page web **interactive**. Si HTML construit le squelette et CSS l'habille, **JavaScript donne vie** à la page : clics, animations, calculs, validations de formulaires, etc.

```html
<!-- On lie un fichier JS à une page HTML -->
<script src="script.js"></script>
```

> 💡 On peut aussi écrire du JS directement dans la console du navigateur (F12 → onglet *Console*) pour tester rapidement du code.

---

## 🧩 2. Les variables

Une variable est une **boîte nommée** qui contient une valeur.

```js
let prenom = "Amine";     // peut changer plus tard
const anneeNaissance = 1995; // ne change jamais
var ville = "Relizane";   // ancienne syntaxe, à éviter
```

| Mot-clé | Modifiable ? | Portée      | Recommandation           |
|---------|--------------|-------------|---------------------------|
| `let`   | ✅ Oui       | Bloc `{ }`  | Utiliser par défaut        |
| `const` | ❌ Non       | Bloc `{ }`  | Utiliser si la valeur fixe |
| `var`   | ✅ Oui       | Fonction    | ⚠️ À éviter (legacy)        |

### Règles de nommage

```js
let nomEtudiant = "Sarah";  // camelCase ✅
let 2eme_note = 15;          // ❌ interdit (commence par un chiffre)
let const = 5;               // ❌ interdit (mot réservé)
```

---

## 🧩 3. Les types de données

```js
let age = 22;                 // number
let nom = "Chikh";            // string
let estEtudiant = true;       // boolean
let notes = [12, 15, 18];     // array (tableau)
let profil = { nom: "Amine", age: 22 }; // object
let rien = null;              // null (vide intentionnellement)
let inconnu;                  // undefined (pas encore défini)
```

Pour vérifier le type d'une valeur, on utilise `typeof` :

```js
console.log(typeof age);        // "number"
console.log(typeof nom);        // "string"
console.log(typeof estEtudiant);// "boolean"
```

---

## 🧩 4. Les opérateurs

### Arithmétiques

```js
let a = 10, b = 3;
console.log(a + b); // 13  addition
console.log(a - b); // 7   soustraction
console.log(a * b); // 30  multiplication
console.log(a / b); // 3.33 division
console.log(a % b); // 1   reste (modulo)
console.log(a ** b);// 1000 puissance
```

### Comparaison

```js
console.log(5 == "5");   // true  (compare la valeur seulement)
console.log(5 === "5");  // false (compare valeur ET type) ✅ recommandé
console.log(5 !== "5");  // true
console.log(5 > 3);      // true
```

### Logiques

```js
let majeur = true, algerien = true;
console.log(majeur && algerien); // ET → true si les deux sont vrais
console.log(majeur || algerien); // OU → true si au moins un est vrai
console.log(!majeur);            // NON → inverse la valeur
```

---

## 🧩 5. Afficher dans la console

```js
console.log("Bonjour LingoLab !");
console.log("Résultat :", 5 + 3);
console.error("Ceci est une erreur");
console.warn("Ceci est un avertissement");
```

> 🔎 Ouvre la console de ton navigateur (clic droit → *Inspecter* → *Console*) pour voir ces messages en direct.

---

## 🧪 Exercices

### Exercice 1 — Déclaration (facile)

Complète le code pour déclarer les variables suivantes puis affiche-les dans la console.

```js
// TODO : déclare une variable "prenom" (string) avec ton prénom
___ prenom = ___;

// TODO : déclare une constante "anneeCours" avec la valeur 2026
___ anneeCours = ___;

// TODO : affiche les deux variables dans la console
console.log(___);
```

### Exercice 2 — Types de données (facile)

Pour chaque variable, écris en commentaire son type (`number`, `string`, `boolean`, `array`, `object`) sans utiliser `typeof` — puis vérifie ta réponse avec `typeof`.

```js
let x1 = 42;              // type : ___
let x2 = "LingoLab";       // type : ___
let x3 = false;            // type : ___
let x4 = [1, 2, 3];         // type : ___
let x5 = { ville: "Oran" }; // type : ___

// Vérifie tes réponses :
console.log(typeof x1, typeof x2, typeof x3, typeof x4, typeof x5);
```

### Exercice 3 — Opérateurs (intermédiaire)

Un étudiant a obtenu **14** en contrôle continu et **16** à l'examen. La moyenne finale se calcule ainsi : `(controle + examen * 2) / 3`.

```js
let controle = 14;
let examen = 16;

// TODO : calcule la moyenne avec la formule ci-dessus
let moyenne = ___;

// TODO : affiche "Moyenne : X" dans la console
console.log(___);

// TODO : vérifie si la moyenne est supérieure ou égale à 10 (admis)
let admis = ___;
console.log("Admis :", admis);
```

### Exercice 4 — Mini-défi (avancé)

Sans regarder la correction, prédis ce qu'affiche ce code, puis exécute-le pour vérifier :

```js
let a = "5";
let b = 5;

console.log(a == b);   // ta prédiction : ___
console.log(a === b);  // ta prédiction : ___
console.log(a + b);    // ta prédiction : ___ (attention au piège !)
console.log(Number(a) + b); // ta prédiction : ___
```

> 📁 Les corrigés de ces exercices seront disponibles dans le dossier `corrections/03-Javascript/`.

---

<p align="center">
  <img src="https://img.shields.io/badge/LingoLab-Academy-38bdf8?style=for-the-badge" />
  <img src="https://img.shields.io/badge/DevLab-Solutions-6366f1?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:6366f1,100:38bdf8&height=120&section=footer" width="100%"/>
</p>