# Wireframe : Dashboard (`/dashboard`)

**Rôle(s)** : Tous (contenu adapté au rôle connecté)
**Sprint** : 1
**Lecture visuelle** : F-pattern (scan gauche → droite → bas)

---

## ZONE 1 : Header (Navigation principale)

- **Composant** : Logo + Nom
- **Contenu** : "SoliQuiz"

- **Composant** : Menu de navigation (adapté au rôle)
  - Étudiant : "Mes QCM" | "Mon historique" | "Ma progression"
  - Formateur : "Mes QCM" | "Créer un QCM" | "Tableau de bord"
  - Admin : "Utilisateurs" | "Tableau de bord" | "API SoliLMS"

- **Composant** : Avatar + Prénom utilisateur + Déconnexion
- **Action** : Clic déconnexion → `/login`

---

## ZONE 2 : Hero (Accroche personnalisée)

- **Composant** : Titre H1
- **Contenu** : "Bonjour [Prénom] — Votre tableau de bord"

- **Composant** : Sous-titre contextuel
  - Étudiant : "Vos QCM du jour sont disponibles."
  - Formateur : "Gérez vos évaluations et suivez votre classe."
  - Admin : "Supervisez le centre et gérez les accès."

---

## ZONE 3 : Body (Contenu principal)

### Bloc A — Actions rapides (cards horizontales)

- **Composant** : Card action principale (CTA above the fold)
  - Étudiant : Card "QCM disponibles" → `Commencer le QCM` → `/etudiant/qcm`
  - Formateur : Card "Créer un QCM" → `Créer maintenant` → `/formateur/qcm/creer`
  - Admin : Card "Gérer les utilisateurs" → `Voir les utilisateurs` → `/admin/utilisateurs`

### Bloc B — Résumé statistique (3 indicateurs)

- **Composant** : 3 × Stat Cards (icône + chiffre + libellé)
  - Étudiant : QCM passés | Score moyen | Dernière note
  - Formateur : QCM créés | Étudiants actifs | Taux réussite moyen
  - Admin : Utilisateurs actifs | QCM totaux | Taux réussite global

### Bloc C — Activité récente (liste)

- **Composant** : Liste des 5 dernières activités
- **Contenu** : Date | Titre QCM | Score/Statut
- **Action** : Clic sur ligne → Détail résultat ou QCM

---

## ZONE 4 : Footer

- **Composant** : Navigation secondaire
- **Contenu** : "© SoliQuiz — Bootcamp interne"
