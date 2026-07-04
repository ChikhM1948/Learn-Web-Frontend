<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:22c55e,100:38bdf8&amp;height=180&amp;section=header&amp;text=Balises%20S%C3%A9mantiques%20%F0%9F%A7%A9&amp;fontSize=40&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=35&amp;desc=HTML5%20qui%20a%20du%20sens&amp;descAlignY=55&amp;descSize=16"/>

<a href="#">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&amp;size=20&amp;pause=1000&amp;color=22C55E&amp;center=true&amp;vCenter=true&amp;width=650&amp;lines=header+%E2%80%A2+nav+%E2%80%A2+main+%E2%80%A2+article+%E2%80%A2+section;aside+%E2%80%A2+footer+%E2%80%A2+figure+%E2%80%A2+time" alt="Typing SVG" />
</a>

<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&amp;logo=html5&amp;logoColor=white"/>
<img src="https://img.shields.io/badge/Niveau-D%C3%A9butant-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Type-S%C3%A9mantique-22c55e?style=for-the-badge"/>

</div>

<br/>

## 🎯 Objectif de la fiche

> Une balise **sémantique** décrit **le sens** de son contenu, pas seulement son apparence. `<nav>` dit "ceci est une navigation", `<article>` dit "ceci est un contenu autonome" — alors qu'une `<div>` ne dit rien du tout. Les balises sémantiques aident **les moteurs de recherche** (SEO), **les lecteurs d'écran** (accessibilité), et **les autres développeurs** (lisibilité du code) à comprendre la structure de la page sans lire une seule ligne de CSS.

<br/>

## 📂 Fichiers du projet

| Fichier | Lien GitHub |
|---|---|
| 🧩 Ce guide (`Semantic-Tags.md`) | [HTML/Html-Tags + Exercices/Semantic-Tags.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/HTML/Html-Tags%20+%20Exercices/Semantic-Tags.md) |
| 🚫 Guide complémentaire (non-sémantique) | [HTML/Html-Tags + Exercices/Non-Semantic-Tags.md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/HTML/Html-Tags%20+%20Exercices/Non-Semantic-Tags.md) |
| 📖 Balises HTML utiles en Markdown | [HTML/Html-Tags + Exercices/Html-Tags.Md](https://github.com/ChikhM1948/Learn-Web-Frontend/blob/main/HTML/Html-Tags%20+%20Exercices/Html-Tags.Md) |

<br/>

## 🗺️ Le plan d'une page en un coup d'œil

<div align="center">
<svg width="480" height="380" viewBox="0 0 480 380" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="10" width="460" height="360" fill="#fafafa" stroke="#333" stroke-width="2"/>

  <rect x="25" y="25" width="430" height="50" fill="#38bdf8" rx="6">
    <animate attributeName="opacity" values="1;0.7;1" dur="2.5s" repeatCount="indefinite"/>
  </rect>
  <text x="240" y="55" font-family="monospace" font-size="14" fill="white" text-anchor="middle">&lt;header&gt;</text>

  <rect x="25" y="85" width="430" height="35" fill="#0ea5e9" rx="6"/>
  <text x="240" y="107" font-family="monospace" font-size="13" fill="white" text-anchor="middle">&lt;nav&gt;</text>

  <rect x="25" y="130" width="430" height="150" fill="none" stroke="#22c55e" stroke-width="2" stroke-dasharray="5,3"/>
  <text x="45" y="122" font-family="monospace" font-size="11" fill="#22c55e">&lt;main&gt;</text>

  <rect x="35" y="140" width="270" height="130" fill="#22c55e" rx="6" opacity="0.85">
    <animate attributeName="opacity" values="0.85;0.5;0.85" dur="3s" repeatCount="indefinite"/>
  </rect>
  <text x="170" y="165" font-family="monospace" font-size="13" fill="white" text-anchor="middle">&lt;article&gt;</text>
  <rect x="50" y="180" width="240" height="30" fill="#16a34a" rx="4"/>
  <text x="170" y="200" font-family="monospace" font-size="11" fill="white" text-anchor="middle">&lt;section&gt;</text>
  <rect x="50" y="220" width="110" height="35" fill="#16a34a" rx="4"/>
  <text x="105" y="242" font-family="monospace" font-size="10" fill="white" text-anchor="middle">&lt;figure&gt;</text>
  <rect x="180" y="220" width="110" height="35" fill="#16a34a" rx="4"/>
  <text x="235" y="242" font-family="monospace" font-size="10" fill="white" text-anchor="middle">&lt;time&gt;</text>

  <rect x="315" y="140" width="140" height="130" fill="#f59e0b" rx="6"/>
  <text x="385" y="165" font-family="monospace" font-size="12" fill="white" text-anchor="middle">&lt;aside&gt;</text>

  <rect x="25" y="290" width="430" height="60" fill="#6366f1" rx="6">
    <animate attributeName="opacity" values="1;0.7;1" dur="2.5s" repeatCount="indefinite"/>
  </rect>
  <text x="240" y="325" font-family="monospace" font-size="14" fill="white" text-anchor="middle">&lt;footer&gt;</text>
</svg>
</div>

> 💡 **Astuce mnémotechnique** : une page classique se lit du haut vers le bas comme une histoire — l'en-tête présente le site (`header`), la navigation guide (`nav`), le contenu principal informe (`main` → `article`/`section`), le contenu annexe complète (`aside`), et le pied de page conclut (`footer`).

<br/>

## 1️⃣ `<header>` — l'en-tête

```html
<header>
  <h1>Mon Blog de Voyage</h1>
  <p>Découvertes et carnets de route</p>
</header>
```

> 🧠 **À retenir** : `<header>` n'est pas réservé au haut de la page entière ! On peut en avoir **plusieurs**, un par `<article>` ou `<section>` (ex : l'en-tête d'un article de blog avec son titre et sa date).

<br/>

## 2️⃣ `<nav>` — la navigation

```html
<nav>
  <ul>
    <li><a href="#accueil">Accueil</a></li>
    <li><a href="#articles">Articles</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>
```

> ⚠️ **Piège fréquent** : tous les liens d'une page ne doivent pas être dans un `<nav>` — seulement les **blocs de liens de navigation principaux** (menu principal, fil d'Ariane, pagination). Un simple lien dans un paragraphe reste un `<a>` normal.

