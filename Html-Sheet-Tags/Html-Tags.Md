# Balises HTML utiles dans un fichier Markdown

Le Markdown ne couvre pas tout. Quand une fonctionnalité manque, on peut utiliser du HTML directement dans le fichier `.md`. Voici les balises les plus utiles, avec exemple de code et résultat.

---

## 1. Saut de ligne — `<br>`

En Markdown, un simple retour à la ligne est souvent ignoré. `<br>` force le saut de ligne.

**Code :**
```html
Première ligne.<br>
Deuxième ligne.
```

**Résultat :**

Première ligne.<br>
Deuxième ligne.

---

## 2. Espace insécable — `&nbsp;`

```html
Mot1&nbsp;&nbsp;&nbsp;Mot2
```

Mot1&nbsp;&nbsp;&nbsp;Mot2

---

## 3. Souligner du texte — `<u>`

Markdown n'a pas de syntaxe native pour souligner.

**Code :**
```html
<u>Ce texte est souligné</u>
```

**Résultat :** <u>Ce texte est souligné</u>

---

## 4. Texte en exposant et en indice — `<sup>` / `<sub>`

**Code :**
```html
H<sub>2</sub>O et E = mc<sup>2</sup>
```

**Résultat :** H<sub>2</sub>O et E = mc<sup>2</sup>

---

## 5. Surligner du texte — `<mark>`

**Code :**
```html
<mark>Texte important surligné</mark>
```

**Résultat :** <mark>Texte important surligné</mark>

---

## 6. Touches de clavier — `<kbd>`

**Code :**
```html
Pour copier : <kbd>Ctrl</kbd> + <kbd>C</kbd>
```

**Résultat :** Pour copier : <kbd>Ctrl</kbd> + <kbd>C</kbd>

---

## 7. Centrer un bloc — `<div align="center">`

**Code :**
```html
<div align="center">

**Ce texte est centré**

</div>
```

**Résultat :**

<div align="center">

**Ce texte est centré**

</div>

---

## 8. Image avec taille contrôlée — `<img>`

La syntaxe Markdown `![alt](url)` ne permet pas de fixer la largeur. Avec `<img>`, oui.

**Code :**
```html
<img src="https://via.placeholder.com/150" width="150">
```

---

## 9. Section repliable — `<details>` / `<summary>`

Très utile pour cacher une correction ou un contenu optionnel.

**Code :**
```html
<details>
<summary>Cliquez pour voir la réponse</summary>

La réponse est 42.

</details>
```

**Résultat :**

<details>
<summary>Cliquez pour voir la réponse</summary>

La réponse est 42.

</details>

---

## 10. Tableau HTML (pour cas complexes) — `<table>`

Quand un tableau Markdown classique ne suffit pas (cellules fusionnées, mise en page spéciale).

**Code :**
```html
<table>
  <tr>
    <th>Nom</th>
    <th>Note</th>
  </tr>
  <tr>
    <td>Ahmed</td>
    <td>16/20</td>
  </tr>
</table>
```

**Résultat :**

<table>
  <tr>
    <th>Nom</th>
    <th>Note</th>
  </tr>
  <tr>
    <td>Ahmed</td>
    <td>16/20</td>
  </tr>
</table>

---

## 11. Ancre personnalisée — `<a id="...">`

Permet de créer un point de lien interne précis.

**Code :**
```html
<a id="section-exercices"></a>
## Exercices

Lien vers cette section : [Aller aux exercices](#section-exercices)
```

---

## 12. Texte barré — `<del>` / `<s>`

`<del>` indique un texte supprimé (sens sémantique), `<s>` un texte simplement barré visuellement.

**Code :**
```html
<del>Ancien prix : 2000 DA</del>
<s>Erreur corrigée</s>
```

**Résultat :** <del>Ancien prix : 2000 DA</del> — <s>Erreur corrigée</s>

---

## 13. Couleur de texte — `<span style="color:...">`

Markdown ne permet pas de colorer du texte. `<span>` avec un style en ligne le permet.

