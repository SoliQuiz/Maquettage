# Wireframe : Passer un QCM (`/etudiant/qcm/:id/passer`)

**Rôle(s)** : Étudiant
**Sprint** : 1 (base) + Sprint 2 (Timer, Auto-save)
**Lecture visuelle** : Z-pattern — focus total sur la question courante

---

## ZONE 1 : Header (Barre de progression)

- **Composant** : Titre du QCM (H1 réduit)
- **Contenu** : "[Titre du QCM] — Évaluation en cours"

- **Composant** : Barre de progression linéaire
- **Contenu** : "Question 3 / 10" + barre visuelle remplie à 30%

- **Composant** : Timer (compte à rebours) — Sprint 2
- **Contenu** : "⏱ 12:45 restantes"
- **Règle** : Toujours visible, couleur change à rouge sous 2 min

---

## ZONE 2 : Hero (Question courante — Above the fold)

- **Composant** : Numéro + Énoncé de la question (H2)
- **Contenu** : "Question 3 — [Énoncé de la question]"

- **Composant** : Badge type de question
- **Contenu** : "🔘 Choix unique" OU "☑ Choix multiple"
- **Règle** : Distinction visuelle obligatoire (WCAG AA)

---

## ZONE 3 : Body (Choix de réponses)

- **Composant** : Liste de choix (radio ou checkbox selon le type)
  - Choix unique → Boutons radio `( ) Réponse A`
  - Choix multiple → Cases à cocher `[ ] Réponse A`
- **Nombre** : 3 à 5 choix par question

- **Composant** : Indicateur auto-save — Sprint 2
- **Contenu** : "✅ Réponses sauvegardées" (discret, en bas de zone)

---

## ZONE 4 : Footer (Navigation entre questions)

- **Composant** : Bouton secondaire — "← Question précédente"
- **Action** : Revenir à la question précédente

- **Composant** : Bouton principal — "Question suivante →"
- **Action** : Passer à la question suivante

- **Composant** : Bouton CTA final (visible uniquement à la dernière question)
- **Contenu** : "Valider mes réponses"
- **Action** : Soumission → `/etudiant/qcm/:id/resultats`
- **Règle** : Confirmation modale avant soumission définitive ("Êtes-vous sûr ?")
