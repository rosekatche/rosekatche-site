# rosekatche.com

Site vitrine statique (une page, HTML/CSS/JS pur, pas de framework). Prêt à déployer.

## Structure
- `index.html` — toute la page
- `images/` — les 9 photos du site, en fichiers séparés (plus de base64 inline)

## Déploiement (GitHub → Cloudflare Pages → OVH)

1. **GitHub** : créer un nouveau dépôt (ex. `rosekatche-site`), y pousser ces fichiers tels quels (`index.html` + `images/`) à la racine.
2. **Cloudflare Pages** : connecter ce dépôt GitHub. Pas de build command nécessaire (site statique) — laisser le dossier de sortie sur `/` (racine). Cloudflare déploie automatiquement à chaque push.
3. **Domaine (OVH → Cloudflare)** :
   - Dans OVH, changer les serveurs DNS du domaine pour ceux fournis par Cloudflare (Cloudflare les affiche lors de l'ajout du domaine).
   - Dans Cloudflare Pages, section "Custom domains", ajouter `rosekatche.com` (et `www.rosekatche.com` si voulu).
   - La propagation DNS peut prendre de quelques minutes à 24h.

## À vérifier après mise en ligne
- Le bouton FR/EN en haut à droite
- Les liens Vimeo (mot de passe sur demande par mail)
- L'affichage sur mobile (le site est déjà responsive, mais toujours bon de vérifier en vrai)
