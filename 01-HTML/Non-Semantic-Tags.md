<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:6b7280,100:9ca3af&amp;height=180&amp;section=header&amp;text=Balises%20Non-S%C3%A9mantiques%20%F0%9F%93%A6&amp;fontSize=36&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=35&amp;desc=Les%20boites%20neutres%20du%20HTML&amp;descAlignY=55&amp;descSize=16"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&amp;size=20&amp;pause=1000&amp;color=6B7280&amp;center=true&amp;vCenter=true&amp;width=650&amp;lines=div+%E2%80%A2+span+%E2%80%A2+b+%E2%80%A2+i+%E2%80%A2+br+%E2%80%A2+hr;des+boites+sans+signification+propre" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&amp;logo=html5&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Type-Non%20S%C3%A9mantique-6b7280?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif de la fiche

> Une balise **non sémantique** ne dit **rien sur le sens** de son contenu — elle sert uniquement de **conteneur générique** pour appliquer du style (CSS) ou du comportement (JavaScript). Ce n'est pas "mal" de les utiliser : c'est même indispensable ! Le problème, c'est de les utiliser **partout**, y compris là où une balise sémantique (`<nav>`, `<article>`...) existerait et serait plus appropriée.

<br/>

## 📂 Fichiers du projet

| Fichier | Lien GitHub |
|---|---|
| 📦 Ce guide (`Non-Semantic-Tags.md`) | [HTML/Html-Tags + Exercices/Non-Semantic-Tags.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/HTML/Html-Tags%20+%20Exercices/Non-Semantic-Tags.md) |
| 🧩 Guide complémentaire (sémantique) | [HTML/Html-Tags + Exercices/Semantic-Tags.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/HTML/Html-Tags%20+%20Exercices/Semantic-Tags.md) |
| 📖 Balises HTML utiles en Markdown | [HTML/Html-Tags + Exercices/Html-Tags.Md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/HTML/Html-Tags%20+%20Exercices/Html-Tags.Md) |

<br/>

## 🎬 Le concept en une image

<div align="center">
<svg width="480" height="180" viewBox="0 0 480 180" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="200" height="140" fill="#9ca3af" rx="10" stroke="#6b7280" stroke-width="2" stroke-dasharray="6,4">
    <animate attributeName="opacity" values="1;0.6;1" dur="2.5s" repeatCount="indefinite"/>
  </rect>
  <text x="120" y="95" font-family="monospace" font-size="16" fill="white" text-anchor="middle">&lt;div&gt;</text>
  <text x="120" y="115" font-family="Arial" font-size="10" fill="white" text-anchor="middle">"une boîte, sans plus"</text>

  <rect x="260" y="60" width="200" height="60" fill="#9ca3af" rx="30" stroke="#6b7280" stroke-width="2" stroke-dasharray="6,4">
    <animate attributeName="opacity" values="1;0.6;1" dur="2.5s" repeatCount="indefinite"/>
  </rect>
  <text x="360" y="95" font-family="monospace" font-size="14" fill="white" text-anchor="middle">&lt;span&gt;</text>
</svg>
<p><em>Aucune des deux ne dit "je suis une navigation" ou "je suis un article" — elles sont sémantiquement vides</em></p>
</div>

<br/>

## 1️⃣ `<div>` — le conteneur de bloc universel

```html
<div class="carte-produit">
  <img src="produit.jpg" alt="Photo du produit">
  <p>Nom du produit — 2500 DA</p>
</div>
```

> 🧠 **À retenir** : `<div>` est un élément de type **bloc** (il prend toute la largeur disponible et force un retour à la ligne). Il ne signifie **rien** en soi — son seul rôle est de regrouper des éléments pour les styliser ou les manipuler ensemble en CSS/JS.

<div align="center">

