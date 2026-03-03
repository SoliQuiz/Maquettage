# Wireframe : Gestion des Utilisateurs (`/admin/utilisateurs`)

**Rôle(s)** : Administrateur
**Sprint** : 1
**Lecture visuelle** : F-pattern — liste principale avec actions inline

---

## ZONE 1 : Header (Navigation Admin)

- **Composant** : Logo + Menu Admin
- **Contenu** : "Utilisateurs" (actif) | "Tableau de bord" | "API SoliLMS"

- **Composant** : Avatar + Prénom Admin + Déconnexion

---

## ZONE 2 : Hero (Titre + Recherche)

- **Composant** : Titre H1
- **Contenu** : "Gestion des utilisateurs — SoliQuiz"

- **Composant** : Barre de recherche
- **Contenu** : Placeholder "Rechercher un utilisateur..."

- **Composant** : Filtres inline
  - Toggle : "Tous" | "Formateurs" | "Étudiants"
  - Toggle : "Actifs" | "Inactifs"

- **Composant** : Bouton CTA principal (above the fold)
- **Contenu** : "+ Ajouter un utilisateur"
- **Action** : Ouvre modale de création

---

## ZONE 3 : Body — Tableau des utilisateurs

- **Composant** : Tableau paginé
  - Colonnes : Nom | Prénom | Email | Rôle | Statut | Actions

- **Composant** : Badges de rôle (colorés)
  - 🟦 Formateur | 🟩 Étudiant | 🟥 Admin

- **Composant** : Toggle statut par ligne
  - Switch "Actif / Inactif" directement dans le tableau

- **Composant** : Boutons d'action par ligne
  - [Modifier le rôle] → Dropdown inline
  - [Désactiver] → Confirmation modale

---

## ZONE 4 : Body — Modale "Ajouter un utilisateur" (conditionnelle)

- **Composant** : Formulaire court (overlay/modale)
  - Champ : Prénom + Nom
  - Champ : Email
  - Sélecteur : Rôle (Formateur / Étudiant)
  - Bouton : "Créer le compte"

---

## ZONE 5 : Footer (Pagination)

- **Composant** : Pagination numérique
- **Contenu** : "← 1 2 3 ... →"

- **Composant** : Indicateur
- **Contenu** : "Affichage de 1 à 20 sur 87 utilisateurs"
