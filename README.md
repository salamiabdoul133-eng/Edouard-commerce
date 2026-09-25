# Édouard Commerce

Site web vitrine pour **Édouard Commerce** - Achat et vente de produits agricoles (Soja, Karité, Cacao, Acadjou, Sésame) au Bénin et Togo.

## 🌐 Fonctionnalités SEO

- **Meta tags optimisés** : description, keywords, author, robots
- **Open Graph** : partage optimal sur Facebook, LinkedIn, WhatsApp
- **Twitter Cards** : affichage enrichi sur X/Twitter
- **Schema.org (JSON-LD)** : données structurées pour Google (LocalBusiness, Product, OfferCatalog)
- **Sitemap.xml** : indexation facilitée pour les moteurs de recherche
- **Robots.txt** : directives pour les crawlers
- **Manifest.json** : support PWA (Progressive Web App)
- **Canonical URL** : évite le contenu dupliqué
- **Hreflang** : ciblage linguistique (français)
- **Images optimisées** : alt text, lazy loading, formats WebP

## 📁 Structure du projet

```
Edouard-commerce/
├── index.html          # Page principale
├── sitemap.xml         # Plan de site pour SEO
├── robots.txt          # Directives pour crawlers
├── manifest.json       # Configuration PWA
├── package.json        # Dépendances (optionnel)
└── Images/             # Assets visuels
    ├── magasin_cacao.webp
    ├── sac_soja.webp
    ├── camion_karité.webp
    ├── Acadjou.jpeg
    ├── Sésame.png
    └── transport.webp
```

## 🚀 Déploiement

### Prérequis
- Remplacez `https://edouard-commerce.com/` par votre vrai domaine dans :
  - `index.html` (canonical, og:url, twitter:url, Schema.org)
  - `sitemap.xml`
  - `robots.txt` (Sitemap URL)

### Hébergement statique recommandé
- **Netlify** : `npm install -g netlify-cli && netlify deploy`
- **Vercel** : `npm install -g vercel && vercel`
- **GitHub Pages** : push sur branch `gh-pages`
- **Firebase Hosting** : `firebase deploy`
- **Cloudflare Pages** : connectez le repo GitHub

### Configuration serveur (Apache/Nginx)

**Apache (.htaccess)** :
```apache
# Compression
<IfModule mod_deflate.c>
  AddOutputFilterByType DEFLATE text/html text/css application/json application/javascript
</IfModule>

# Cache
<IfModule mod_expires.c>
  ExpiresActive On
  ExpiresByType image/webp "access plus 1 year"
  ExpiresByType image/png "access plus 1 year"
  ExpiresByType text/css "access plus 1 month"
  ExpiresByType application/javascript "access plus 1 month"
</IfModule>

# Security headers
<IfModule mod_headers.c>
  Header set X-Content-Type-Options "nosniff"
  Header set X-Frame-Options "SAMEORIGIN"
  Header set Referrer-Policy "strict-origin-when-cross-origin"
</IfModule>
```

**Nginx** :
```nginx
# Cache static assets
location ~* \.(webp|png|jpg|jpeg|gif|ico|css|js)$ {
    expires 1y;
    add_header Cache-Control "public, immutable";
}

# Security headers
add_header X-Content-Type-Options nosniff;
add_header X-Frame-Options SAMEORIGIN;
add_header Referrer-Policy strict-origin-when-cross-origin;

# Gzip
gzip on;
gzip_types text/css application/javascript application/json;
```

## 📱 Contact WhatsApp

Tous les boutons mènent vers : `https://wa.me/+2290197642426`

## ✅ Checklist SEO avant mise en production

- [ ] Remplacer `https://edouard-commerce.com/` par le vrai domaine
- [ ] Vérifier que toutes les images existent dans `/Images/`
- [ ] Soumettre le sitemap à Google Search Console
- [ ] Soumettre le sitemap à Bing Webmaster Tools
- [ ] Configurer Google Analytics / Matomo
- [ ] Tester avec [Rich Results Test](https://search.google.com/test/rich-results)
- [ ] Tester avec [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)
- [ ] Tester avec [Twitter Card Validator](https://cards-dev.twitter.com/validator)
- [ ] Vérifier la vitesse avec [PageSpeed Insights](https://pagespeed.web.dev/)

## 📞 Contact

**Édouard ADJAGOUDOU**
- WhatsApp : +229 01 97 64 24 26
- Pays : Bénin & Togo

---

© 2026 Édouard Commerce - Tous droits réservés.