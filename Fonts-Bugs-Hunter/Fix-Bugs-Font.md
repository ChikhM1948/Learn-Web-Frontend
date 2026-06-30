# Correction — Exercice CSS : La propriété `font`

## Tableau des 10 bugs et corrections

| # | Sélecteur concerné | Propriété | Erreur | Correction |
|---|---------------------|-----------|--------|------------|
| 1 | `body` | `font-family` | `(SegoeUI)` | `"Segoe UI"` |
| 2 | `h1` | `font-size` | `2.5` | `2.5rem` |
| 3 | `h1` | `font-weight` | `extra-bold` | `800` |
| 4 | `.subtitle` | `font-style` | `oblique-italic` | `italic` |
| 5 | `.card h2` | `font` (raccourci) | ordre inversé | `italic bold 1.4rem/1.6 "Georgia", serif` |
| 6 | `.card p` | `line-height` | `0.5` | `1.6` |
| 7 | `.citation p` | `font-variant` | `smallcaps` | `small-caps` |
| 8 | `.badge` | `font-size` | `11 px` | `11px` |
| 9 | `.author` | `font-weight` | `light` | `300` |
| 10 | `footer` | `font` (raccourci) | `font-family` manquante | `italic 0.8rem "Segoe UI", sans-serif` |

## Explication rapide des erreurs

**Bug 1 — Parenthèses invalides**
Un nom de police avec espace doit être entre guillemets, jamais entre parenthèses.

**Bug 2 — Unité manquante**
Toute valeur de taille en CSS (sauf `0` et `line-height` sans unité) nécessite une unité (`rem`, `px`, `em`...).

**Bug 3 — Mot-clé invalide**
`font-weight` accepte uniquement des mots-clés précis (`normal`, `bold`, `lighter`, `bolder`) ou des valeurs numériques de 100 à 900. `extra-bold` n'existe pas.

**Bug 4 — Valeur invalide**
`font-style` accepte seulement `normal`, `italic` ou `oblique` — pas de valeur composée.

**Bug 5 — Ordre incorrect**
La syntaxe de la propriété raccourcie `font` est :
`font: [style] [variant] [weight] size/line-height family;`

**Bug 6 — Valeur trop faible**
Une `line-height` inférieure à 1 fait chevaucher les lignes de texte.

**Bug 7 — Tiret manquant**
La valeur correcte est `small-caps`, avec un tiret entre les deux mots.

**Bug 8 — Espace interdit**
En CSS, il ne doit jamais y avoir d'espace entre un nombre et son unité.

**Bug 9 — Mot-clé vs valeur numérique**
`light` n'est pas un mot-clé CSS standard pour `font-weight` ; il faut utiliser sa valeur numérique équivalente, `300`.

**Bug 10 — Propriété raccourcie incomplète**
La propriété raccourcie `font` exige obligatoirement `font-size` **et** `font-family`. Sans `font-family`, la déclaration est invalide.

---
*LingoLab Academy © 2026 dr Chikh Amine*