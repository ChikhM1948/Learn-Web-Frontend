<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:a855f7,100:38bdf8&height=200&section=header&text=JavaScript%20-%20Variables%20en%20Situation%20R%C3%A9elle&fontSize=32&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Mini-projets%20pratiques%20avec%20des%20variables&descAlignY=55&descSize=18" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-a855f7?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Module-01%2F03%20%E2%80%94%20Exercices-38bdf8?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Type-Projet%20Concret-brightgreen?style=for-the-badge" />
</p>

## 🎯 Objectif

Utiliser uniquement ce que tu connais du **Module 1** (variables, types, opérateurs, template literals) pour résoudre des **cas concrets** inspirés de vrais besoins : fiche étudiant, facture, conversion, budget. Pas de boucles ni de conditions ici — juste des variables bien construites.

> 💡 Rappel : `let` pour ce qui change, `const` pour ce qui ne change pas, et les *template literals* (`` `Bonjour ${nom}` ``) pour construire des phrases proprement.

---

## 🧪 Projet 1 — Fiche d'inscription étudiant (LingoLab Academy)

Un centre de formation comme LingoLab a besoin d'enregistrer les informations d'un nouvel inscrit et d'afficher une fiche résumée.

```js
const prenom = "Sarah";
const nom = "Benali";
const anneeNaissance = 2005;
const anneeActuelle = 2026;
const formationChoisie = "Anglais - Niveau B1";
const fraisInscription = 8000; // en DA
```

**À faire :**

```js
// TODO 1 : construis le nom complet "Prénom NOM" dans une variable "nomComplet"
const nomComplet = ___;

// TODO 2 : calcule l'âge de l'étudiant (anneeActuelle - anneeNaissance)
const age = ___;

// TODO 3 : construis une phrase récapitulative avec un template literal :
// "Sarah BENALI, 21 ans, inscrit(e) à Anglais - Niveau B1 pour 8000 DA."
const ficheResume = ___;

console.log(ficheResume);
```

<details>
<summary>💡 Indice</summary>

Un *template literal* s'écrit avec des backticks : `` `${variable} texte ${autre}` ``.
</details>

---

## 🧪 Projet 2 — Ticket de caisse (mini e-commerce)

Tu développes la logique de calcul d'un panier pour une boutique en ligne (comme celles que DevLab Solutions pourrait livrer à un client).

```js
const nomProduit = "Casque Bluetooth";
const prixUnitaire = 4500;   // en DA
const quantite = 3;
const tauxTVA = 0.19;        // 19%
const codePromo = "LINGO10"; // réduction de 10%
```

**À faire :**

```js
// TODO 1 : calcule le sous-total (prixUnitaire * quantite)
const sousTotal = ___;

// TODO 2 : applique une réduction de 10% (le code promo est actif)
const montantReduction = ___;
const totalApresReduction = ___;

// TODO 3 : calcule la TVA sur le total après réduction
const montantTVA = ___;

// TODO 4 : calcule le total final TTC (toutes taxes comprises)
const totalFinal = ___;

// TODO 5 : affiche un ticket lisible avec un template literal multi-lignes
const ticket = `
--- Ticket de caisse ---
Produit : ${nomProduit}
Quantité : ${quantite}
Sous-total : ${sousTotal} DA
Réduction (${codePromo}) : -${___} DA
TVA (19%) : ${___} DA
TOTAL : ${___} DA
------------------------
`;

console.log(ticket);
```

> ⚠️ Attention à l'ordre des opérations : la réduction s'applique **avant** la TVA.

---

## 🧪 Projet 3 — Convertisseur de température (widget réel)

Un client demande un petit widget web qui convertit une température de Celsius en Fahrenheit — un vrai composant qu'on retrouve dans des sites météo.

Formule : `F = (C × 9/5) + 32`

```js
const temperatureCelsius = 28;
```

**À faire :**

```js
// TODO 1 : applique la formule de conversion
const temperatureFahrenheit = ___;

// TODO 2 : construis un message d'affichage arrondi à 1 décimale
// indice : la méthode .toFixed(1) arrondit un nombre à 1 décimale
const message = `Il fait ${temperatureCelsius}°C, soit ${___}°F`;

console.log(message);
```

---

## 🧪 Projet 4 — Suivi de budget mensuel (mini-défi combiné)

Tu gères ton budget personnel (ou celui d'un petit business comme LingoLab) et tu veux calculer ce qu'il te reste à la fin du mois.

```js
const revenuMensuel = 65000;      // DA
const loyer = 18000;
const facturesElectriciteEau = 3200;
const abonnementInternet = 2500;
const depensesAlimentaires = 15000;
const epargneObjectif = 0.15;     // on veut épargner 15% du revenu
```

**À faire :**

```js
// TODO 1 : calcule le total des dépenses fixes
const totalDepenses = ___;

// TODO 2 : calcule le montant à épargner (15% du revenu mensuel)
const montantEpargne = ___;

// TODO 3 : calcule ce qu'il reste réellement disponible
// (revenu - dépenses fixes - épargne)
const resteDisponible = ___;

// TODO 4 : calcule le pourcentage du revenu déjà "engagé" (dépenses + épargne)
// astuce : (totalDepenses + montantEpargne) / revenuMensuel * 100
const pourcentageEngage = ___;

const rapport = `
Revenu : ${revenuMensuel} DA
Dépenses fixes : ${totalDepenses} DA
Épargne (15%) : ${montantEpargne} DA
Reste disponible : ${resteDisponible} DA
Budget engagé : ${pourcentageEngage.toFixed(1)}%
`;

console.log(rapport);
```

---

## 🚀 Défi bonus — Va plus loin

Choisis **un** des projets ci-dessus et améliore-le en ajoutant une variable et un calcul supplémentaire de ton choix. Exemples :
- Projet 1 : ajoute une variable `dateInscription` et un champ dans la fiche
- Projet 2 : ajoute une variable `fraisLivraison` intégrée au total
- Projet 4 : ajoute une dépense variable comme `sortiesLoisirs`

> 📁 Les corrigés seront disponibles dans `corrections/03-Javascript/Variables-Projet-Reel/`.

---

<p align="center">
  <img src="https://img.shields.io/badge/LingoLab-Academy-a855f7?style=for-the-badge" />
  <img src="https://img.shields.io/badge/DevLab-Solutions-38bdf8?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:38bdf8,100:a855f7&height=120&section=footer" width="100%"/>
</p>