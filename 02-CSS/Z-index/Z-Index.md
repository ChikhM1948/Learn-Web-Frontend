<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:6366f1,100:a21caf&amp;height=180&amp;section=header&amp;text=Z-Index%20%F0%9F%97%82%EF%B8%8F&amp;fontSize=42&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=35&amp;desc=L'ordre%20d'empilement%20en%20CSS&amp;descAlignY=55&amp;descSize=16"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&amp;size=20&amp;pause=1000&amp;color=6366F1&amp;center=true&amp;vCenter=true&amp;width=650&amp;lines=z-index%3A+999%3B;stacking+context+%E2%80%A2+position+requise" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&amp;logo=css3&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-Interm%C3%A9diaire-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Cours-Z--Index-6366f1?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif du cours

> `z-index` décide **quel élément s'affiche par-dessus lequel** quand plusieurs éléments se chevauchent visuellement. C'est une notion courte à apprendre, mais avec un piège classique : elle ne fonctionne **que** sous certaines conditions précises.

<br/>

## 🧱 Le concept : des couches empilées

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDIwIiBoZWlnaHQ9IjI2MCIgdmlld0JveD0iMCAwIDQyMCAyNjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iNjAiIHk9IjE0MCIgd2lkdGg9IjE0MCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiMzOGJkZjgiIHJ4PSI4Ii8+CiAgPHRleHQgeD0iMTMwIiB5PSIxOTUiIGZvbnQtZmFtaWx5PSJtb25vc3BhY2UiIGZvbnQtc2l6ZT0iMTIiIGZpbGw9IndoaXRlIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj56LWluZGV4OiAxPC90ZXh0PgogIDxyZWN0IHg9IjEyMCIgeT0iMTAwIiB3aWR0aD0iMTQwIiBoZWlnaHQ9IjEwMCIgZmlsbD0iIzYzNjZmMSIgcng9IjgiIG9wYWNpdHk9IjAuOTUiPgogICAgPGFuaW1hdGUgYXR0cmlidXRlTmFtZT0ib3BhY2l0eSIgdmFsdWVzPSIwLjk1OzAuNjswLjk1IiBkdXI9IjIuNXMiIHJlcGVhdENvdW50PSJpbmRlZmluaXRlIi8+CiAgPC9yZWN0PgogIDx0ZXh0IHg9IjE5MCIgeT0iMTU1IiBmb250LWZhbWlseT0ibW9ub3NwYWNlIiBmb250LXNpemU9IjEyIiBmaWxsPSJ3aGl0ZSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+ei1pbmRleDogMjwvdGV4dD4KICA8cmVjdCB4PSIxODAiIHk9IjYwIiB3aWR0aD0iMTQwIiBoZWlnaHQ9IjEwMCIgZmlsbD0iI2EyMWNhZiIgcng9IjgiLz4KICA8dGV4dCB4PSIyNTAiIHk9IjExNSIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMiIgZmlsbD0id2hpdGUiIHRleHQtYW5jaG9yPSJtaWRkbGUiPnotaW5kZXg6IDM8L3RleHQ+CiAgPHRleHQgeD0iMjEwIiB5PSIyMCIgZm9udC1mYW1pbHk9Im1vbm9zcGFjZSIgZm9udC1zaXplPSIxMSIgZmlsbD0iIzU1NSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+dmFsZXVyIHBsdXMgZ3JhbmRlID0gcGx1cyBwcm9jaGUgZGUgbCfFk2lsID0gYWZmaWNow6kgYXUtZGVzc3VzPC90ZXh0Pgo8L3N2Zz4=" width="480"/>
</div>

> 🧠 **Analogie simple** : imagine des feuilles de papier calque empilées sur un bureau. `z-index` décide l'ordre de la pile — plus le nombre est grand, plus la feuille est proche du dessus.

<br/>

## 1️⃣ La règle n°1 — `z-index` ne marche QUE sur un élément positionné

```css
.carte {
  position: relative; /* ou absolute, fixed, sticky */
  z-index: 5;
}
```

> ⚠️ **Le piège n°1 des débutants** : écrire `z-index: 999` sur un élément en `position: static` (la valeur par défaut) **ne fait absolument rien**. `z-index` exige que l'élément ait une `position` autre que `static` — `relative`, `absolute`, `fixed` ou `sticky`.

| Position de l'élément | `z-index` fonctionne ? |
|---|---|
| `static` (défaut) | ❌ Non — ignoré silencieusement |
| `relative` | ✅ Oui |
| `absolute` | ✅ Oui |
| `fixed` | ✅ Oui |
| `sticky` | ✅ Oui |

<br/>

## 2️⃣ Comparer deux éléments — la valeur la plus grande gagne

```css
.arriere-plan {
  position: relative;
  z-index: 1;
}

.premier-plan {
  position: relative;
  z-index: 2;
}
```

> 🧠 Seule la **comparaison relative** compte : `z-index: 2` passe devant `z-index: 1`, exactement comme `z-index: 200` passerait devant `z-index: 100`. Il n'y a pas de valeur magique — seulement "plus grand que le voisin avec lequel je me chevauche".

<br/>

## 3️⃣ Cas d'usage réel — une fenêtre modale

```css
.overlay {
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  background: rgba(0, 0, 0, 0.5);
  z-index: 999;
}

.modale {
  position: fixed;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  background: white;
  padding: 24px;
  border-radius: 8px;
  z-index: 1000;
}
```

