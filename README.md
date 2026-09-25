# Portfolio – Maho Vidal

Portfolio professionnel réalisé dans le cadre du **BTS SIO option SISR** (Solutions
d'Infrastructure, Systèmes et Réseaux) au lycée Saint-Michel d'Annecy, en vue de
l'épreuve E5.

## Contenu du site

| Rubrique | Objet |
| --- | --- |
| Présentation | Identité, formation, coordonnées |
| Compétences | Les trois blocs du référentiel SISR et les technologies maîtrisées |
| Réalisations | Huit réalisations professionnelles détaillées (contexte, travail, technologies) |
| Tableau de synthèse | Correspondance réalisations / compétences du référentiel |
| Parcours | Formation et expérience professionnelle |
| Veille technologique | Thème retenu, démarche et sources |
| Contact | Coordonnées et formulaire d'envoi de message |

## Technique

Site statique, écrit à la main, sans framework ni étape de compilation.

- **HTML5 sémantique** : `header`, `main`, `section`, `article`, `footer`, listes de
  définitions, `scope` sur les en-têtes de tableau.
- **CSS3** : palette centralisée en variables CSS (`:root`), mise en page en Flexbox et
  Grid, adaptation aux petits écrans par media queries, feuille d'impression.
- **Accessibilité** : lien d'évitement clavier, focus visible, `prefers-reduced-motion`,
  contrastes conformes au niveau AA.
- **JavaScript natif** (aucune bibliothèque) : apparition des sections au défilement,
  surlignage du lien de navigation actif, envoi du formulaire de contact sans
  rechargement de page.

Le formulaire de contact est relayé par le service [FormSubmit](https://formsubmit.co),
le site étant statique et donc dépourvu de traitement côté serveur.

## Fichiers

```
index.html       Page unique du portfolio
styles.css       Feuille de styles
VIDAL_Maho.jpg   Photo de profil
CV_BTS_SIO.pdf   Curriculum vitae téléchargeable
```

## Consultation en local

Le formulaire de contact nécessite d'être servi en HTTP (un navigateur bloque les
requêtes réseau depuis un fichier ouvert en `file://`) :

```bash
python -m http.server 8000
```

Puis ouvrir <http://localhost:8000>.
