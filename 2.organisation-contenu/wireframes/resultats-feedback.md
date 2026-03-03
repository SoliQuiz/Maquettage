# Wireframe : Résultats & Feedback (`/etudiant/qcm/:id/resultats`)

**Rôle(s)** : Étudiant
**Sprint** : 1 (score global) + Sprint 2 (score/objectif + correction détaillée)
**Lecture visuelle** : F-pattern — score en haut, détail en bas

---

## ZONE 1 : Header (Navigation retour)

- **Composant** : Logo + Fil d'Ariane
- **Contenu** : "SoliQuiz > Mes QCM > [Titre QCM] > Résultats"

- **Composant** : Bouton retour
- **Contenu** : "← Retour à mes QCM"
- **Action** : Vers `/etudiant/qcm`

---

## ZONE 2 : Hero (Score global — Above the fold)

- **Composant** : Titre H1
- **Contenu** : "Vos résultats — [Titre du QCM]"

- **Composant** : Score visuel principal (grand format)
- **Contenu** : "15 / 20" + mention (Ex : "✅ Réussi" / "⚠️ À retravailler")

- **Composant** : Jauge circulaire ou barre de score
- **Contenu** : Pourcentage de réussite global (75%)

---

## ZONE 3 : Body — Bloc A (Score par objectif — Sprint 2)

- **Composant** : Titre H2
- **Contenu** : "Score par objectif pédagogique"

- **Composant** : Liste de barres de progression par objectif
  - "Logique algorithmique : 80% ████████░░"
  - "Syntaxe JavaScript : 50% █████░░░░░"
  - "Structures de données : 60% ██████░░░░"

---

## ZONE 4 : Body — Bloc B (Correction détaillée — Sprint 2)

- **Composant** : Titre H2
- **Contenu** : "Correction détaillée"

- **Composant** : Liste accordéon (une entrée par question)
  - ✅ "Question 1 — Bonne réponse" (vert)
  - ❌ "Question 2 — Mauvaise réponse" (rouge) → Explication affichée

- **Composant** : Explication de la bonne réponse
- **Contenu** : "[Texte explicatif de la bonne réponse]"

---

## ZONE 5 : Footer (CTA de navigation)

- **Composant** : Bouton secondaire
- **Contenu** : "Voir mon historique"
- **Action** : Vers `/etudiant/historique`

- **Composant** : Bouton principal
- **Contenu** : "Retour à mes QCM"
- **Action** : Vers `/etudiant/qcm`
