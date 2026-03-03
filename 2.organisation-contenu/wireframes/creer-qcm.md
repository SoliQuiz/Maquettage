# Wireframe : Créer un QCM (`/formateur/qcm/creer` + `/formateur/qcm/:id/questions`)

**Rôle(s)** : Formateur
**Sprint** : 1
**Lecture visuelle** : F-pattern — formulaire structuré en 2 étapes

---

## ZONE 1 : Header (Navigation)

- **Composant** : Logo + Fil d'Ariane
- **Contenu** : "SoliQuiz > Mes QCM > Créer un QCM"

- **Composant** : Indicateur d'étapes
- **Contenu** : "Étape 1 : Informations générales → Étape 2 : Questions & Choix"

---

## ZONE 2 : Hero (Titre de section)

- **Composant** : Titre H1
- **Contenu** : "Créer un nouveau QCM"

- **Composant** : Sous-titre
- **Contenu** : "Créez votre évaluation en quelques minutes."

---

## ZONE 3 : Body — Étape 1 (Informations générales)

- **Composant** : Champ texte — Titre du QCM (obligatoire)
- **Contenu** : Placeholder "Ex : QCM J05 — Algorithmes de tri"

- **Composant** : Champ texte — Description
- **Contenu** : Placeholder "Objectif général de ce QCM"

- **Composant** : Sélecteur — Session liée (Sprint 2)
- **Contenu** : Dropdown "Sélectionner une session"

- **Composant** : Sélecteur — Objectif pédagogique (Sprint 2)
- **Contenu** : Dropdown "Sélectionner un objectif"

- **Composant** : Bouton CTA primaire
- **Contenu** : "Enregistrer et ajouter les questions →"
- **Action** : Sauvegarde QCM → Redirection `/formateur/qcm/:id/questions`

---

## ZONE 4 : Body — Étape 2 (Gestion Questions & Choix)

- **Composant** : Titre H2
- **Contenu** : "Questions du QCM (0 ajoutées)"

- **Composant** : Card par question (liste)
  - Numéro | Énoncé | Type (unique/multiple) | Boutons [Modifier] [Supprimer]

- **Composant** : Formulaire ajout question (inline ou modale)
  - Champ : Énoncé de la question
  - Toggle : Type → Choix unique 🔘 / Choix multiple ☑
  - Champs dynamiques : Choix A, B, C, D + sélecteur "Bonne réponse"
  - Bouton : "Ajouter la question"

---

## ZONE 5 : Footer (Actions globales)

- **Composant** : Bouton secondaire
- **Contenu** : "← Retour aux informations"

- **Composant** : Bouton principal
- **Contenu** : "Enregistrer le QCM"
- **Action** : Finaliser → `/formateur/qcm`
