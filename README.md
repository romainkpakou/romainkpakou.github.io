# Portfolio — Romain Kpakou

**🔗 En ligne : [romainkpakou.github.io](https://romainkpakou.github.io)**

Portfolio professionnel de bioinformaticien & data scientist. Site statique en un seul
fichier HTML, sans framework ni dépendance de build, hébergé gratuitement sur GitHub Pages.

## Contenu du site

- **Présentation** — profil, approche, formation
- **Compétences** — pipelines NGS, bioinformatique structurale, data science & ML
- **Parcours** — timeline formation & expériences (2019 → 2026)
- **Projets** — sélection de projets appliqués, avec liens vers les dépôts GitHub concernés
- **Contact** — email, téléphone, LinkedIn, GitHub, CV téléchargeable

## Stack technique

- **HTML / CSS / JavaScript vanilla** — aucun framework, aucune dépendance
- **Polices** : Fraunces (display), Geist (texte), JetBrains Mono (mono) — via Google Fonts
- **Animations** : révélation au scroll (IntersectionObserver), transitions CSS pures
- **Accessibilité** : respecte `prefers-reduced-motion`, reste utilisable sans JavaScript
- **Responsive** : desktop, tablette, mobile

## Structure

```
.
├── index.html                       # Portfolio complet (structure, styles, script)
├── assets/
│   ├── cv/Romain_KPAKOU_CV.pdf      # CV téléchargeable depuis le site
│   └── img/
│       ├── README.md                # Comment ajouter une photo de profil
│       └── photo.jpg                # Optionnelle — initiales "RK" affichées par défaut si absente
└── README.md
```

## Mettre à jour le contenu

```bash
git clone https://github.com/romainkpakou/romainkpakou.github.io.git
cd romainkpakou.github.io
# éditer les fichiers...
git add .
git commit -m "Mise à jour du portfolio"
git push
```

Le site se redéploie automatiquement via GitHub Pages à chaque push sur `main` (1–2 minutes).

**Points d'entrée utiles dans `index.html` :**

| À modifier | Repère |
|---|---|
| Disponibilité | `hero-meta-item` (en-tête) et `contact-block-value` (section contact) |
| Chiffres clés ("À propos") | `const targets = [...]` dans le script en bas du fichier |
| Nouveau projet | dupliquer un `<article class="project-card">` dans `#projects` |
| CV | remplacer `assets/cv/Romain_KPAKOU_CV.pdf` (même nom de fichier) |
| Photo de profil | voir `assets/img/README.md` |

## Licence

Contenu personnel — libre d'usage et de modification pour Romain Kpakou.
