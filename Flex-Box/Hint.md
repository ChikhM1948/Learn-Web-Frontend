# Consigne — Créer une carte (card) avec Flexbox

## Objectif
Compléter le code CSS ci-dessous pour transformer le HTML fourni en une **carte** bien organisée, comme dans l'exemple vu en cours : un titre, un texte, et deux boutons alignés côte à côte.

## Ce qui est fourni — HTML (ne pas modifier)

```html
<div class="card">
  <h3>Card title</h3>
  <p>This is a short description of the card content, demonstrating how flexbox stacks elements vertically with consistent spacing.</p>
  <div class="card-actions">
    <button>Action</button>
    <button>Cancel</button>
  </div>
</div>
```

## À vous de jouer — CSS à compléter

Remplacez chaque `____` par la bonne valeur ou la bonne propriété.

```css
.card {
  display: ____;              /* (1) active flexbox sur .card */
  flex-direction: ____;       /* (2) empile les éléments verticalement */
  gap: ____;                  /* (3) espace de 8px entre chaque élément */
  background: #fff;
  border: 1px solid #e0e0e0;
  border-radius: 12px;
  padding: 1.25rem;
  max-width: 320px;
}

.card-actions {
  display: ____;              /* (4) active flexbox sur .card-actions */
  gap: ____;                  /* (5) espace de 8px entre les boutons */
  margin-top: 8px;
}
```

## Consignes

1. Complétez les **5 propriétés manquantes** dans le code CSS ci-dessus.
2. Copiez le HTML et votre CSS complété dans un seul fichier `.html` (ou dans deux fichiers liés : `index.html` + `style.css`).
3. Ouvrez le fichier dans votre navigateur et vérifiez que :
   - Le titre, le texte et les boutons sont **empilés verticalement**.
   - Les deux boutons sont **côte à côte**, pas l'un sous l'autre.
   - Il y a un espace régulier entre chaque élément (pas besoin de `margin` partout).
4. Ajoutez une question écrite (3-4 phrases) : **Pourquoi `.card-actions` n'a-t-il pas besoin de `flex-direction` ?** (Indice : pensez à la valeur par défaut de cette propriété.)

## Bonus (facultatif)

- Changez `flex-direction` de `.card-actions` en `column` et observez ce qui change.
- Ajoutez `justify-content: center;` sur `.card-actions` pour centrer les boutons.
- Ajoutez `align-items: center;` sur `.card` et observez l'effet sur le titre et le texte.

## Grille d'évaluation

| Critère | Points |
|---|---|
| Les 5 blancs sont correctement remplis | 10 |
| La carte s'affiche correctement dans le navigateur | 5 |
| Réponse à la question écrite | 3 |
| Bonus réalisé (au moins un) | 2 |
| **Total** | **20** |