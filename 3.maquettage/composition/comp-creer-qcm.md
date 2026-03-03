# Composition - Page Créer QCM

## Source
- **Wireframe** : `2.organisation-contenu/wireframes/creer-qcm.md`
- **Mockup Final** : `3.maquettage/mockups/creer-qcm.html`

## Structure de Composition

```
Header
└── navbar-simple (Molécule) → components-lib/molecules/navbar-simple/
    ├── logo (Atom) → components-lib/atoms/logo/
    └── breadcrumb (Molécule) → components-lib/molecules/breadcrumb/
        └── breadcrumb-item (Atom) → components-lib/atoms/breadcrumb-item/

Main
├── step-indicator (Molécule) → components-lib/molecules/step-indicator/
│   └── step-item (Atom) → components-lib/atoms/step-item/
│
├── hero-section (Molécule) → components-lib/molecules/hero-section/
│   ├── heading-1 (Atom) → components-lib/atoms/heading-1/
│   └── text-muted (Atom) → components-lib/atoms/text-muted/
│
├── Form Step 1 (Général)
│   └── form-qcm-general (Molécule) → components-lib/molecules/form-qcm-general/
│       ├── form-group (Molécule)
│       │   ├── label (Atom)
│       │   └── input-text (Atom)
│       ├── form-group (Molécule)
│       │   ├── label (Atom)
│       │   └── textarea (Atom)
│       ├── form-group (Molécule)
│       │   ├── label (Atom)
│       │   └── select (Atom)
│       └── button-primary (Atom)
│
└── Form Step 2 (Questions)
    └── questions-manager (Molécule) → components-lib/molecules/questions-manager/
        ├── heading-2 (Atom)
        ├── question-list (Molécule)
        │   └── question-card-admin (Molécule)
        └── question-form-inline (Molécule)
            ├── input-text (Atom)
            ├── choice-toggle (Atom)
            └── button-secondary (Atom)

Footer
└── action-bar (Molécule) → components-lib/molecules/action-bar/
    ├── button-secondary (Atom)
    └── button-primary (Atom)
```

## Composants Nécessaires

### Atoms (dans components-lib/atoms/)
- [ ] `logo/` - Logo
- [ ] `breadcrumb-item/` - Item de lien de navigation
- [ ] `step-item/` - Indicateur d'étape (actif/inactif)
- [x] `heading-1/` - Titre H1
- [ ] `heading-2/` - Titre H2
- [ ] `text-muted/` - Texte secondaire
- [x] `label/` - Label de formulaire
- [x] `input-text/` - Champ texte
- [ ] `textarea/` - Zone de texte
- [ ] `select/` - Menu déroulant
- [ ] `choice-toggle/` - Toggle switch ou segmented control pour le type de question
- [x] `button-primary/` - Bouton principal
- [ ] `button-secondary/` - Bouton secondaire

### Molécules (dans components-lib/molecules/)
- [ ] `navbar-simple/` - Navbar avec fil d'ariane
- [ ] `breadcrumb/` - Fil d'ariane
- [ ] `step-indicator/` - Barre de progression d'étapes
- [ ] `hero-section/` - Titre + Sous-titre
- [x] `form-group/` - Label + Input (hérité du login-form)
- [ ] `form-qcm-general/` - Formulaire complet étape 1
- [ ] `questions-manager/` - Conteneur complet étape 2
- [ ] `question-list/` - Liste des questions ajoutées
- [ ] `question-card-admin/` - Carte question avec actions modif/suppr
- [ ] `question-form-inline/` - Petit formulaire d'ajout de question
- [ ] `action-bar/` - Barre de boutons fixe en bas ou sous le formulaire

## Statut de Création
- [ ] Charte Graphique validée
- [ ] Tous les atoms créés
- [ ] Toutes les molécules créées
- [ ] Mockup assemblé dans `mockups/creer-qcm.html`
