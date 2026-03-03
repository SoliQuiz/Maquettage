# Sitemap : SoliQuiz

> **Règles appliquées** : Règle des 3 clics · Siloing par rôle · Menu ≤ 7 entrées

---

## 🌐 Architecture Globale

```
[Connexion / Auth]                        ← Point d'entrée unique
│
├── [Dashboard]                           ← Page d'accueil post-connexion (adaptée au rôle)
│
├── 👨‍🎓 ESPACE ÉTUDIANT
│   ├── [Mes QCM]                         ← Liste des QCM disponibles
│   │   └── [Passer le QCM]              ← Interface de passation (timer + auto-save)
│   │       └── [Résultats & Feedback]   ← Score global + score/objectif + correction
│   ├── [Mon Historique]                  ← Liste des évaluations passées
│   └── [Mon Tableau de bord]            ← Progression par compétence/objectif
│
├── 👨‍🏫 ESPACE FORMATEUR
│   ├── [Mes QCM]                         ← Liste des QCM créés
│   │   ├── [Créer un QCM]               ← Titre, description, session, objectif
│   │   │   └── [Gérer Questions/Choix]  ← Ajout / modification / suppression
│   │   └── [Voir les Résultats]         ← Scores de la classe par QCM
│   └── [Tableau de bord Classe]         ← Vue d'ensemble des performances par session
│
└── 🔧 ESPACE ADMINISTRATEUR
    ├── [Gestion des Utilisateurs]        ← Activer / désactiver / rôles
    ├── [Tableau de bord Global]          ← Taux de réussite par cohorte & module
    └── [Configuration API SoliLMS]      ← Paramétrage synchronisation
```

---

## 📄 Inventaire des Pages/Vues

| # | Slug / Vue | Rôle(s) | Sprint | Besoin fonctionnel |
|---|---|---|---|---|
| 1 | `/login` | Tous | Sprint 1 | Authentification |
| 2 | `/dashboard` | Tous | Sprint 1 | Hub adaptatif post-connexion |
| 3 | `/etudiant/qcm` | Étudiant | Sprint 1 | Liste des QCM disponibles |
| 4 | `/etudiant/qcm/:id/passer` | Étudiant | Sprint 1 | Passation QCM (timer, auto-save) |
| 5 | `/etudiant/qcm/:id/resultats` | Étudiant | Sprint 1-2 | Score + feedback + correction |
| 6 | `/etudiant/historique` | Étudiant | Sprint 2 | Historique des évaluations |
| 7 | `/etudiant/progression` | Étudiant | Sprint 2 | Dashboard compétences/objectifs |
| 8 | `/formateur/qcm` | Formateur | Sprint 1 | Liste des QCM créés |
| 9 | `/formateur/qcm/creer` | Formateur | Sprint 1 | Création QCM |
| 10 | `/formateur/qcm/:id/questions` | Formateur | Sprint 1 | Gestion questions & choix |
| 11 | `/formateur/qcm/:id/resultats` | Formateur | Sprint 1-2 | Résultats classe + score/objectif |
| 12 | `/formateur/tableau-de-bord` | Formateur | Sprint 2 | Vue globale classe |
| 13 | `/admin/utilisateurs` | Admin | Sprint 1 | Gestion des utilisateurs (rôles & cohortes) |
| 14 | `/admin/tableau-de-bord` | Admin | Sprint 2 | Stats globales cohortes |
| 15 | `/admin/api-solilms` | Admin | Sprint 2 | Config synchronisation SoliLMS |

---

## 🗂️ Silos Sémantiques

| Silo | Pages concernées | Thématique |
|---|---|---|
| **Auth** | `/login` | Gestion de l'identité |
| **Évaluation** | `/etudiant/qcm/*` | Passation & résultats |
| **Progression** | `/etudiant/historique`, `/etudiant/progression` | Suivi individuel |
| **Création** | `/formateur/qcm/*` | Gestion des QCM |
| **Pilotage** | `/formateur/tableau-de-bord`, `/admin/tableau-de-bord` | Analyse & supervision |
| **Administration** | `/admin/utilisateurs`, `/admin/api-solilms` | Gestion système |
