# Wireframe : Connexion (`/login`)

**Rôle(s)** : Tous (Étudiant, Formateur, Administrateur)
**Sprint** : 1
**Lecture visuelle** : Centrage vertical (Z-pattern)

---

## ZONE 1 : Header (Identité)

- **Composant** : Logo + Nom
- **Contenu** : Logo SoliQuiz — "SoliQuiz"
- **Action** : Aucune (page publique unique)

---

## ZONE 2 : Hero / Formulaire (Above the fold)

- **Composant** : Titre H1
- **Contenu** : "Connectez-vous à SoliQuiz"

- **Composant** : Champ de saisie — Email
- **Contenu** : Placeholder "Votre adresse email"

- **Composant** : Champ de saisie — Mot de passe
- **Contenu** : Placeholder "Votre mot de passe"

- **Composant** : Bouton CTA principal (full-width)
- **Contenu** : "Se connecter"
- **Action** : Soumettre le formulaire → Redirection `/dashboard`

---

## ZONE 3 : Body (Aide)

- **Composant** : Texte d'aide
- **Contenu** : "Première connexion ? Contactez votre administrateur."

- **Composant** : Message d'erreur (conditionnel)
- **Contenu** : "Identifiants incorrects. Vérifiez et réessayez."

---

## ZONE 4 : Footer

- **Composant** : Texte légal minimal
- **Contenu** : "© SoliQuiz — Bootcamp interne"
