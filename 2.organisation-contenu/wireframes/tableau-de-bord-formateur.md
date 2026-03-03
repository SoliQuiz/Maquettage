# Wireframe : Tableau de Bord Formateur (`/formateur/tableau-de-bord`)

**Rôle(s)** : Formateur
**Sprint** : 2
**Lecture visuelle** : F-pattern — KPIs en haut, détail en bas

---

## ZONE 1 : Header (Navigation)

- **Composant** : Logo + Menu Formateur
- **Contenu** : "Mes QCM" | "Créer un QCM" | "Tableau de bord" (actif)

- **Composant** : Avatar + Prénom + Déconnexion

---

## ZONE 2 : Hero (Accroche + Filtres)

- **Composant** : Titre H1
- **Contenu** : "Tableau de bord — Performances de votre classe"

- **Composant** : Sélecteurs de filtre (inline)
  - Dropdown "Session" — Ex : "Session 5 — Semaine du 24/02"
  - Dropdown "Module / Objectif" — Ex : "JavaScript — Algorithmes"

---

## ZONE 3 : Body — Bloc A (KPIs globaux — 3 cards)

- **Composant** : 3 × Stat Cards (icône + grand chiffre + libellé)
  - Card 1 : "78% — Taux de réussite moyen"
  - Card 2 : "22 — Étudiants ayant passé le QCM"
  - Card 3 : "3 — Étudiants en difficulté (< 50%)"

---

## ZONE 4 : Body — Bloc B (Répartition par objectif)

- **Composant** : Titre H2
- **Contenu** : "Résultats par objectif pédagogique"

- **Composant** : Barres de progression horizontales par objectif
  - "Logique algorithmique : 82% ████████░░"
  - "Syntaxe JavaScript : 55% █████░░░░░"
  - "Débogage : 70% ███████░░░"

---

## ZONE 5 : Body — Bloc C (Liste individuelle des étudiants)

- **Composant** : Titre H2
- **Contenu** : "Détail par étudiant"

- **Composant** : Tableau (Nom | Score / 20 | Score % | Statut | Lien détail)
  - Lignes triables par score
  - Étudiants < 50% surlignés en rouge
  - Bouton "Voir le détail" → `/formateur/qcm/:id/resultats?etudiant=:id`

---

## ZONE 6 : Footer

- **Composant** : Bouton CTA
- **Contenu** : "Créer un nouveau QCM"
- **Action** : Vers `/formateur/qcm/creer`
