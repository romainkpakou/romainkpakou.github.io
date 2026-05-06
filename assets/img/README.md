# Photo de profil

Pour afficher votre photo dans le portfolio, ajoutez ici un fichier nommé exactement :

**`photo.jpg`**

## Recommandations

- **Format** : JPG (le PNG fonctionne aussi mais sera plus lourd)
- **Dimensions minimum** : 800 × 1000 pixels (ratio portrait 4:5 idéal)
- **Poids** : idéalement < 500 Ko (utilisez [tinyjpg.com](https://tinyjpg.com) pour compresser)
- **Cadrage** : visage centré dans le tiers supérieur de l'image
- **Style** : photo professionnelle nette, fond neutre

## Pas de photo ?

Aucun problème — si le fichier `photo.jpg` est absent, le portfolio affiche élégamment vos initiales **"RK"** à la place. Pas d'image cassée, pas d'icône d'erreur.

## Comment changer le rendu de la photo

La photo est légèrement désaturée et contrastée par défaut (effet éditorial sobre). Si vous préférez un rendu différent, modifiez la propriété `filter` de `.portrait-photo` dans `index.html` :

```css
/* Style actuel — léger noir et blanc, contraste augmenté */
filter: grayscale(15%) contrast(1.05);

/* Pour un rendu naturel sans effet */
filter: none;

/* Pour un rendu très sombre/dramatique */
filter: grayscale(40%) contrast(1.15) brightness(0.92);
```
