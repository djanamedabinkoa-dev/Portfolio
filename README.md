# Portfolio — Dabinkoa DJANAME

Site portfolio d'architecture (HTML / CSS / JS, sans framework), prêt pour **GitHub Pages**.
Il reprend le portfolio PDF de novembre 2026 : Les Bulles d'Assilah, le Centre d'oncologie (Agdal) et l'Immeuble résidentiel, avec la même identité (fond pierre, arches caramel / brun / sauge, titres en Cormorant).

## Contenu du dossier

```
index.html      → textes et structure du site
style.css       → couleurs, typographies, mise en page
script.js       → menu mobile, visionneuse d'images, animations
images/         → rendus et planches (JPG optimisés pour le web)
portfolio.pdf   → le portfolio PDF complet (version allégée, 17 Mo), téléchargeable depuis Contact
```

## Mettre à jour le site sur GitHub

Le dépôt est déjà configuré (Settings → Pages → branche `main`, dossier `/ (root)`). Il suffit de remplacer les fichiers :

1. Dans le dépôt, supprime l'ancien dossier `images/` (il contient les images de l'ancienne version).
   Sur github.com : ouvre `images/`, menu `…` en haut à droite → *Delete directory* → *Commit changes*.
2. *Add file → Upload files* : glisse **le contenu** du dossier (index.html, style.css, script.js, README.md, portfolio.pdf et le dossier images), puis *Commit changes*.
   ⚠️ `index.html` doit être **à la racine** du dépôt, pas dans un sous-dossier.
3. Attends 1 à 2 minutes (onglet *Actions* : coche verte), puis recharge le site.
   Si l'ancienne version s'affiche encore, fais Ctrl + F5 (ou Cmd + Shift + R sur Mac).

Avec Git :
```bash
git rm -r images
git add .
git commit -m "Nouvelle version du portfolio"
git push
```

## À compléter

Dans `index.html`, section **Contact** (vers la fin du fichier) :
- remplace `ton.email@exemple.com` (2 fois) par l'adresse email ;
- remplace `https://www.linkedin.com/in/ton-profil` et `linkedin.com/in/ton-profil` par le profil LinkedIn (ou supprime ce bloc `<a>…</a>`).

## Modifier le site

- **Textes** : directement dans `index.html` (sections `#assilah`, `#oncologie`, `#immeuble`).
- **Ajouter une image** : place le JPG dans `images/` puis copie une ligne de la galerie :
  ```html
  <button class="zoom" data-src="images/mon-image.jpg" data-caption="Légende"><img src="images/mon-image.jpg" alt="Description" loading="lazy"></button>
  ```
  Ajoute `wide` à la classe pour une image sur deux colonnes. Chaque galerie est prévue pour 3 images larges + 3 normales.
  Garde les images sous ~300 Ko (largeur 1600 px, qualité 80).
- **Couleurs** : en haut de `style.css` (`--caramel`, `--brown`, `--sage`, `--paper`).

## Tester en local

Ouvre `index.html` dans un navigateur. Les polices (Cormorant Garamond, Inter) viennent de Google Fonts et s'affichent dès qu'il y a une connexion internet.
