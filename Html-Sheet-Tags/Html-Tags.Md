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

## Remarque importante

Le support de ces balises HTML dépend du moteur qui affiche le Markdown :
- **GitHub** (README, issues) : supporte presque toutes ces balises.
- **Sites statiques / générateurs de documentation** : variable selon la configuration.
- **Obsidian, Typora** : support large mais peut varier selon les plugins.
- **Markdown "strict"** : peut nettoyer (supprimer) le HTML brut par sécurité.

Toujours tester le rendu sur la plateforme cible avant de livrer un document final.

---

### Exercice pour les étudiants

Rédigez un court paragraphe sur vous-même en utilisant au moins :
1. Une balise `<br>`
2. Une balise `<u>` ou `<mark>`
3. Une balise `<details>` avec un `<summary>`