**Code :**
```html
<span style="color:red">Texte en rouge</span>
<span style="color:blue">Texte en bleu</span>
```

**Résultat :** <span style="color:red">Texte en rouge</span> — <span style="color:blue">Texte en bleu</span>

---

## 14. Citation avec source — `<blockquote>` + `<cite>`

**Code :**
```html
<blockquote>
  La connaissance s'acquiert par la pratique.
  <cite>— Proverbe</cite>
</blockquote>
```

**Résultat :**

<blockquote>
  La connaissance s'acquiert par la pratique.
  <cite>— Proverbe</cite>
</blockquote>

---

## 15. Police de texte — `<font>` (ancien, à éviter mais encore utilisé)

**Code :**
```html
<font size="5" color="green">Titre en grand et en vert</font>
```

**Résultat :** <font size="5" color="green">Titre en grand et en vert</font>

> Remarque : `<font>` est une balise obsolète en HTML5. Préférez `<span style="...">` quand c'est possible.

---

## 16. Ligne horizontale — `<hr>`

Markdown a `---`, mais `<hr>` permet plus de contrôle (épaisseur, couleur via CSS).

**Code :**
```html
<hr>
```

**Résultat :**

<hr>

---

## 17. Mise en page sur deux colonnes — `<table>` détourné

**Code :**
```html
<table>
<tr>
<td width="50%">

**Colonne gauche**
Texte ici.

</td>
<td width="50%">

**Colonne droite**
Autre texte ici.

</td>
</tr>
</table>
```

**Résultat :**

<table>
<tr>
<td width="50%">

**Colonne gauche**
Texte ici.

</td>
<td width="50%">

**Colonne droite**
Autre texte ici.

</td>
</tr>
</table>

---

## Remarque importante

Le support de ces balises HTML dépend du moteur qui affiche le Markdown :
- **GitHub** (README, issues) : supporte presque toutes ces balises.
- **Sites statiques / générateurs de documentation** : variable selon la configuration.
- **Obsidian, Typora** : support large mais peut varier selon les plugins.
- **Markdown "strict"** : peut nettoyer (supprimer) le HTML brut par sécurité.

Toujours tester le rendu sur la plateforme cible avant de livrer un document final.

---

## Exercices pour les étudiants

### Exercice 1 — Présentation personnelle
Rédigez un court paragraphe sur vous-même en utilisant au moins :
1. Une balise `<br>`
2. Une balise `<u>` ou `<mark>`
3. Une balise `<details>` avec un `<summary>`

### Exercice 2 — Fiche produit
Créez une fiche produit (réel ou imaginaire) qui utilise :
1. `<del>` pour montrer un ancien prix barré
2. `<span style="color:...">` pour mettre en valeur le nouveau prix
3. Un `<table>` simple pour lister les caractéristiques (nom, prix, disponibilité)

### Exercice 3 — Mise en forme d'un cours
À partir d'un petit texte de cours (5 lignes minimum), ajoutez :
1. Un titre avec `<font>` ou `<span style="...">` pour le mettre en couleur
2. Une `<blockquote>` contenant une citation ou définition importante, avec `<cite>` pour la source
3. Un `<hr>` pour séparer deux parties du cours

### Exercice 4 — Page biographique en deux colonnes
En utilisant un `<table>` à deux colonnes (`<td width="50%">`), présentez :
- Colonne gauche : une photo (`<img>` avec largeur fixée) et votre nom
- Colonne droite : un court texte de présentation avec `<sup>` ou `<sub>` pour une note de bas de texte

### Exercice 5 — FAQ repliable
Créez une mini FAQ (3 questions minimum) où chaque réponse est cachée dans un `<details>`/`<summary>`. Utilisez `<kbd>` pour illustrer au moins un raccourci clavier dans une des réponses.

### Exercice 6 — Défi combiné
Combinez au moins 6 balises différentes vues dans ce document pour créer une page complète (par exemple une annonce d'événement, un CV simplifié, ou un menu de restaurant). Listez en commentaire (sous forme de liste Markdown) les balises utilisées.