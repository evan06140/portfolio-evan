# Evan Arbajian — Portfolio wedding planner

Site portfolio d’une seule page pour **Evan Arbajian**, futur wedding planner basé à Vence (Côte d’Azur), à la recherche d’un poste d’assistant wedding planner.

- 100 % HTML/CSS : aucun JavaScript, aucune installation, aucun outil à compiler
- Tons crème, doré et blanc, typographie Cormorant Garamond + Jost
- Adapté au mobile, à la tablette et à l’ordinateur (menu plein écran sur mobile)
- Sections : Accueil · À propos · Portfolio · Compétences · Contact (Instagram)

---

## Structure des fichiers

```
portfolio-evan/
├── index.html              ← tout le contenu du site (textes, liens, photos)
├── css/
│   └── style.css           ← la mise en forme (couleurs, polices, mise en page)
├── images/
│   ├── accueil.jpg         ← photo en arche de l’accueil
│   ├── portrait.jpg        ← portrait de la section « À propos »
│   └── portfolio/
│       ├── photo-1.jpg     ← photos de la galerie « Portfolio »
│       ├── …
│       └── photo-6.jpg
├── favicon.svg             ← petite icône « EA » de l’onglet du navigateur
└── README.md
```

## Voir le site sur son ordinateur

Double-cliquez sur `index.html` : le site s’ouvre dans votre navigateur. Rien d’autre à installer.

---

## Remplacer les photos

Les images fournies sont des **emplacements temporaires** (on y lit « Remplacez ce fichier par votre photo »). Pour mettre vos photos, il suffit de **remplacer chaque fichier par une photo portant exactement le même nom** : aucun code à modifier.

| Emplacement sur le site | Fichier à remplacer | Format conseillé |
|---|---|---|
| Accueil (photo en arche) | `images/accueil.jpg` | vertical, ~1200 × 1500 px |
| À propos (votre portrait) | `images/portrait.jpg` | vertical, ~1200 × 1500 px |
| Portfolio, grande photo haute | `images/portfolio/photo-1.jpg` | vertical, ~1200 × 1500 px |
| Portfolio, photos 2 à 6 | `images/portfolio/photo-2.jpg` … `photo-6.jpg` | horizontal, ~1600 px de large |

Les photos sont recadrées automatiquement pour remplir leur cadre : gardez le sujet principal plutôt au centre.

**Directement sur GitHub (sans rien installer) :**

1. Ouvrez le dossier `images/portfolio` (ou `images`) de votre dépôt sur github.com.
2. Cliquez sur **Add file → Upload files**.
3. Glissez vos photos, **renommées à l’identique** (`photo-1.jpg`, `photo-2.jpg`…).
4. Cliquez sur **Commit changes** : les anciennes images sont remplacées.

**Conseils :**

- Le nom doit être **identique, en minuscules**, avec l’extension `.jpg` (`Photo-1.JPG` ou `photo-1.jpeg` ne fonctionneront pas en ligne).
- Les photos d’iPhone au format HEIC doivent être converties en JPG (ou exportées en « Le plus compatible »).
- Allégez vos photos (moins de 500 Ko chacune) avec un outil gratuit comme [squoosh.app](https://squoosh.app) : le site restera rapide sur mobile.
- Pensez à adapter la **légende** (`<figcaption>`) et la **description** (`alt="…"`) de chaque photo dans `index.html` : la description est lue par les lecteurs d’écran et aide le référencement.

**Ajouter des photos à la galerie :** dans `index.html`, copiez un bloc `<figure class="gallery__item reveal"> … </figure>`, collez-le à la suite et changez le numéro (`photo-7.jpg`, etc.). La mosaïque se répète toutes les 6 photos : ajoutez-les de préférence par 6 pour un rendu parfaitement harmonieux.

## Modifier les textes et les liens

Tout le contenu se trouve dans `index.html`. Chaque section est signalée par un repère en commentaire (`ACCUEIL`, `À PROPOS`, `PORTFOLIO`, `COMPÉTENCES`, `CONTACT`). Sur GitHub, ouvrez le fichier, cliquez sur l’icône **crayon** (Edit), faites vos modifications puis **Commit changes**.

- **Instagram** : le lien `https://www.instagram.com/evan.arbajian.events/` apparaît deux fois (portfolio et contact).
- **Ajouter une adresse e-mail** : dans la section Contact, une ligne prête à l’emploi est en commentaire. Retirez `<!--` et `-->` autour de cette ligne et remplacez `votre.adresse@email.fr` (2 fois).

## Changer les couleurs

En haut de `css/style.css`, la section **« 1. Réglages »** regroupe toutes les couleurs (`--cream`, `--gold`, `--ink`…). Modifiez une valeur : elle change sur tout le site.

---

## Mettre le site en ligne gratuitement avec GitHub Pages

GitHub Pages héberge gratuitement les sites HTML/CSS directement depuis votre dépôt.

### 1. Vérifier que le dépôt est public

GitHub Pages est gratuit pour les dépôts **publics**. Dans **Settings → General**, tout en bas (*Danger Zone*), vérifiez que le dépôt est public, sinon cliquez sur **Change visibility → Make public**.

### 2. Mettre les fichiers sur la branche `main`

Si le site se trouve sur une autre branche (par exemple une branche de travail), fusionnez-la dans `main` : onglet **Pull requests → New pull request**, choisissez la branche du site, puis **Create pull request** et **Merge pull request**.

> Le fichier `index.html` doit se trouver **à la racine** du dépôt (c’est déjà le cas).

### 3. Activer GitHub Pages

1. Sur la page du dépôt, cliquez sur **Settings** (Paramètres).
2. Dans le menu de gauche, cliquez sur **Pages**.
3. Dans **Build and deployment → Source**, choisissez **Deploy from a branch**.
4. Dans **Branch**, sélectionnez **`main`** et le dossier **`/ (root)`**, puis cliquez sur **Save**.

### 4. Ouvrir le site

Après 1 à 2 minutes, l’adresse du site s’affiche en haut de la page **Settings → Pages** :

```
https://evan06140.github.io/portfolio-evan/
```

Vous pouvez suivre la publication dans l’onglet **Actions** (une coche verte = site en ligne).

### Mettre à jour le site

Chaque modification enregistrée sur la branche `main` (nouvelle photo, texte corrigé…) est **publiée automatiquement** en 1 à 2 minutes. Si vous ne voyez pas le changement, rechargez la page en vidant le cache (`Ctrl + F5` sur ordinateur, ou fermez/rouvrez l’onglet sur mobile).

### Options

- **Adresse plus courte** : renommez le dépôt en `evan06140.github.io` (**Settings → General → Repository name**) ; le site sera alors accessible à `https://evan06140.github.io`.
- **Nom de domaine personnalisé** (ex. `evan-arbajian.fr`, payant auprès d’un registraire) : renseignez-le dans **Settings → Pages → Custom domain** et suivez les instructions de GitHub pour la configuration DNS. Cochez ensuite **Enforce HTTPS**.

### En cas de problème

| Problème | Solution |
|---|---|
| Erreur 404 | Attendez quelques minutes ; vérifiez que `index.html` est à la racine de la branche choisie dans Settings → Pages. |
| Une photo ne s’affiche pas | Vérifiez le nom exact du fichier (majuscules, `.jpg` et non `.jpeg`/`.JPG`/`.heic`). |
| Le site n’a pas changé | Attendez 1 à 2 minutes, regardez l’onglet Actions, puis rechargez sans cache. |
