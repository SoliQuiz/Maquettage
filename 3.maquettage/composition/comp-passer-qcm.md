# Composition - Page Passer QCM

## Source
- **Wireframe** : `2.organisation-contenu/wireframes/passer-qcm.md`
- **Mockup Final** : `3.maquettage/mockups/passer-qcm.html`

## Structure de Composition

```
Header
└── quiz-header (Molécule) → components-lib/molecules/quiz-header/
    ├── heading-1-mini (Atom)
    ├── progress-bar (Molécule)
    │   ├── text-progress (Atom)
    │   └── progress-track (Atom)
    └── quiz-timer (Atom)

Main (Focus Zone)
├── question-header (Molécule) → components-lib/molecules/question-header/
│   ├── heading-2 (Atom)
│   └── question-badge (Atom)
│
├── choice-container (Molécule) → components-lib/molecules/choice-container/
│   └── choice-item (Molécule)
│       ├── input-selector (Atom: radio/checkbox)
│       └── text-choice (Atom)
│
└── status-feedback (Atom) → components-lib/atoms/status-feedback/

Footer (Navigation)
└── quiz-nav (Molécule) → components-lib/molecules/quiz-nav/
    ├── button-secondary (Atom)
    ├── button-primary (Atom)
    └── button-cta-final (Atom)
```

## Composants Nécessaires

### Atoms (dans components-lib/atoms/)
- [ ] `heading-1-mini/` - Version compacte du H1
- [ ] `text-progress/` - Label de progression (ex: "Question 3 / 10")
- [ ] `progress-track/` - Fond et jauge de la barre de progression
- [ ] `quiz-timer/` - Affichage du temps avec variant d'urgence
- [x] `heading-2/` - Énoncé de la question
- [ ] `question-badge/` - Badge "Choix unique" / "Multiple"
- [x] `input-selector/` - Radio button ou Checkbox stylisé
- [ ] `text-choice/` - Texte de la réponse
- [ ] `status-feedback/` - Indicateur discret "Sauvegardé"
- [x] `button-primary/` - Bouton "Suivant"
- [ ] `button-secondary/` - Bouton "Précédent"
- [ ] `button-cta-final/` - Bouton "Valider" (Accentué)

### Molécules (dans components-lib/molecules/)
- [ ] `quiz-header/` - Barre de statut complète
- [ ] `progress-bar/` - Ensemble texte + jauge
- [ ] `question-header/` - Énoncé + badge type
- [ ] `choice-container/` - Liste des réponses
- [ ] `choice-item/` - Ligne de réponse (Cliquable)
- [ ] `quiz-nav/` - Barre de navigation entre questions

## Statut de Création
- [ ] Charte Graphique validée
- [ ] Tous les atoms créés
- [ ] Toutes les molécules créées
- [ ] Mockup assemblé dans `mockups/passer-qcm.html`
