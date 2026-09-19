# Site TRUFALINO

Site vitrine statique de TRUFALINO — entreprise familiale lorraine
dédiée à la mise en valeur de la truffe.

## Contenu

```
trufalino-site/
├── index.html              page unique (2 sections : contact, qui sommes-nous)
├── assets/
│   ├── logo-mot.png        mot-symbole seul, transparent (bandeau)
│   ├── logo-complet.png    illustration + mot-symbole, transparent
│   └── logo-complet-creme.png
└── README.md
```

Aucune dépendance, aucun build, aucun framework. Un seul fichier HTML
contenant sa propre feuille de style. Seule ressource externe : les polices
Google Fonts (Cormorant Garamond, Inter), chargées par CDN.

## Visualiser en local

```bash
cd trufalino-site
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```

Ouvrir `index.html` directement dans le navigateur fonctionne aussi.

## Mettre en ligne

Le site étant entièrement statique, n'importe quel hébergeur convient.

**GitHub Pages** — gratuit, adapté à une démonstration
1. Créer un dépôt, y pousser le contenu de ce dossier
2. Settings → Pages → Source : branche `main`, dossier `/root`
3. Le site est publié sur `https://<utilisateur>.github.io/<depot>/`

**Netlify** — gratuit, glisser-déposer du dossier sur app.netlify.com/drop

**Hébergeur classique** — déposer le dossier en FTP à la racine web.

### Nom de domaine

Pour un usage professionnel, un domaine propre (`trufalino.fr`) doit être
enregistré **au nom de l'entreprise**, pas d'un tiers. Compter 10 à 15 €/an
chez un registrar français (OVH, Gandi, Infomaniak).

## Technique

- Page unique, navigation par ancres
- Mise en page en flexbox, unités relatives, adaptation mobile
- Thème clair / sombre automatique selon la préférence du système
  (`prefers-color-scheme`), avec variables CSS
- Prise en compte des encoches d'écran (`env(safe-area-inset-*)`)
- Mesure de ligne limitée à 62 caractères pour le confort de lecture

### Personnalisation rapide

Les couleurs sont définies en variables CSS dans `:root` :

| Variable     | Rôle                          |
|--------------|-------------------------------|
| `--bg`       | fond de page                  |
| `--ink`      | texte courant                 |
| `--ink-fort` | titres                        |
| `--or`       | accent doré                   |
| `--line`     | filets et séparateurs         |

## Contenu et responsabilité

Les informations publiées (coordonnées, description de l'activité) engagent
TRUFALINO. Toute modification du texte doit être validée par la direction
avant mise en ligne.

Le numéro de téléphone affiché est un portable personnel : vérifier qu'il
est bien destiné à figurer publiquement.
