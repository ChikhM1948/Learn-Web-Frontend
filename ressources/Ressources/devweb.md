<!--
  📘 GUIDE ANIMÉ — RESSOURCES POUR APPRENDRE LE DÉVELOPPEMENT WEB
  HTML + CSS intégré pour des cartes animées au survol.
  ⚠️ Rendu : ouvre en Aperçu VS Code (Ctrl+Shift+V), Obsidian ou Typora
  pour voir les animations. Sur github.com, seuls le texte et les liens
  s'afficheront (les <style> sont filtrés par sécurité).
-->

<div align="center">

# 🚀 RESSOURCES DEV WEB
### La boîte à outils complète pour apprendre à coder — sites, cours, chaînes YouTube

![Web Dev](https://img.shields.io/badge/Web-Development-38B2AC?style=for-the-badge&logo=htmx)
![Gratuit](https://img.shields.io/badge/100%25-Gratuit%20ou%20Freemium-orange?style=for-the-badge)
![2026](https://img.shields.io/badge/Mis%20à%20jour-2026-blueviolet?style=for-the-badge)

</div>

---

<div>
<style>
.card-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
  margin: 16px 0;
}
.res-card {
  flex: 1 1 260px;
  background: #1e293b;
  border-radius: 12px;
  padding: 18px;
  color: #e2e8f0;
  border: 1px solid #334155;
  transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
}
.res-card:hover {
  transform: translateY(-6px) scale(1.02);
  border-color: #38bdf8;
  box-shadow: 0 10px 24px -8px #38bdf8aa;
}
.res-card h4 { margin: 0 0 6px; color: #38bdf8; }
.res-card p  { margin: 0; font-size: 13px; color: #94a3b8; }
.res-card a  { color: #f472b6; text-decoration: none; font-weight: 600; }
.pulse-badge {
  display: inline-block;
  background: #ef4444;
  color: white;
  font-size: 11px;
  padding: 2px 8px;
  border-radius: 100px;
  margin-left: 6px;
  animation: pulse 1.6s infinite;
}
@keyframes pulse {
  0%   { opacity: 1;   transform: scale(1); }
  50%  { opacity: 0.6; transform: scale(1.1); }
  100% { opacity: 1;   transform: scale(1); }
}
.progress-track {
  background: #1e293b;
  border-radius: 100px;
  height: 14px;
  overflow: hidden;
  margin: 6px 0 14px;
}
.progress-fill {
  height: 100%;
  border-radius: 100px;
  background: linear-gradient(90deg,#38bdf8,#818cf8);
  animation: grow-fill 2.5s ease-out forwards;
}
@keyframes grow-fill { from { width: 0%; } }
</style>
</div>

## 🗺️ 1. Par où commencer — la feuille de route

<div>
<p style="font-size:13px;color:#64748b;margin-bottom:2px;">HTML &amp; CSS (fondations)</p>
<div class="progress-track"><div class="progress-fill" style="width:100%;"></div></div>
<p style="font-size:13px;color:#64748b;margin-bottom:2px;">JavaScript (logique &amp; interactivité)</p>
<div class="progress-track"><div class="progress-fill" style="width:80%;"></div></div>
<p style="font-size:13px;color:#64748b;margin-bottom:2px;">Framework (React / Vue) + Git</p>
<div class="progress-track"><div class="progress-fill" style="width:55%;"></div></div>
<p style="font-size:13px;color:#64748b;margin-bottom:2px;">Back-end (Node.js, bases de données)</p>
<div class="progress-track"><div class="progress-fill" style="width:30%;"></div></div>
</div>

Pour une carte interactive complète du parcours (avec toutes les branches : frontend, backend, DevOps, mobile...), utilise **roadmap.sh** — la référence visuelle gratuite. <https://roadmap.sh>

---

## 📚 2. Sites & plateformes pour apprendre

<div class="card-grid">

<div class="res-card">
<h4>MDN Web Docs <span class="pulse-badge">RÉFÉRENCE</span></h4>
<p>La documentation officielle HTML/CSS/JS, tenue par Mozilla. À consulter à chaque doute sur une propriété.</p>
<a href="https://developer.mozilla.org/fr/">developer.mozilla.org</a>
</div>

<div class="res-card">
<h4>freeCodeCamp</h4>
<p>Curriculum complet et gratuit, certificats à la clé (Responsive Design, JS Algorithms, React...).</p>
<a href="https://www.freecodecamp.org/">freecodecamp.org</a>
</div>

<div class="res-card">
<h4>The Odin Project</h4>
<p>Parcours full-stack open-source, projets concrets, communauté active. Excellent pour la rigueur.</p>
<a href="https://www.theodinproject.com/">theodinproject.com</a>
</div>

<div class="res-card">
<h4>roadmap.sh</h4>
<p>Feuilles de route visuelles et interactives pour chaque spécialité (frontend, backend, DevOps...).</p>
<a href="https://roadmap.sh/">roadmap.sh</a>
</div>

<div class="res-card">
<h4>W3Schools</h4>
<p>Références rapides + éditeur en ligne pour tester du code instantanément. Idéal pour débuter.</p>
<a href="https://www.w3schools.com/">w3schools.com</a>
</div>

<div class="res-card">
<h4>CSS-Tricks</h4>
<p>Articles de référence sur CSS moderne (Grid, Flexbox, animations). Guides très visuels.</p>
<a href="https://css-tricks.com/">css-tricks.com</a>
</div>

<div class="res-card">
<h4>Frontend Mentor</h4>
<p>Maquettes réelles (Figma/JPG) à coder toi-même — parfait pour construire un portfolio.</p>
<a href="https://www.frontendmentor.io/">frontendmentor.io</a>
</div>

<div class="res-card">
<h4>JavaScript.info</h4>
<p>Le cours JS le plus complet et le mieux écrit, du niveau débutant à avancé.</p>
<a href="https://javascript.info/">javascript.info</a>
</div>

</div>

### 🇫🇷 En français

<div class="card-grid">

<div class="res-card">
<h4>Grafikart</h4>
<p>LA référence francophone : tutos vidéo + articles sur HTML/CSS, JS, PHP, Symfony, Laravel...</p>
<a href="https://grafikart.fr/">grafikart.fr</a>
</div>

<div class="res-card">
<h4>OpenClassrooms</h4>
<p>Plus de 600 cours gratuits, dont plusieurs parcours complets "Développeur Web" avec quiz et exercices.</p>
<a href="https://openclassrooms.com/">openclassrooms.com</a>
</div>

</div>

---

## 🎬 3. Chaînes YouTube incontournables (2026)

<div class="card-grid">

<div class="res-card">
<h4>freeCodeCamp.org</h4>
<p>Cours complets de plusieurs heures, structurés comme de vrais bootcamps — 100% gratuit.</p>
<a href="https://www.youtube.com/@freecodecamp">@freecodecamp</a>
</div>

<div class="res-card">
<h4>Kevin Powell</h4>
<p>LA référence CSS. Flexbox, Grid, responsive, accessibilité — clarté et précision inégalées.</p>
<a href="https://www.youtube.com/@KevinPowell">@KevinPowell</a>
</div>

<div class="res-card">
<h4>Web Dev Simplified</h4>
<p>Kyle Cook explique un concept à la fois (JS, React) avec une clarté redoutable.</p>
<a href="https://www.youtube.com/@WebDevSimplified">@WebDevSimplified</a>
</div>

<div class="res-card">
<h4>Traversy Media</h4>
<p>Crash courses et projets complets : HTML/CSS/JS, React, Node.js, MERN stack.</p>
<a href="https://www.youtube.com/@TraversyMedia">@TraversyMedia</a>
</div>

<div class="res-card">
<h4>The Net Ninja</h4>
<p>Playlists séquentielles très méthodiques : React 19, Next.js, Node/Express, Firebase.</p>
<a href="https://www.youtube.com/@NetNinja">@NetNinja</a>
</div>

<div class="res-card">
<h4>Fireship</h4>
<p>Explications ultra-rapides et denses (100 secondes de code) pour rester à jour sans perdre de temps.</p>
<a href="https://www.youtube.com/@Fireship">@Fireship</a>
</div>

</div>

### 🇫🇷 Chaînes francophones

<div class="card-grid">

<div class="res-card">
<h4>Grafikart (YouTube)</h4>
<p>Le pendant vidéo du site — HTML, CSS, JS, PHP, Symfony expliqués en français, clairement.</p>
<a href="https://www.youtube.com/@Grafikart">@Grafikart</a>
</div>

<div class="res-card">
<h4>HTeuMeuLeu</h4>
<p>Contenu francophone pointu sur l'accessibilité web et le CSS moderne.</p>
<a href="https://www.youtube.com/@hteumeuleu">@hteumeuleu</a>
</div>

</div>

---

## 🛠️ 4. Outils pratiques pour progresser

<div class="card-grid">

<div class="res-card">
<h4>CodePen / CodeSandbox</h4>
<p>Bac à sable en ligne pour tester du HTML/CSS/JS instantanément, sans installation.</p>
<a href="https://codepen.io/">codepen.io</a>
</div>

<div class="res-card">
<h4>Flexbox Froggy / Grid Garden</h4>
<p>Jeux pédagogiques pour maîtriser Flexbox et Grid en s'amusant — parfait pour tes étudiants.</p>
<a href="https://flexboxfroggy.com/">flexboxfroggy.com</a>
</div>

<div class="res-card">
<h4>Can I Use</h4>
<p>Vérifie la compatibilité d'une propriété CSS/API JS avec les navigateurs avant de l'utiliser.</p>
<a href="https://caniuse.com/">caniuse.com</a>
</div>

<div class="res-card">
<h4>GitHub</h4>
<p>Héberge ton code, construis un portfolio public, contribue à des projets open-source.</p>
<a href="https://github.com/">github.com</a>
</div>

</div>

---

## 📅 5. Plan d'étude suggéré (12 semaines)

| Semaines | Focus | Ressource principale |
|---|---|---|
| 1–2 | HTML sémantique + CSS de base | MDN + Grafikart |
| 3–4 | Flexbox & Grid | Kevin Powell + Flexbox Froggy |
| 5–6 | JavaScript fondamentaux | JavaScript.info + Web Dev Simplified |
| 7–8 | DOM, événements, fetch/API | freeCodeCamp |
| 9–10 | Git/GitHub + un framework (React) | The Net Ninja |
| 11 | Projet portfolio | Frontend Mentor |
| 12 | Révisions + mise en ligne | GitHub Pages / Vercel |

---

## ✏️ 6. Conseils pour tes étudiants

1. **Un concept, un exercice.** Ne pas accumuler les tutoriels sans coder soi-même.
2. **Reproduire puis modifier.** Copier un projet, puis changer une fonctionnalité pour vraiment comprendre.
3. **Documenter ses erreurs.** Un carnet de bugs résolus vaut plus que 10 heures de vidéos passives.
4. **Construire un portfolio dès le premier mois.** Même 2-3 projets simples suffisent pour démarrer.
5. **Une seule chaîne YouTube à la fois par sujet** — évite l'éparpillement entre trop de formats.

---

<div align="center">

💡 **Astuce prof** : ouvre ce fichier en Aperçu VS Code (`Ctrl+Shift+V`) pour voir
les cartes s'animer au survol pendant la présentation en cours.

Made with 💙 for **LingoLab Academy**

</div>