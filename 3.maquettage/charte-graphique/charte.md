# Charte Graphique : SoliQuiz

> **Inspiration** : SoliLMS (Professional, Clean, Data-centric)
> **Ton** : Professionnel, Pédagogique, Rassurant
> **Priorité** : Lisibilité & Mobile-First

---

## 🎨 Palette de Couleurs

| Rôle | Couleur | Hex | Usage |
|---|---|---|---|
| **Primary (SoliDark)** | ![#0E4B5E](https://via.placeholder.com/15/0E4B5E/0E4B5E.png) | `#0E4B5E` | Sidebar, Titres, Identité forte |
| **Secondary (SoliAction)** | ![#00A8E8](https://via.placeholder.com/15/00A8E8/00A8E8.png) | `#00A8E8` | Boutons d'action, Liens, Focus |
| **Success** | ![#28A745](https://via.placeholder.com/15/28A745/28A745.png) | `#28A745` | Scores élevés, Validations, Feedback positif |
| **Warning** | ![#FFB800](https://via.placeholder.com/15/FFB800/FFB800.png) | `#FFB800` | À valider, Timer (alerte), Attention |
| **Danger** | ![#DC3545](https://via.placeholder.com/15/DC3545/DC3545.png) | `#DC3545` | Erreurs, Scores bas, Alertes critiques |
| **Background** | ![#F8FAFC](https://via.placeholder.com/15/F8FAFC/F8FAFC.png) | `#F8FAFC` | Fond de page neutre |
| **Surface** | ![#FFFFFF](https://via.placeholder.com/15/FFFFFF/FFFFFF.png) | `#FFFFFF` | Cards, Blocs de contenu, Inputs |
| **Border** | ![#E2E8F0](https://via.placeholder.com/15/E2E8F0/E2E8F0.png) | `#E2E8F0` | Séparateurs, Bordures de cards |

---

## ✍️ Typographie

- **Police principale** : `Inter` (Sans-serif)
  - *Alternative* : `system-ui`
- **Échelle de tailles** :
  - **H1 (Titre Page)** : 24px (Mobile) / 32px (Desktop) | Bold
  - **H2 (Section/Question)** : 18px / 22px | Semibold
  - **Body (Texte/Choix)** : 16px | Regular
  - **Caption (Stats/Meta)** : 13px | Medium

---

## ✨ Principes UI & Composants

### 📱 Mobile-First
- Largeur des boutons : 100% sur mobile.
- Espacement minimal (Touch Target) : 44px.
- Marges latérales : 16px (4rem).

### 🧊 Formes & Ombres
- **Border Radius** : `8px` (Standard) / `12px` (Cards).
- **Shadows** : `sm` (Subtle) sur les cards pour la profondeur.
- **Inputs** : Bordure légère `#E2E8F0`, focus `#00A8E8`.

### 🔘 Système de Choix (Critique)
- **Choix Unique** : Cercle (Radio) — Cercle plein au centre au focus.
- **Choix Multiple** : Carré (Checkbox) — Crochet/Check au focus.
- **Feedback** : Affichage vert (Juste) / Rouge (Faux) lors de la correction.

---

## 🛠️ Tokens CSS (Tailwind)

```javascript
module.exports = {
  theme: {
    extend: {
      colors: {
        soli: {
          dark: '#0E4B5E',
          action: '#00A8E8',
          bg: '#F8FAFC',
          border: '#E2E8F0'
        }
      },
      borderRadius: {
        'soli': '8px',
      }
    }
  }
}
```
