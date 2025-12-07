# 🎨 Formalita Design System

> **Version:** 1.0.0  
> **Date:** 07/12/2025  
> **Référence:** Tag `v1.0.0-stable`

---

## 🔒 RÈGLE D'OR

**Toute nouvelle page (blog, services, contact, etc.) DOIT utiliser ce Design System.**

Pour créer une nouvelle page :
1. Copier les tokens CSS de `index.html`
2. Réutiliser les composants existants
3. Ne JAMAIS modifier les couleurs/typos/espacements

---

## 🎨 Couleurs

### Palette Principale
```css
/* Primary - Orange Formalita */
--orange-primary: #F97316;
--orange-dark: #EA580C;
--orange-light: #FDBA74;
--orange-50: #FFF7ED;
--orange-100: #FFEDD5;

/* Secondary - Bleu Confiance */
--blue-secondary: #2B5F9E;
--blue-dark: #1E4A7D;
--blue-light: #3B82F6;
```

### Neutres
```css
--gray-900: #111827;  /* Texte principal */
--gray-700: #374151;  /* Texte secondaire */
--gray-500: #6B7280;  /* Texte tertiaire */
--gray-300: #D1D5DB;  /* Bordures */
--gray-100: #F3F4F6;  /* Backgrounds légers */
--gray-50: #F9FAFB;   /* Backgrounds très légers */
--white: #FFFFFF;
```

### Sémantiques
```css
--success: #10B981;       /* Vert succès */
--success-light: #D1FAE5;
--warning: #F59E0B;       /* Orange warning */
--error: #EF4444;         /* Rouge erreur */
```

---

## ✏️ Typographie

### Font Family
```css
--font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
```

### Échelle de tailles
```css
--font-size-xs: 0.75rem;   /* 12px */
--font-size-sm: 0.875rem;  /* 14px */
--font-size-base: 1rem;    /* 16px */
--font-size-lg: 1.125rem;  /* 18px */
--font-size-xl: 1.25rem;   /* 20px */
--font-size-2xl: 1.5rem;   /* 24px */
--font-size-3xl: 1.875rem; /* 30px */
--font-size-4xl: 2.25rem;  /* 36px */
--font-size-5xl: 3rem;     /* 48px */
--font-size-6xl: 3.75rem;  /* 60px */
```

### Utilisation
| Élément | Taille | Poids |
|---------|--------|-------|
| H1 Hero | 5xl-6xl | 800 |
| H2 Section | 3xl-4xl | 700 |
| H3 Card | xl-2xl | 600 |
| Body | base | 400 |
| Small | sm | 400 |
| Label | xs | 500 |

---

## 📏 Espacements

```css
--space-1: 0.25rem;   /* 4px */
--space-2: 0.5rem;    /* 8px */
--space-3: 0.75rem;   /* 12px */
--space-4: 1rem;      /* 16px */
--space-5: 1.25rem;   /* 20px */
--space-6: 1.5rem;    /* 24px */
--space-8: 2rem;      /* 32px */
--space-10: 2.5rem;   /* 40px */
--space-12: 3rem;     /* 48px */
--space-16: 4rem;     /* 64px */
--space-20: 5rem;     /* 80px */
--space-24: 6rem;     /* 96px */
```

### Sections
- Padding vertical sections: `var(--space-16)` à `var(--space-24)`
- Container max-width: `1200px`
- Container padding: `var(--space-6)`

---

## 🔲 Border Radius

```css
--radius-sm: 8px;
--radius-md: 12px;
--radius-lg: 16px;
--radius-xl: 24px;
--radius-2xl: 32px;
--radius-full: 9999px;  /* Pills, avatars */
```

### Utilisation
| Élément | Radius |
|---------|--------|
| Boutons | md (12px) |
| Cards | lg-xl (16-24px) |
| Inputs | sm (8px) |
| Badges | full |
| Modals | xl (24px) |

---

## 🌑 Ombres

```css
--shadow-sm: 0 1px 2px rgba(0,0,0,0.05);
--shadow-md: 0 4px 6px -1px rgba(0,0,0,0.1), 0 2px 4px -1px rgba(0,0,0,0.06);
--shadow-lg: 0 10px 15px -3px rgba(0,0,0,0.1), 0 4px 6px -2px rgba(0,0,0,0.05);
--shadow-xl: 0 20px 25px -5px rgba(0,0,0,0.1), 0 10px 10px -5px rgba(0,0,0,0.04);
--shadow-2xl: 0 25px 50px -12px rgba(0,0,0,0.25);
--shadow-glow: 0 0 40px rgba(249, 115, 22, 0.3);  /* Glow orange */
```

---

## 🎬 Animations

### Transitions
```css
--transition-fast: 0.15s ease;
--transition-base: 0.3s ease;
--transition-slow: 0.5s ease;
--transition-bounce: 0.5s cubic-bezier(0.34, 1.56, 0.64, 1);
```

### Classes d'animation (scroll reveal)
```css
.reveal        /* Fade in up */
.reveal-left   /* Fade in from left */
.reveal-right  /* Fade in from right */
.reveal-scale  /* Scale in */
```

---

## 🧩 Composants Réutilisables

### Bouton Principal
```html
<a href="#" class="btn-primary">
    Texte du bouton →
</a>
```

### Bouton Secondaire
```html
<a href="#" class="btn-secondary">
    Texte du bouton
</a>
```

### Card Service
```html
<div class="service-card">
    <div class="service-card-icon">🏠</div>
    <h3 class="service-card-title">Titre</h3>
    <p class="service-card-desc">Description...</p>
    <a href="#" class="service-card-link">En savoir plus →</a>
</div>
```

### Badge
```html
<span class="badge">Nouveau</span>
<span class="badge badge-success">Validé</span>
```

---

## 📱 Breakpoints Responsive

```css
/* Mobile first */
@media (min-width: 640px)  { /* sm */ }
@media (min-width: 768px)  { /* md */ }
@media (min-width: 1024px) { /* lg */ }
@media (min-width: 1280px) { /* xl */ }
```

---

## 📄 Structure de Page Type

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <!-- Copier les meta + fonts de index.html -->
</head>
<body>
    <!-- Navbar (copier de index.html) -->
    <nav class="navbar">...</nav>
    
    <!-- Contenu spécifique -->
    <main>
        <section class="section-lg">
            <div class="container">
                <!-- Votre contenu -->
            </div>
        </section>
    </main>
    
    <!-- Footer (copier de index.html) -->
    <footer>...</footer>
    
    <!-- Scripts (copier de index.html) -->
</body>
</html>
```

---

## ✅ Checklist Nouvelle Page

- [ ] Copier les tokens CSS (`:root`)
- [ ] Utiliser la même navbar
- [ ] Utiliser le même footer
- [ ] Respecter les couleurs du Design System
- [ ] Utiliser les mêmes composants (boutons, cards, etc.)
- [ ] Tester responsive (mobile, tablet, desktop)
- [ ] Vérifier les animations reveal
- [ ] Inclure la mention Pôle Démarches si pertinent

---

## 🔄 Rollback vers version stable

```bash
# Si quelque chose casse, revenir à la version stable :

# Option 1: Via GitHub UI
# Aller sur releases > v1.0.0-stable > Download

# Option 2: Via Git
git fetch origin
git checkout v1.0.0-stable -- index.html
git commit -m "Rollback to stable v1.0.0"
git push

# Option 3: Reset complet
git reset --hard origin/stable
git push --force
```

---

**Maintenu par:** Groupe Yuki / Projet Y  
**Contact:** contact@formalita.fr
