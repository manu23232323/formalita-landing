# 🟠 Formalita - Landing Page

Landing page professionnelle pour **Formalita** - Services d'accompagnement administratif.

## 🚀 Déploiement rapide

### Prérequis
- Un compte [GitHub](https://github.com)
- Un compte [Netlify](https://netlify.com)
- Le domaine `formalita.fr` (accès DNS)

### Étape 1 : Créer le repo GitHub

1. Connecte-toi à GitHub
2. Crée un nouveau repository :
   - Nom : `formalita-landing` (ou ce que tu veux)
   - Visibilité : **Private** (recommandé)
   - Initialise SANS README (on a déjà les fichiers)

3. Clone le repo en local :
```bash
git clone https://github.com/TON-USERNAME/formalita-landing.git
cd formalita-landing
```

4. Copie les fichiers de ce dossier dans le repo

5. Push vers GitHub :
```bash
git add .
git commit -m "Initial commit - Landing page Formalita"
git push origin main
```

### Étape 2 : Déployer sur Netlify

1. Connecte-toi à [Netlify](https://app.netlify.com)
2. Clique sur **"Add new site"** → **"Import an existing project"**
3. Choisis **GitHub** et autorise l'accès
4. Sélectionne le repo `formalita-landing`
5. Configuration de build :
   - **Branch to deploy** : `main`
   - **Build command** : (laisser vide)
   - **Publish directory** : `.`
6. Clique **"Deploy site"**

✅ Ton site est en ligne sur une URL temporaire Netlify !

### Étape 3 : Connecter le domaine formalita.fr

1. Dans Netlify → **Site settings** → **Domain management**
2. Clique **"Add custom domain"**
3. Entre : `formalita.fr`
4. Netlify te donne des **serveurs DNS** à configurer

5. Va chez ton registrar (là où tu as acheté le domaine) et configure :
   - **Option A (recommandée)** : Change les NS (nameservers) vers Netlify
   - **Option B** : Ajoute un enregistrement CNAME ou A

6. Active **HTTPS** (Netlify le fait automatiquement avec Let's Encrypt)

### Étape 4 : Vérifier les formulaires

1. Dans Netlify → **Forms**
2. Tu verras le formulaire `contact` apparaître après le premier test
3. Les soumissions seront stockées ici

**Configurer les notifications email :**
1. **Forms** → **Form notifications** → **Add notification**
2. Choisis **Email notification**
3. Entre : `contact@formalita.fr`
4. Tu recevras un email à chaque nouvelle soumission !

---

## 📁 Structure des fichiers

```
formalita-landing/
├── index.html        # Page principale
├── success.html      # Page de confirmation après envoi
├── netlify.toml      # Configuration Netlify
└── README.md         # Ce fichier
```

---

## ✏️ Personnalisation

### Modifier le contenu

Édite directement `index.html` :
- **Textes** : Cherche et modifie les textes dans le HTML
- **Statistiques** : Section `.hero-stats` (98%, 48h, 500+)
- **Services** : Sections `#services-particuliers` et `#services-professionnels`

### Modifier les couleurs

Les couleurs sont définies en CSS variables au début du `<style>` :
```css
:root {
    --orange-primary: #F5A623;
    --blue-primary: #2B5F9E;
    /* ... */
}
```

### Ajouter un numéro de téléphone

Dans le footer, modifie :
```html
<div class="footer-contact-item">
    <span>📞</span>
    <span>04 XX XX XX XX</span>
</div>
```

---

## 📊 Formulaire Netlify

Le formulaire utilise **Netlify Forms** (gratuit jusqu'à 100 soumissions/mois).

**Champs capturés :**
- Prénom
- Nom
- Email
- Téléphone
- Profil (particulier/entreprise)
- Besoin (type de service)
- Message

**Protection anti-spam :**
- Honeypot field (champ caché)
- Netlify spam filter intégré

---

## 🔄 Mise à jour du site

1. Modifie les fichiers localement
2. Commit et push :
```bash
git add .
git commit -m "Description des changements"
git push
```
3. Netlify déploie automatiquement en ~30 secondes !

---

## 📱 Responsive

Le site est optimisé pour :
- ✅ Desktop (1200px+)
- ✅ Tablette (768px - 1024px)
- ✅ Mobile (< 768px)

---

## 🔒 Sécurité

- HTTPS automatique via Let's Encrypt
- Headers de sécurité configurés dans `netlify.toml`
- Protection honeypot contre le spam

---

## 📈 Prochaines étapes suggérées

- [ ] Ajouter Google Analytics / Plausible
- [ ] Créer une page Mentions Légales
- [ ] Créer une page Politique de Confidentialité
- [ ] Configurer Google Search Console
- [ ] Ajouter le pixel Facebook/LinkedIn si nécessaire

---

## 🆘 Support

En cas de problème :
- Documentation Netlify : https://docs.netlify.com
- Documentation GitHub : https://docs.github.com

---

**Créé le :** 05/12/2025  
**Par :** Projet Y - Groupe Yuki
