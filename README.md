# Portfolio — Romain Kpakou

Portfolio professionnel pour bioinformaticien & data scientist.
Site statique, un seul fichier HTML, sans framework. Hébergeable gratuitement sur GitHub Pages.

---

## 📁 Structure du dossier

```
portfolio_site/
├── index.html              # Le portfolio (fichier principal)
├── README.md               # Ce fichier — guide de déploiement
├── .gitignore              # Fichiers à exclure de Git
└── assets/
    ├── cv/
    │   └── Romain_KPAKOU_CV.pdf   # CV téléchargeable depuis le site
    └── img/
        ├── README.md              # Comment ajouter votre photo
        └── photo.jpg              # ← À ajouter (optionnel, sinon initiales par défaut)
```

---

## 🚀 Déploiement sur GitHub Pages — méthode recommandée pour débutant

Cette méthode utilise uniquement l'interface web GitHub. Aucune commande Git à taper.

### Étape 1 — Créer le dépôt GitHub

1. Connectez-vous sur [github.com](https://github.com)
2. Cliquez sur le bouton vert **"New"** en haut à droite (ou allez sur [github.com/new](https://github.com/new))
3. Dans **"Repository name"**, tapez exactement : `votre-username.github.io`
   (remplacez `votre-username` par votre vrai nom d'utilisateur GitHub — par exemple `romainkpakou.github.io`)

   > ⚠️ Ce nom est important : c'est ce qui rend votre site accessible automatiquement à l'adresse `https://votre-username.github.io`

4. Laissez le dépôt en **"Public"** (obligatoire pour la version gratuite de GitHub Pages)
5. **Ne cochez pas** "Add a README file" (vous en avez déjà un)
6. Cliquez sur **"Create repository"**

### Étape 2 — Uploader vos fichiers

Sur la page de votre nouveau dépôt vide, vous verrez un lien **"uploading an existing file"** au milieu. Cliquez dessus.

1. **Glissez-déposez le contenu** du dossier `portfolio_site/` dans la zone de drop
   (le fichier `index.html`, le dossier `assets/`, le `README.md`, etc.)
2. ⚠️ **Important** : glissez le **contenu** du dossier, pas le dossier lui-même.
   Si vous glissez le dossier entier, le site sera dans un sous-dossier et ne fonctionnera pas.
3. En bas de la page, dans **"Commit changes"**, laissez le message par défaut ou tapez `Initial commit`
4. Cliquez sur **"Commit changes"**

### Étape 3 — Activer GitHub Pages

1. Sur la page de votre dépôt, cliquez sur l'onglet **"Settings"** (en haut à droite)
2. Dans le menu de gauche, cliquez sur **"Pages"**
3. Sous **"Source"**, sélectionnez la branche **"main"** dans le menu déroulant
4. Laissez le dossier sur `/ (root)`
5. Cliquez sur **"Save"**

### Étape 4 — Patientez quelques minutes

Le déploiement prend 1 à 5 minutes. Rafraîchissez la page Settings/Pages.
Quand c'est prêt, vous verrez un message vert :

> ✅ Your site is live at `https://votre-username.github.io/`

Cliquez sur le lien — votre portfolio est en ligne ! 🎉

---

## 🔄 Mettre à jour le site plus tard

Pour modifier votre portfolio (ajouter un projet, changer un texte, mettre à jour le CV) :

### Option A — Édition en ligne (la plus simple)

1. Allez sur votre dépôt GitHub
2. Cliquez sur le fichier que vous voulez modifier (`index.html` par exemple)
3. Cliquez sur l'icône crayon ✏️ en haut à droite
4. Modifiez le texte directement dans le navigateur
5. En bas, cliquez sur **"Commit changes"**
6. Le site se met à jour tout seul en 1-2 minutes

### Option B — Remplacer un fichier (CV par exemple)

1. Allez dans le dossier `assets/cv/` sur GitHub
2. Cliquez sur le fichier `Romain_KPAKOU_CV.pdf`
3. Cliquez sur l'icône poubelle 🗑️ pour le supprimer
4. Validez la suppression avec **"Commit changes"**
5. Retournez dans `assets/cv/` et cliquez sur **"Add file"** → **"Upload files"**
6. Glissez votre nouveau PDF (en gardant le même nom : `Romain_KPAKOU_CV.pdf`)
7. Validez avec **"Commit changes"**

---

## 📸 Ajouter votre photo de profil

Le portfolio affiche par défaut vos initiales **"RK"** en élégant italique.
Vous pouvez les remplacer par une vraie photo :

1. Préparez une photo carrée ou portrait (au moins 800x1000 px, format JPG)
2. Renommez-la exactement : `photo.jpg`
3. Uploadez-la dans le dossier `assets/img/` de votre dépôt GitHub :
   - Allez dans `assets/img/` sur GitHub
   - Cliquez **"Add file"** → **"Upload files"**
   - Glissez votre `photo.jpg`
   - Validez avec **"Commit changes"**

C'est tout — la photo apparaîtra automatiquement à la place des initiales.
Si la photo est absente ou mal nommée, les initiales restent affichées (pas d'image cassée).

---

## ✏️ Personnalisations à faire dans `index.html`

Cherchez ces éléments dans le fichier (Ctrl+F dans l'éditeur GitHub) :

### 1. Lien LinkedIn

Cherchez : `id="linkedin-link"`
Vous verrez : `<a href="#" class="contact-channel" id="linkedin-link">`
Remplacez `href="#"` par votre vraie URL :
`<a href="https://linkedin.com/in/votre-profil" target="_blank" class="contact-channel" id="linkedin-link">`

### 2. Lien GitHub

Cherchez : `id="github-link"`
Même principe — remplacez `href="#"` par `https://github.com/votre-username`

### 3. Mettre à jour la date / l'âge des stats

Si vous voulez modifier les chiffres "3 stages, 7+ projets, 284 patients" affichés dans la section "À propos",
cherchez `targets = ['3', '7+', '284']` dans le script en bas du fichier et changez les valeurs.

---

## 🎨 Design & technologies

- **Aucun framework** — HTML/CSS/JavaScript vanilla
- **Polices** : Fraunces (display), Geist (texte), JetBrains Mono (mono) — chargées via Google Fonts
- **Responsive** — fonctionne sur desktop, tablette, mobile
- **Animations** — entrée au scroll via IntersectionObserver, animations CSS pures
- **Fonctionne sans JavaScript** — le contenu reste accessible (les animations seules sont désactivées)
- **Accessibilité** — respecte `prefers-reduced-motion` pour les utilisateurs sensibles aux animations

---

## 🔧 Pour aller plus loin (méthode Git en ligne de commande)

Quand vous serez plus à l'aise avec Git, voici les commandes équivalentes au déploiement :

```bash
# Cloner votre dépôt
git clone https://github.com/votre-username/votre-username.github.io.git
cd votre-username.github.io

# Modifier les fichiers localement avec votre éditeur préféré...

# Puis pousser les changements
git add .
git commit -m "Mise à jour du portfolio"
git push
```

Pour configurer Git la première fois :
```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@example.com"
```

---

## 🌐 Domaine personnalisé (optionnel)

Si plus tard vous achetez un domaine (ex: `romain-kpakou.fr` chez Gandi pour ~12€/an), vous pourrez le pointer vers GitHub Pages depuis l'onglet Settings → Pages → Custom domain. GitHub vous fournit aussi un certificat HTTPS gratuit.

---

## 📝 Licence

Code du portfolio personnel — libre d'usage et de modification pour Romain Kpakou.
