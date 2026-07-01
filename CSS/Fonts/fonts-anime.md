<!--
  📘 GUIDE ANIMÉ — TYPOGRAPHIE CSS (FONTS)
  HTML + CSS intégré pour des démonstrations ANIMÉES.
  ⚠️ Rendu : ouvre en Aperçu VS Code (Ctrl+Shift+V), Obsidian ou Typora.
  GitHub.com filtre les <style> par sécurité (le code restera lisible,
  mais les animations ne joueront pas directement sur github.com).
-->

<div align="center">

# 🔤 TYPOGRAPHIE CSS — Le Guide Animé
### Comprendre les polices en les voyant changer

![CSS](https://img.shields.io/badge/CSS-Typography-38B2AC?style=for-the-badge&logo=css3)
![Niveau](https://img.shields.io/badge/Niveau-Débutant%20→%20Intermédiaire-orange?style=for-the-badge)

</div>

---

## 🧠 1. C'est quoi la typographie CSS ?

La typographie, c'est **tout ce qui contrôle l'apparence du texte** :
la police, sa taille, son épaisseur, l'espacement des lettres et des lignes.

**Les propriétés clés :**
- `font-family` → quelle police
- `font-size` → quelle taille
- `font-weight` → quelle épaisseur (gras/fin)
- `font-style` → normal / italique
- `line-height` → hauteur de ligne
- `letter-spacing` → espace entre les lettres

```css
p {
  font-family: "Poppins", sans-serif;
  font-size: 16px;
  font-weight: 400;
  line-height: 1.5;
}
```

---

## 🎬 2. Démo animée — `font-family`

<div>
<style>
.demo1-text {
  background: #1e293b;
  color: white;
  padding: 20px;
  border-radius: 12px;
  font-size: 28px;
  text-align: center;
  animation: family-cycle 8s infinite;
}
@keyframes family-cycle {
  0%, 20%   { font-family: "Georgia", serif; }
  25%, 45%  { font-family: "Courier New", monospace; }
  50%, 70%  { font-family: "Arial", sans-serif; }
  75%, 95%  { font-family: "Comic Sans MS", cursive; }
  100%      { font-family: "Georgia", serif; }
}
</style>
<div class="demo1-text">LingoLab Academy</div>
</div>

👀 **Regarde** : le même mot change complètement d'ambiance selon la police
utilisée — `serif` → `monospace` → `sans-serif` → `cursive`.

```css
p {
  font-family: "Georgia", serif; /* police de secours obligatoire ! */
}
```

> 💡 On met toujours une **police de secours** (`serif`, `sans-serif`...)
> au cas où la police principale ne charge pas.

---

## 🎬 3. Démo animée — `font-weight`

<div>
<style>
.demo2-text {
  background: #1e293b;
  color: white;
  padding: 20px;
  border-radius: 12px;
  font-size: 32px;
  text-align: center;
  font-family: Arial, sans-serif;
  animation: weight-cycle 6s infinite;
}
@keyframes weight-cycle {
  0%, 20%   { font-weight: 100; }
  25%, 45%  { font-weight: 400; }
  50%, 70%  { font-weight: 700; }
  75%, 95%  { font-weight: 900; }
  100%      { font-weight: 100; }
}
</style>
<div class="demo2-text">Aa Bb Cc</div>
</div>

👀 **Ordre observé** : `100` (ultra-fin) → `400` (normal) → `700` (gras)
→ `900` (extra-gras).

```css
h1 {
  font-weight: 700; /* ou "bold" */
}
p {
  font-weight: 400; /* ou "normal" */
}
```

---

## 🎬 4. Démo animée — `font-size`

<div>
<style>
.demo3-text {
  background: #1e293b;
  color: #38bdf8;
  padding: 20px;
  border-radius: 12px;
  text-align: center;
  font-family: Arial, sans-serif;
  font-weight: 700;
  animation: size-cycle 6s infinite;
}
@keyframes size-cycle {
  0%, 25%  { font-size: 14px; }
  40%, 65% { font-size: 32px; }
  80%, 100% { font-size: 56px; }
}
</style>
<div class="demo3-text">Aa</div>
</div>

```css
small   { font-size: 12px; }
p       { font-size: 16px; }  /* taille de base recommandée */
h1      { font-size: 40px; }
```

> 📏 Astuce : utilise `rem` plutôt que `px` pour que la taille s'adapte
> aux préférences d'accessibilité du visiteur (`1rem = 16px` par défaut).

---

## 🎬 5. Démo animée — `letter-spacing`

<div>
<style>
.demo4-text {
  background: #1e293b;
  color: white;
  padding: 20px;
  border-radius: 12px;
  text-align: center;
  font-size: 24px;
  font-family: Arial, sans-serif;
  text-transform: uppercase;
  animation: spacing-cycle 6s infinite;
}
@keyframes spacing-cycle {
  0%, 30%  { letter-spacing: -2px; }
  50%, 80% { letter-spacing: 0px; }
  100%     { letter-spacing: 10px; }
}
</style>
<div class="demo4-text">Design</div>
</div>

```css
h2 {
  letter-spacing: 2px;   /* lettres plus espacées → élégant */
  text-transform: uppercase;
}
```

---

## 🎬 6. Démo animée — `line-height`

<div>
<style>
.demo5-text {
  background: #1e293b;
  color: white;
  padding: 20px;
  border-radius: 12px;
  font-family: Arial, sans-serif;
  font-size: 15px;
  width: 260px;
  margin: 0 auto;
  animation: lh-cycle 6s infinite;
}
@keyframes lh-cycle {
  0%, 30%  { line-height: 1; }
  50%, 80% { line-height: 1.6; }
  100%     { line-height: 2.5; }
}
</style>
<div class="demo5-text">
Flexbox et Typographie sont les deux bases du design web moderne à maîtriser.
</div>
</div>

👀 Une `line-height` trop petite = texte compressé, illisible.
Une bonne valeur (`1.4` à `1.6`) = lecture confortable.

```css
p {
  line-height: 1.6; /* valeur sans unité = multiplicateur de la font-size */
}
```

---

## 🎬 7. Démo animée — `font-style` & `text-decoration`

<div>
<style>
.demo6-text {
  background: #1e293b;
  color: #fbbf24;
  padding: 20px;
  border-radius: 12px;
  text-align: center;
  font-size: 26px;
  font-family: Georgia, serif;
  animation: style-cycle 8s infinite;
}
@keyframes style-cycle {
  0%, 20%  { font-style: normal; text-decoration: none; }
  25%, 45% { font-style: italic; text-decoration: none; }
  50%, 70% { font-style: normal; text-decoration: underline; }
  75%, 95% { font-style: italic; text-decoration: line-through; }
  100%     { font-style: normal; text-decoration: none; }
}
</style>
<div class="demo6-text">Citation du jour</div>
</div>

```css
em     { font-style: italic; }
a      { text-decoration: underline; }
del    { text-decoration: line-through; }
```

---

## 🌐 8. Importer une police web (Google Fonts)

```html
<!-- Dans le <head> du HTML -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap" rel="stylesheet">
```

```css
body {
  font-family: "Poppins", sans-serif;
}
```

> ⚡ `font-display: swap` évite le texte invisible pendant le chargement
> de la police (le texte s'affiche avec la police système en attendant).

**Ou en local avec `@font-face` :**

```css
@font-face {
  font-family: "MaPolice";
  src: url("/fonts/MaPolice.woff2") format("woff2");
  font-weight: 400;
  font-display: swap;
}
```

---

## 📝 9. Aide-mémoire (cheat sheet)

| Propriété | Rôle | Exemples de valeurs |
|---|---|---|
| `font-family` | choix de la police | `"Poppins", sans-serif` |
| `font-size` | taille du texte | `16px`, `1rem`, `1.2em` |
| `font-weight` | épaisseur | `100`–`900`, `normal`, `bold` |
| `font-style` | italique ou pas | `normal`, `italic` |
| `line-height` | hauteur de ligne | `1.4`, `1.6`, `24px` |
| `letter-spacing` | espace entre lettres | `0.5px`, `2px`, `-1px` |
| `text-transform` | casse du texte | `uppercase`, `lowercase`, `capitalize` |
| `text-decoration` | souligné / barré | `underline`, `line-through`, `none` |
| `text-align` | alignement | `left`, `center`, `right`, `justify` |

---

## ✏️ 10. Exercices pour les étudiants

1. Crée un titre `h1` avec une police Google Fonts de ton choix,
   `font-weight: 700` et `letter-spacing: 1px`.
2. Compare visuellement un même paragraphe avec `line-height: 1` puis `1.6`.
3. Fabrique une carte de citation avec police en `italic` et alignement `center`.
4. **Défi** : reproduis une des animations ci-dessus avec ta propre police
   et tes propres couleurs.
5. Recherche 2 polices "serif" et 2 polices "sans-serif" sur Google Fonts
   et explique en une phrase quand utiliser chaque catégorie.

---

<div align="center">

💡 **Astuce prof** : ouvre ce fichier dans VS Code et fais `Ctrl+Shift+V`
pour voir toutes les animations en direct pendant le cours.

Made with 💙 for **LingoLab Academy**

</div>