<div align="center">
<img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDQwIiBoZWlnaHQ9IjI0MCIgdmlld0JveD0iMCAwIDQ0MCAyNDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHJlY3QgeD0iMTAiIHk9IjEwIiB3aWR0aD0iNDIwIiBoZWlnaHQ9IjIyMCIgZmlsbD0iI2U1ZTdlYiIvPgogIDxyZWN0IHg9IjMwIiB5PSIzMCIgd2lkdGg9IjM4MCIgaGVpZ2h0PSIyMCIgZmlsbD0iI2NiZDVlMSIvPgogIDxyZWN0IHg9IjMwIiB5PSI2MCIgd2lkdGg9IjM4MCIgaGVpZ2h0PSIyMCIgZmlsbD0iI2NiZDVlMSIvPgogIDxyZWN0IHg9IjMwIiB5PSI5MCIgd2lkdGg9IjM4MCIgaGVpZ2h0PSIyMCIgZmlsbD0iI2NiZDVlMSIvPgogIDxyZWN0IHg9IjYwIiB5PSI1MCIgd2lkdGg9IjMyMCIgaGVpZ2h0PSIxNDAiIGZpbGw9ImJsYWNrIiBvcGFjaXR5PSIwLjUiPgogICAgPGFuaW1hdGUgYXR0cmlidXRlTmFtZT0ib3BhY2l0eSIgdmFsdWVzPSIwLjU7MC4zOzAuNSIgZHVyPSIycyIgcmVwZWF0Q291bnQ9ImluZGVmaW5pdGUiLz4KICA8L3JlY3Q+CiAgPHJlY3QgeD0iMTIwIiB5PSI3MCIgd2lkdGg9IjIwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IndoaXRlIiByeD0iOCIgc3Ryb2tlPSIjMzMzIiBzdHJva2Utd2lkdGg9IjIiLz4KICA8dGV4dCB4PSIyMjAiIHk9IjExNSIgZm9udC1mYW1pbHk9IkFyaWFsIiBmb250LXNpemU9IjEzIiBmaWxsPSIjMzMzIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmb250LXdlaWdodD0iYm9sZCI+TW9kYWxlPC90ZXh0PgogIDx0ZXh0IHg9IjIyMCIgeT0iMTM1IiBmb250LWZhbWlseT0ibW9ub3NwYWNlIiBmb250LXNpemU9IjEwIiBmaWxsPSIjNjM2NmYxIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj56LWluZGV4OiAxMDAwPC90ZXh0Pgo8L3N2Zz4=" width="480"/>
</div>

> 💡 La modale (`z-index: 1000`) doit avoir une valeur **plus grande** que le fond assombri (`z-index: 999`), qui lui-même doit être plus grand que tout le reste de la page (souvent laissée à `static`, donc automatiquement derrière).

<br/>

## 4️⃣ Le piège avancé — le "contexte d'empilement" (stacking context)

> 🧠 Un `z-index` élevé ne garantit pas **toujours** de passer devant tout : certaines propriétés (`position` + `z-index`, mais aussi `opacity < 1`, `transform`, `filter`) créent un **nouveau contexte d'empilement**. À l'intérieur de ce contexte, les `z-index` des enfants sont comparés **entre eux uniquement**, jamais directement avec des éléments d'un autre contexte. C'est une notion avancée : pour l'instant, retiens simplement que si un `z-index` "ne marche pas" alors qu'il devrait, la cause est souvent un parent avec `transform` ou `opacity` qui isole son contenu dans son propre contexte.

<br/>

## 📌 Résumé express

| Je veux... | Solution |
|---|---|
| Faire fonctionner `z-index` | Ajouter `position: relative/absolute/fixed/sticky` |
| Passer un élément devant un autre | Lui donner un `z-index` plus grand |
| Créer un fond assombri derrière une modale | `.overlay` en `z-index` inférieur à `.modale` |
| Déboguer un `z-index` qui "ne marche pas" | Vérifier qu'aucun parent n'a de `transform`/`opacity` qui crée un contexte isolé |

<br/>

## 🧪 Exercices

### Exercice 1 — Activer z-index

```css
.badge {
  ____: relative; /* (1) valeur nécessaire pour activer z-index */
  z-index: ____;   /* (2) une valeur qui passe devant .fond (z-index: 1) */
}
.fond {
  position: relative;
  z-index: 1;
}
```

**Consigne** : complétez les 2 blancs pour que `.badge` s'affiche devant `.fond`.

### Exercice 2 — Empiler 3 cartes qui se chevauchent

Construisez 3 `<div class="carte">` positionnées en `absolute` avec un léger décalage (`top`/`left` différents pour chacune), et donnez-leur des `z-index` de sorte que la **carte du milieu créée en HTML** s'affiche **au-dessus** des deux autres.

### Exercice 3 — Modale complète

En reprenant le code de la section 3, construisez une modale fonctionnelle : un bouton "Ouvrir" affiche l'overlay + la modale (vous pouvez utiliser uniquement `display: none/block` en CSS pour cette version simplifiée, sans JavaScript).

### 📊 Grille d'évaluation

| Critère | Points |
|---|---|
| Exercice 1 complété | 4 |
| Exercice 2 — ordre d'empilement correct | 8 |
| Exercice 3 — modale fonctionnelle | 8 |
| **Total** | **20** |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>