<br/>

## 3️⃣ `<main>` — le contenu principal

```html
<main>
  <!-- Le contenu unique de CETTE page, pas le menu ni le footer -->
</main>
```

> 🧠 **Règle stricte** : **un seul `<main>` par page**, jamais imbriqué dans un `<article>`, `<aside>`, `<header>`, `<footer>` ou `<nav>`. C'est la balise que les lecteurs d'écran utilisent pour "sauter directement au contenu" et ignorer les menus répétitifs.

<br/>

## 4️⃣ `<article>` vs `<section>` — la confusion n°1

<div align="center">
<svg width="500" height="160" viewBox="0 0 500 160" xmlns="http://www.w3.org/2000/svg">
  <rect x="20" y="20" width="220" height="120" fill="#22c55e" rx="8" opacity="0.85"/>
  <text x="130" y="50" font-family="monospace" font-size="13" fill="white" text-anchor="middle">&lt;article&gt;</text>
  <text x="130" y="80" font-family="Arial" font-size="11" fill="white" text-anchor="middle">Se suffit à lui-même</text>
  <text x="130" y="98" font-family="Arial" font-size="11" fill="white" text-anchor="middle">(article de blog, produit,</text>
  <text x="130" y="116" font-family="Arial" font-size="11" fill="white" text-anchor="middle">commentaire, tweet...)</text>

  <rect x="260" y="20" width="220" height="120" fill="#0ea5e9" rx="8" opacity="0.85"/>
  <text x="370" y="50" font-family="monospace" font-size="13" fill="white" text-anchor="middle">&lt;section&gt;</text>
  <text x="370" y="80" font-family="Arial" font-size="11" fill="white" text-anchor="middle">Regroupe un thème</text>
  <text x="370" y="98" font-family="Arial" font-size="11" fill="white" text-anchor="middle">(a besoin du contexte</text>
  <text x="370" y="116" font-family="Arial" font-size="11" fill="white" text-anchor="middle">de la page pour avoir un sens)</text>
</svg>
</div>

```html
<!-- article : autonome, aurait du sens même isolé et republié ailleurs -->
<article>
  <h2>10 conseils pour apprendre le CSS</h2>
  <p>Le CSS peut sembler difficile au début...</p>
</article>

<!-- section : regroupe un thème DANS le contexte de la page -->
<section>
  <h2>Nos formations</h2>
  <p>LingoLab Academy propose...</p>
</section>
```

| Question à se poser | Si oui → | Si non → |
|---|---|---|
| "Ce contenu aurait-il du sens tout seul, republié sur un autre site (flux RSS, réseau social) ?" | `<article>` | `<section>` |
| "Est-ce juste un regroupement thématique dans la page actuelle ?" | `<section>` | `<article>` |

> 💡 **Astuce pratique** : un `<article>` peut contenir des `<section>` (ex : un article long découpé en parties), et une `<section>` peut contenir plusieurs `<article>` (ex : une section "Derniers articles" qui liste plusieurs `<article>`).

<br/>

## 5️⃣ `<aside>` — le contenu annexe

```html
<aside>
  <h3>À propos de l'auteur</h3>
  <p>Dr. Chikh enseigne le développement web depuis...</p>
</aside>
```

> 🧠 Contenu **lié mais secondaire** au sujet principal : encadré "à propos", publicité, liens connexes, définitions dans la marge. Si on le supprimait, l'article principal resterait compréhensible.

<br/>

## 6️⃣ `<footer>` — le pied de page

