# romainkpakou.github.io

**🔗 En ligne : [romainkpakou.github.io](https://romainkpakou.github.io)**

Portfolio professionnel de bioinformaticien & data scientist.

## Ce repo

Ce repo contient l'**export statique buildé** du portfolio, publié directement par GitHub
Pages. Ce n'est plus le code source à modifier.

Le code source (Next.js + TypeScript + Tailwind + shadcn/ui + Framer Motion) vit dans un
projet séparé. Pour mettre à jour le contenu du site :

1. Modifier le contenu dans `src/lib/content.ts` du projet source (profil, compétences,
   parcours, projets).
2. Builder l'export statique :
   ```bash
   STATIC_EXPORT=true npm run build
   ```
3. Copier le contenu généré dans `out/` vers ce repo (en écrasant tout sauf `.git`) :
   ```bash
   rm -rf assets index.html robots.txt sitemap.xml _next cv img rapports \
         404.html favicon.ico _not-found* __next* index.txt .nojekyll
   cp -a <chemin-vers-projet-source>/out/. .
   ```
4. Committer et pousser sur `main` — GitHub Pages republie automatiquement (1–2 minutes).

## Point technique important : `.nojekyll`

GitHub Pages traite les fichiers par **Jekyll** par défaut, qui **ignore tout ce qui
commence par `_`** — ce qui supprimerait le dossier `_next/` (tout le CSS/JS de
l'application) du site publié. Le fichier `.nojekyll` à la racine désactive ce
traitement. **Il doit toujours être présent** après chaque republication.

## Sécurité

Les headers HTTP de sécurité (CSP, HSTS, etc.) sont définis dans le projet source mais
**ne s'appliquent pas ici** : GitHub Pages sert des fichiers statiques bruts, sans passer
par un serveur Next.js capable de les émettre. Choix assumé : le site est 100% statique,
sans formulaire ni donnée sensible — la surface d'attaque réelle reste minime.
