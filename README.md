# 🟠 Formalita Landing Page

> **Site web officiel** : [formalita.fr](https://formalita.fr)  
> **Hébergement** : Netlify (auto-deploy)  
> **Version stable** : `v1.0.0-stable`

---

## 🚀 Déploiement

Le site est **automatiquement déployé** sur Netlify à chaque push sur `main`.

| Environnement | URL | Branche |
|---------------|-----|---------|
| **Production** | https://formalita.fr | `main` |
| **Backup stable** | - | `stable` |

---

## 📁 Structure du Repo

```
formalita-landing/
├── index.html          # Landing page principale
├── DESIGN_SYSTEM.md    # Documentation Design System
├── README.md           # Ce fichier
└── (futures pages)     # blog.html, services.html, etc.
```

---

## 🔒 Stratégie de Backup

### Niveaux de Protection

| Niveau | Type | Usage |
|--------|------|-------|
| 🏷️ **Tag** | `v1.0.0-stable` | Version immutable de référence |
| 🌿 **Branche** | `stable` | Backup de la version stable |
| 📦 **Release** | GitHub Release | Archive téléchargeable |

### Revenir à la version stable

```bash
# Option 1: Restaurer un fichier spécifique
git checkout v1.0.0-stable -- index.html
git commit -m "Rollback index.html to stable"
git push

# Option 2: Reset complet sur stable
git fetch origin
git reset --hard origin/stable
git push --force

# Option 3: Via GitHub UI
# Releases > v1.0.0-stable > Download ZIP
```

---

## 🎨 Design System

Toute nouvelle page **DOIT** respecter le Design System documenté dans [`DESIGN_SYSTEM.md`](DESIGN_SYSTEM.md).

### Tokens Principaux

| Token | Valeur |
|-------|--------|
| Orange Primary | `#F97316` |
| Blue Secondary | `#2B5F9E` |
| Font | Inter |
| Border Radius | 8-32px |

### Créer une Nouvelle Page

1. Copier la structure de `index.html`
2. Réutiliser navbar + footer
3. Appliquer les tokens CSS
4. Suivre la checklist dans DESIGN_SYSTEM.md

---

## 📝 Workflow de Modification

### Modification Simple
```bash
# 1. Éditer le fichier
# 2. Commit + Push
git add .
git commit -m "Description du changement"
git push
# → Auto-deploy sur Netlify
```

### Modification Risquée
```bash
# 1. Créer une branche
git checkout -b feature/ma-modification

# 2. Faire les changements
# 3. Tester localement
# 4. Merger si OK
git checkout main
git merge feature/ma-modification
git push
```

### ⚠️ En cas de problème
```bash
# Rollback immédiat
git checkout v1.0.0-stable -- index.html
git commit -m "🚨 Rollback to stable"
git push
```

---

## 🔗 Ressources

- **Netlify Dashboard** : [app.netlify.com](https://app.netlify.com)
- **Site ID** : `2223fae8-6e90-4fe9-932e-9e7d2ac77e1b`
- **Release stable** : [v1.0.0-stable](https://github.com/manu23232323/formalita-landing/releases/tag/v1.0.0-stable)

---

## 📞 Contact

- **Email** : contact@formalita.fr
- **Projet** : Groupe Yuki / Projet Y

---

**⚠️ Service privé indépendant, non affilié à l'administration publique. Partenaire certifié Pôle Démarches.**
