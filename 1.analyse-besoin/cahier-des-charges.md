# Cahier des Charges : SoliQuiz

## 1. Contexte & Enjeux

- **Pourquoi ce projet ?** : Remplacer les outils génériques (Google Forms, Excel) utilisés pour évaluer les apprenants d'un bootcamp. Ces outils créent un **aveuglement pédagogique** : scores globaux déconnectés des objectifs, absence de feedback, saisie manuelle des notes dans SoliLMS, et interface non adaptée au mobile.
- **Cible** :
  - **Étudiant (Apprenti)** — passe les QCM quotidiennement, révise souvent sur mobile, a besoin de feedback immédiat et de suivi de progression.
  - **Formateur** — crée et gère les QCM, veut lier chaque test à une session et un objectif précis, obtenir les scores automatiquement.
  - **Administrateur (Direction pédagogique)** — supervise le centre, gère les rôles, synchronise les données avec SoliLMS.
- **Ton & Style** : Professionnel, pédagogique, rassurant. Interface sobre, claire et moderne. Priorité absolue à l'ergonomie mobile.

---

## 2. Besoins Fonctionnels

- **Besoin Métier** : Automatiser le cycle complet « Créer → Passer → Corriger → Analyser » un QCM de manière intégrée, sans ressaisie manuelle ni outil externe.

- **Fonctionnalités Clés** :

  ### Sprint 1 — MVP (Cœur du système)
  - Authentification basique avec gestion des rôles (Admin / Formateur / Étudiant)
  - Création et gestion des QCM (titre, description) par les formateurs
  - Ajout de questions à choix unique ou multiple, avec définition des bonnes réponses
  - Passation du QCM par les étudiants
  - Calcul automatique du score global à la soumission
  - Gestion des utilisateurs et des rôles par l'administrateur

  ### Sprint 2 — Fonctionnalités Avancées (Pédagogie & Analyse)
  - Liaison de chaque QCM à une session et un micro-objectif pédagogique
  - Calcul et affichage du score ventilé par objectif (ex : « Logique : 80%, Syntaxe : 20% »)
  - Feedback détaillé : affichage de la correction avec explication de la bonne réponse
  - Timer (compte à rebours) visible pendant la passation
  - Auto-sauvegarde des réponses en cours (prévention des pertes de connexion)
  - Historique des évaluations et tableau de bord de progression (Étudiant & Formateur)
  - Tableau de bord global de supervision pour l'administrateur
  - Export / synchronisation des notes vers SoliLMS via API

- **Contenus Indispensables** :
  - QCM (titre, description, session liée, objectif lié)
  - Questions (énoncé, type : unique / multiple)
  - Choix de réponses (libellé, statut : correct / incorrect)
  - Résultats (score global, score par objectif, historique)
  - Utilisateurs (nom, rôle, cohorte)

---

## 3. Contraintes

- **Deadline** : À définir — développement itératif en 2 sprints.
- **Technique** :
  - Application web (Web & APK envisagé à terme)
  - Interface **mobile-first** obligatoire (les étudiants révisent dans les transports)
  - Distinction visuelle stricte entre choix unique (boutons radio) et choix multiple (cases à cocher)
  - Tolérance aux coupures réseau (auto-sauvegarde côté client)
  - Sécurité : accès aux QCM réservé aux utilisateurs authentifiés
  - Interopérabilité : API de synchronisation vers SoliLMS (moyen terme)
- **Langue** : Français