| ❌ Mauvaise pratique | ✅ Bonne pratique |
|---|---|
| `<div class="nav">...</div>` | `<nav>...</nav>` |
| `<div class="footer">...</div>` | `<footer>...</footer>` |
| `<div class="carte-produit">...</div>` (aucune balise sémantique n'existe pour "carte produit") | `<div>` reste le bon choix ici ✅ |

</div>

<br/>

## 2️⃣ `<span>` — le conteneur de texte en ligne

```html
<p>Le prix est de <span class="prix">2500 DA</span> aujourd'hui.</p>
```

> 🧠 Contrairement à `<div>`, `<span>` est un élément **en ligne** (*inline*) : il ne force **pas** de retour à la ligne, il s'insère au milieu du texte. On l'utilise pour cibler **un mot ou groupe de mots précis** avec du CSS (couleur, taille) sans casser le flux du paragraphe.

<div align="center">
<svg width="460" height="100" viewBox="0 0 460 100" xmlns="http://www.w3.org/2000/svg">
  <text x="20" y="40" font-family="Arial" font-size="15" fill="#333">Le prix est de </text>
  <rect x="150" y="22" width="80" height="24" fill="#fbbf24" rx="4">
    <animate attributeName="opacity" values="1;0.5;1" dur="2s" repeatCount="indefinite"/>
  </rect>
  <text x="190" y="40" font-family="Arial" font-size="14" fill="#333" text-anchor="middle">2500 DA</text>
  <text x="240" y="40" font-family="Arial" font-size="15" fill="#333"> aujourd'hui.</text>
  <text x="230" y="75" font-family="monospace" font-size="11" fill="#6b7280" text-anchor="middle">&lt;span&gt; ne casse pas la ligne — il reste "dans" le texte</text>
</svg>
</div>

<br/>

## 3️⃣ `<b>` vs `<strong>` — piège classique

```html
<p><b>Attention</b> : ceci est juste visuellement en gras.</p>
<p><strong>Attention</strong> : ceci a une importance réelle, signalée aux lecteurs d'écran.</p>
```

| Balise | Rendu visuel | Sens transmis |
|---|---|---|
| `<b>` | **Gras** | Aucun — purement visuel (non sémantique) |
| `<strong>` | **Gras** (même rendu par défaut !) | "Ce texte est important" — annoncé différemment par les lecteurs d'écran |

> ⚠️ **Le piège** : `<b>` et `<strong>` s'affichent **identiquement** dans le navigateur par défaut. La différence est invisible à l'œil mais essentielle pour l'accessibilité. Si le texte est réellement important → `<strong>`. Si c'est juste une convention visuelle (ex : un mot-clé dans une liste) sans urgence particulière → `<b>` est acceptable.

<br/>

## 4️⃣ `<i>` vs `<em>` — même piège, avec l'italique

```html
<p>Le mot <i>bug</i> vient de l'anglais.</p>
<p><em>Ne clique surtout pas ici</em> avant d'avoir lu les instructions.</p>
```

| Balise | Rendu visuel | Sens transmis |
|---|---|---|
| `<i>` | *Italique* | Aucun — ton différent, terme technique, nom de bateau... purement visuel |
| `<em>` | *Italique* (même rendu par défaut !) | "Ce texte est accentué/insisté" — change l'intonation pour un lecteur d'écran |

<br/>

## 5️⃣ `<br>` — saut de ligne

```html
<p>
  LingoLab Academy<br>
  Relizane, Algérie
</p>
```

> 🧠 À utiliser avec parcimonie : `<br>` casse une ligne **à l'intérieur** d'un même bloc de contenu logique (une adresse, un poème). Ce n'est **pas** un outil de mise en page — pour espacer des blocs, on utilise du CSS (`margin`), pas une accumulation de `<br><br><br>`.

<br/>

## 6️⃣ `<hr>` — séparateur visuel

```html
<p>Chapitre 1 terminé.</p>
<hr>
<p>Chapitre 2 commence ici.</p>
```

> `<hr>` trace une ligne horizontale pour séparer visuellement deux contenus qui n'ont pas de lien thématique direct — un changement de sujet à l'intérieur d'un même texte.

<br/>

## ⚖️ Le tableau de comparaison complet

| Balise | Type | Sémantique ? | Équivalent sémantique si applicable |
|---|---|---|---|
| `<div>` | Bloc | ❌ Non | `<nav>`, `<article>`, `<section>`, `<aside>`, `<header>`, `<footer>`, `<main>` selon le cas |
| `<span>` | En ligne | ❌ Non | `<time>`, `<mark>`, `<strong>`, `<em>` selon le cas |
| `<b>` | En ligne | ❌ Non (visuel uniquement) | `<strong>` si c'est réellement important |
| `<i>` | En ligne | ❌ Non (visuel uniquement) | `<em>` si c'est réellement une insistance |
| `<br>` | En ligne | ❌ Non | — (pas d'équivalent, usage ponctuel accepté) |
| `<hr>` | Bloc | ❌ Non | — (pas d'équivalent, usage ponctuel accepté) |

<br/>

## 🧠 Alors, `<div>`/`<span>` sont-ils "mauvais" ?

> **Non !** Ils restent indispensables. La règle d'or : **avant d'écrire `<div>` ou `<span>`, demande-toi s'il existe une balise sémantique qui correspond exactement à ce contenu.** Si oui, utilise-la. Si non (ex : une simple carte de mise en page, un wrapper pour centrer du contenu), `<div>`/`<span>` restent le bon choix.

<div align="center">
<svg width="480" height="140" viewBox="0 0 480 140" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="200" height="100" fill="#f0f0f0" stroke="#333" stroke-width="2" rx="8"/>
  <text x="120" y="55" font-family="Arial" font-size="12" fill="#333" text-anchor="middle" font-weight="bold">Une balise sémantique</text>
  <text x="120" y="75" font-family="Arial" font-size="12" fill="#333" text-anchor="middle" font-weight="bold">existe pour ce contenu ?</text>
  <text x="120" y="100" font-family="monospace" font-size="11" fill="#22c55e" text-anchor="middle">OUI → utilise-la</text>

  <rect x="260" y="20" width="200" height="100" fill="#f0f0f0" stroke="#333" stroke-width="2" rx="8"/>
  <text x="360" y="60" font-family="Arial" font-size="12" fill="#333" text-anchor="middle" font-weight="bold">Aucune balise sémantique</text>
  <text x="360" y="80" font-family="Arial" font-size="12" fill="#333" text-anchor="middle" font-weight="bold">ne correspond ?</text>
  <text x="360" y="105" font-family="monospace" font-size="11" fill="#6b7280" text-anchor="middle">NON → &lt;div&gt;/&lt;span&gt; ✅</text>
</svg>
</div>

<br/>

## 📄 Exemple complet — usage correct des deux familles

```html
<article>
  <h2>Nos formations</h2>

  <!-- div : pas de balise sémantique pour "une grille de cartes" -->
  <div class="grille-formations">

    <div class="carte-formation">
      <h3>Bureautique</h3>
      <p>Formation de <span class="duree">60 heures</span>.</p>
      <p><strong>Places limitées</strong> — inscrivez-vous vite !</p>
    </div>

    <div class="carte-formation">
      <h3>Développement Web</h3>
      <p>Formation de <span class="duree">60 heures</span>.</p>
      <p>Idéal pour les <em>vrais</em> débutants motivés.</p>
    </div>

  </div>
</article>
```

> Ici, `<div>` sert uniquement de conteneur de mise en page (grille, carte), tandis que `<strong>`, `<em>` et `<span>` gardent un rôle précis à l'intérieur du texte.

<br/>

## 🧪 Exercices pour les étudiants

1. Repère dans un de tes anciens projets HTML tous les `<div>` utilisés — pour chacun, demande-toi s'il devrait être une balise sémantique.
2. Transforme `<div class="titre-important">Attention</div>` en la bonne combinaison de balises (indice : structure + emphase).
3. Écris un court paragraphe utilisant à la fois `<b>` (terme technique sans urgence) et `<strong>` (avertissement réel) — explique la différence à l'oral à un camarade.
4. Construis une grille de 3 "cartes" (`<div>`) contenant chacune un titre, un `<span>` pour un prix, et un `<strong>` pour une mention "Promo".
5. **Défi** : reprends l'exemple complet ci-dessus et remplace `.grille-formations` par une vraie mise en page Flexbox ou Grid (voir le guide Flexbox du dépôt).

<br/>

## 📌 Résumé express

| Je veux... | Balise |
|---|---|
| Regrouper des éléments en bloc, sans signification particulière | `<div>` |
| Cibler un mot/groupe de mots dans une ligne de texte | `<span>` |
| Mettre en gras sans urgence particulière | `<b>` |
| Mettre en gras avec une importance réelle (accessibilité) | `<strong>` |
| Mettre en italique sans insistance particulière | `<i>` |
| Mettre en italique avec une insistance réelle (accessibilité) | `<em>` |
| Sauter une ligne à l'intérieur d'un même bloc | `<br>` |
| Séparer visuellement deux contenus | `<hr>` |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>