```html
<footer>
  <p>&copy; 2026 LingoLab Academy. Tous droits réservés.</p>
  <nav>
    <a href="#mentions">Mentions légales</a>
    <a href="#contact">Contact</a>
  </nav>
</footer>
```

> Comme `<header>`, `<footer>` peut apparaître plusieurs fois : un footer global pour le site, et un footer local à l'intérieur d'un `<article>` (ex : nom de l'auteur, date de publication, tags).

<br/>

## 7️⃣ `<figure>` + `<figcaption>` — image avec légende

```html
<figure>
  <img src="diagramme-flexbox.png" alt="Schéma expliquant Flexbox">
  <figcaption>Fig. 1 — Les axes principal et secondaire en Flexbox</figcaption>
</figure>
```

> ✅ `<figure>` lie **sémantiquement** une image (ou un graphique, du code, une vidéo) à sa légende. Un simple `<img>` suivi d'un `<p>` n'exprime pas ce lien pour les technologies d'assistance.

<br/>

## 8️⃣ `<time>` — dates et heures lisibles par les machines

```html
<p>Publié le <time datetime="2026-07-04">4 juillet 2026</time></p>
```

> 🧠 L'attribut `datetime` (format ISO `AAAA-MM-JJ`) permet aux navigateurs et moteurs de recherche de **comprendre la date exactement**, même si le texte affiché est écrit en toutes lettres ou dans un format différent.

<br/>

## 9️⃣ `<mark>` et `<address>` — deux balises souvent oubliées

```html
<p>Le mot-clé à retenir est <mark>sémantique</mark>.</p>

<address>
  Écrit par <a href="mailto:contact@lingolab.dz">LingoLab Academy</a><br>
  Relizane, Algérie
</address>
```

| Balise | Sens |
|---|---|
| `<mark>` | Surligne un passage **pertinent dans le contexte actuel** (résultat de recherche, terme important) |
| `<address>` | Coordonnées de contact **de l'auteur du document ou de l'article**, pas n'importe quelle adresse postale citée dans le texte |

<br/>

## 📄 Exemple complet — une page assemblée

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>LingoLab Academy — Blog</title>
</head>
<body>

  <header>
    <h1>LingoLab Academy</h1>
    <nav>
      <ul>
        <li><a href="#accueil">Accueil</a></li>
        <li><a href="#blog">Blog</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <article>
      <header>
        <h2>Comprendre le Flexbox</h2>
        <p>Publié le <time datetime="2026-07-04">4 juillet 2026</time></p>
      </header>

      <section>
        <h3>Introduction</h3>
        <p>Flexbox est un modèle de mise en page...</p>
      </section>

      <figure>
        <img src="flexbox-demo.png" alt="Démonstration Flexbox">
        <figcaption>Les boîtes alignées avec Flexbox</figcaption>
      </figure>

      <footer>
        <p>Auteur : Dr. Chikh Amine</p>
      </footer>
    </article>

    <aside>
      <h3>Articles liés</h3>
      <ul>
        <li><a href="#">CSS Grid en 5 minutes</a></li>
      </ul>
    </aside>
  </main>

  <footer>
    <address>
      Contact : <a href="mailto:contact@lingolab.dz">contact@lingolab.dz</a>
    </address>
    <p>&copy; 2026 LingoLab Academy</p>
  </footer>

</body>
</html>
```

<br/>

## 🧪 Exercices pour les étudiants

1. Prends une page HTML que tu as construite uniquement avec des `<div>` et remplace chaque bloc par la balise sémantique correcte.
2. Construis une page "Portfolio" avec : un `<header>`, un `<nav>` à 3 liens, un `<main>` contenant 3 `<article>` (tes projets), un `<aside>` (tes compétences), et un `<footer>` avec tes réseaux sociaux.
3. Ajoute une `<figure>`/`<figcaption>` à chacun de tes projets.
4. Ajoute une balise `<time>` avec l'attribut `datetime` pour la date de création de chaque projet.
5. **Défi** : ouvre les outils de développement du navigateur → onglet Accessibilité → vérifie que ta page a bien un seul `<main>` et une structure de titres logique (`h1` → `h2` → `h3`).

<br/>

## 📌 Résumé express

| Je veux... | Balise |
|---|---|
| L'en-tête d'une page ou d'un article | `<header>` |
| Le menu de navigation principal | `<nav>` |
| Le contenu unique de la page (une seule fois) | `<main>` |
| Un contenu autonome, réutilisable ailleurs | `<article>` |
| Un regroupement thématique dans la page | `<section>` |
| Un contenu annexe, lié mais secondaire | `<aside>` |
| Le pied de page | `<footer>` |
| Une image avec sa légende | `<figure>` + `<figcaption>` |
| Une date lisible par les machines | `<time datetime="...">` |
| Surligner un terme pertinent | `<mark>` |
| Les coordonnées de l'auteur | `<address>` |

<br/>

<div align="center">

*LingoLab Academy © 2026 — Dr Chikh Mohamed Amine*

</div>