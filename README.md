# 🚀 GUIDE DE DÉPLOIEMENT - SITE INSTITUT AL MUTA'ALLIM

## 📁 STRUCTURE DU SITE MULTI-PAGES

```
almutaallim-website/
│
├── index.html              # Page d'accueil (mise à jour avec nouveaux tarifs)
├── bibliotheque.html       # Page Bibliothèque Numérique
├── blog.html               # Page Blog/Articles
├── newsletter.html         # Page Newsletter
│
├── css/
│   └── style.css          # Styles CSS centralisés
│
├── js/
│   └── main.js            # JavaScript principal
│
├── assets/
│   ├── logo.png           # Logo principal
│   └── images/            # Autres images
│
└── README.md              # Ce fichier
```

---

## ✅ ÉTAPE 1 : PRÉPARER LES FICHIERS

### 1.1 Télécharger tous les fichiers

Vous avez reçu :
- ✅ `index-v2.html` (page d'accueil avec tarifs mis à jour)
- ✅ `bibliotheque.html`
- ✅ `blog.html`
- ✅ `newsletter.html`
- ✅ `css/style.css`
- ✅ `js/main.js`

### 1.2 Renommer le fichier principal

```bash
index-v2.html  →  index.html
```

### 1.3 Organiser les dossiers

Créez cette structure :
```
votre-site/
├── index.html
├── bibliotheque.html
├── blog.html
├── newsletter.html
├── css/
│   └── style.css
├── js/
│   └── main.js
└── assets/
    └── logo.png
```

---

## 📤 ÉTAPE 2 : DÉPLOYER SUR NETLIFY

### Option A : Drag & Drop (LA PLUS SIMPLE)

1. **Allez sur** https://app.netlify.com/
2. **Connectez-vous** avec votre compte (ou créez-en un)
3. **Glissez-déposez** TOUT le dossier `almutaallim-website/` sur Netlify
4. **Attendez** le déploiement (30 secondes)
5. **Votre site est en ligne !** 🎉

URL temporaire : `https://random-name-123.netlify.app`

### Option B : Via Git (Plus professionnel)

1. **Créez un dépôt GitHub** avec vos fichiers
2. **Sur Netlify** : "New site from Git"
3. **Connectez GitHub**
4. **Sélectionnez** votre dépôt
5. **Deploy !**

---

## 🌐 ÉTAPE 3 : CONFIGURER VOTRE NOM DE DOMAINE

### 3.1 Sur Netlify (Gratuit)

1. Site settings → Domain management
2. "Add custom domain"
3. Entrez : `almutaallim.dz` (ou `.com`, `.fr`)
4. Netlify vous donne les paramètres DNS

### 3.2 Chez votre registrar (ex: DZWebHost)

Ajoutez ces enregistrements DNS :

```
Type: A
Name: @
Value: 75.2.60.5 (IP Netlify)

Type: CNAME
Name: www
Value: votre-site.netlify.app
```

⏰ **Délai de propagation :** 24-48h

---

## 🔧 ÉTAPE 4 : PERSONNALISATION

### 4.1 Mettre votre logo

1. **Remplacez** `assets/logo.png` par votre logo
2. **Dimensions recommandées :** 400x400px, fond transparent
3. **Format :** PNG

### 4.2 Ajouter de vrais témoignages

Dans `index.html`, section `#temoignages` :

```html
<div class="testimonial-card reveal">
    <p class="testimonial-text">
        "Votre vrai témoignage ici..."
    </p>
    <div class="testimonial-author">
        <div class="author-avatar">A</div>
        <div class="author-info">
            <h4>Amina S.</h4>
            <p>Étudiante en Fiqh</p>
        </div>
    </div>
</div>
```

### 4.3 Ajouter le Planner Ramadan

1. **Créez** un dossier `downloads/` à la racine
2. **Ajoutez** `planner-ramadan.pdf`
3. **Dans** `blog.html` ou page ressources :

```html
<a href="downloads/planner-ramadan.pdf" download class="btn-primary">
    📥 Télécharger le Planner Ramadan
</a>
```

### 4.4 Créer de vrais articles

1. **Copiez** `blog.html`
2. **Renommez** → `article-science-islam.html`
3. **Modifiez** le contenu
4. **Répétez** pour chaque article

---

## 📝 ÉTAPE 5 : CRÉER DES ARTICLES DE BLOG

### Template d'article

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Titre de l'article - Institut Al Muta'allim</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <!-- Copier la navbar de index.html -->
    
    <article class="blog-article">
        <header>
            <h1>Titre de votre article</h1>
            <div class="article-meta">
                <span>Par SOIFI Stamadati</span>
                <span>05 Février 2026</span>
            </div>
        </header>
        
        <div class="article-content">
            <p>Votre contenu ici...</p>
        </div>
    </article>
    
    <!-- Copier le footer de index.html -->
</body>
</html>
```

---

## 📊 ÉTAPE 6 : CONFIGURER LA NEWSLETTER (OPTIONNEL)

### Option A : Mailchimp (Gratuit jusqu'à 500 abonnés)

1. **Créez un compte** sur https://mailchimp.com
2. **Créez une liste**
3. **Générez un formulaire**
4. **Remplacez** le formulaire dans `newsletter.html`

### Option B : Sendinblue

1. **Créez un compte** sur https://www.sendinblue.com
2. **API Key** → Intégration
3. **Formulaire personnalisé**

---

## 🔐 ÉTAPE 7 : SÉCURITÉ & OPTIMISATION

### 7.1 Activer HTTPS

Sur Netlify :
1. Domain settings
2. "Force HTTPS" → ON
3. ✅ Certificat SSL automatique

### 7.2 Optimiser les images

```bash
# Compresser vos images avant upload
# Outil : https://tinypng.com/
```

### 7.3 Ajouter Google Analytics (optionnel)

Dans `<head>` de toutes les pages :

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 📈 ÉTAPE 8 : SEO (Référencement)

### 8.1 Chaque page doit avoir :

```html
<meta name="description" content="Description unique de la page">
<meta name="keywords" content="mots, clés, pertinents">
<title>Titre unique - Institut Al Muta'allim</title>
```

### 8.2 Créer un sitemap.xml

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://votre-site.com/</loc>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://votre-site.com/bibliotheque.html</loc>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://votre-site.com/blog.html</loc>
    <changefreq>weekly</changefreq>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://votre-site.com/newsletter.html</loc>
    <changefreq>monthly</changefreq>
    <priority>0.7</priority>
  </url>
</urlset>
```

### 8.3 Créer robots.txt

```
User-agent: *
Allow: /

Sitemap: https://votre-site.com/sitemap.xml
```

---

## 🎨 ÉTAPE 9 : FUTURES AMÉLIORATIONS

### Dans 1-2 mois :

- ✅ Système de paiement en ligne (Stripe, PayPal)
- ✅ Espace membre avec connexion
- ✅ Calendrier de réservation intégré
- ✅ Chat en direct (Tawk.to gratuit)
- ✅ Formulaires de contact avancés (Formspree)

---

## 🆘 DÉPANNAGE

### Problème : Le CSS ne se charge pas

**Solution :**
```html
<!-- Vérifiez que le chemin est correct -->
<link rel="stylesheet" href="css/style.css">

<!-- Pas : -->
<link rel="stylesheet" href="/css/style.css">
```

### Problème : Les liens internes ne marchent pas

**Solution :**
```html
<!-- Utilisez des chemins relatifs -->
<a href="bibliotheque.html">Bibliothèque</a>

<!-- Pas : -->
<a href="/bibliotheque.html">Bibliothèque</a>
```

### Problème : Le logo ne s'affiche pas

**Solution :**
1. Vérifiez que `logo.png` est dans `assets/`
2. Vérifiez le chemin : `<img src="assets/logo.png">`

---

## 📞 SUPPORT

Si vous avez besoin d'aide :

1. **Documentation Netlify :** https://docs.netlify.com
2. **Tutoriels YouTube :** "Netlify deployment tutorial"
3. **Forum Netlify :** https://answers.netlify.com

---

## ✅ CHECKLIST FINALE

Avant de lancer officiellement :

- [ ] Tous les fichiers uploadés sur Netlify
- [ ] Logo remplacé
- [ ] Tous les liens testés (navigation, formulaires)
- [ ] Témoignages réels ajoutés
- [ ] WhatsApp button testé
- [ ] Formulaires de contact testés
- [ ] Version mobile testée
- [ ] HTTPS activé
- [ ] Nom de domaine configuré (si applicable)
- [ ] Google Analytics ajouté (optionnel)
- [ ] Sitemap.xml créé
- [ ] robots.txt créé

---

## 🎉 FÉLICITATIONS !

Votre site est maintenant professionnel et prêt à accueillir vos élèves ! 

**URL actuelle :** https://al-mutaallim-institute.netlify.app/

**Prochaine étape :** Communiquer sur vos réseaux sociaux ! 📱

---

© 2026 Institut Al Muta'allim™ - Université Islamique de Prestige
```

---

**Bon courage pour le déploiement ! 🚀**

Si vous avez des questions, n'hésitez pas ! 💪
