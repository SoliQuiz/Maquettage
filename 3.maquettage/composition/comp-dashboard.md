# Composition - Page Dashboard

## Source
- **Wireframe** : `2.organisation-contenu/wireframes/dashboard.md`
- **Mockup Final** : `3.maquettage/mockups/dashboard.html`

## Structure de Composition

```
Header
└── navbar (Molécule) → components-lib/molecules/navbar/
    ├── logo (Atom) → components-lib/atoms/logo/
    ├── nav-menu (Molécule) → components-lib/molecules/nav-menu/
    │   └── nav-link (Atom) → components-lib/atoms/nav-link/
    └── user-profile (Molécule) → components-lib/molecules/user-profile/
        ├── avatar (Atom) → components-lib/atoms/avatar/
        └── button-logout (Atom/button) → components-lib/atoms/button-logout/

Main
├── hero-banner (Molécule) → components-lib/molecules/hero-banner/
│   ├── heading-1 (Atom) → components-lib/atoms/heading-1/
│   └── text-lead (Atom) → components-lib/atoms/text-lead/
│
└── Dashboard Content
    ├── action-cards-grid (Molécule) → components-lib/molecules/action-cards-grid/
    │   └── action-card (Molécule) → components-lib/molecules/action-card/
    │       ├── heading-3 (Atom) → components-lib/atoms/heading-3/
    │       └── button-primary (Atom) → components-lib/atoms/button-primary/
    │
    ├── stats-grid (Molécule) → components-lib/molecules/stats-grid/
    │   └── stat-card (Molécule) → components-lib/molecules/stat-card/
    │       ├── icon (Atom) → components-lib/atoms/icon/
    │       ├── stat-value (Atom) → components-lib/atoms/stat-value/
    │       └── stat-label (Atom) → components-lib/atoms/stat-label/
    │
    └── activity-list (Molécule) → components-lib/molecules/activity-list/
        └── activity-item (Molécule) → components-lib/molecules/activity-item/
            ├── text-date (Atom) → components-lib/atoms/text-date/
            ├── text-title (Atom) → components-lib/atoms/text-title/
            └── text-status (Atom) → components-lib/atoms/text-status/

Footer
└── simple-footer (Molécule) → components-lib/molecules/simple-footer/
    └── text-copy (Atom) → components-lib/atoms/text-copy/
```

## Composants Nécessaires

### Atoms (dans components-lib/atoms/)
- [ ] `logo/` - Logo SoliQuiz (SVG)
- [ ] `nav-link/` - Lien de navigation (états hover/active)
- [ ] `avatar/` - Image de profil utilisateur
- [ ] `button-logout/` - Bouton de déconnexion spécifique (ou variant de button)
- [x] `heading-1/` - Titre principal H1
- [ ] `text-lead/` - Texte d'introduction
- [ ] `heading-3/` - Titre H3 pour les cards
- [x] `button-primary/` - Bouton d'action principal
- [ ] `icon/` - Library d'icônes (Heroicons/Lucide)
- [ ] `stat-value/` - Style pour les grands chiffres de stats
- [ ] `stat-label/` - Style pour les labels de stats
- [ ] `text-date/` - Style pour les dates
- [ ] `text-title/` - Style pour les titres d'activité
- [ ] `text-status/` - Badge de statut (terminé, en cours, etc.)
- [ ] `text-copy/` - Texte de copyright footer

### Molécules (dans components-lib/molecules/)
- [ ] `navbar/` - Barre de navigation complète
- [ ] `nav-menu/` - Liste de liens responsive
- [ ] `user-profile/` - Bloc utilisateur (avatar + déconnexion)
- [ ] `hero-banner/` - Bannière de bienvenue personnalisée
- [ ] `action-cards-grid/` - Grille responsive pour les cards d'action
- [ ] `action-card/` - Carte d'action individuelle (Titre + Bouton)
- [ ] `stats-grid/` - Grille pour les indicateurs
- [ ] `stat-card/` - Carte d'indicateur (Icône + Valeur + Label)
- [ ] `activity-list/` - Liste des activités récentes
- [ ] `activity-item/` - Ligne d'activité individuelle
- [ ] `simple-footer/` - Pied de page basique

## Statut de Création
- [ ] Charte Graphique validée
- [ ] Tous les atoms créés
- [ ] Toutes les molécules créées
- [ ] Mockup assemblé dans `mockups/dashboard.html`
