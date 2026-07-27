# Home Staging — Ingrid Molina

Site vitrine statique (HTML/CSS, aucun build). Domaine : mihomestaging.com (OVH, offre Perso, dossier racine `www/`).

## Déploiement — AUTOMATIQUE, ne jamais faire de FTP manuel

Un push sur `master` déclenche `.github/workflows/deploy.yml` qui synchronise tout le repo
vers `www/` sur l'hébergement OVH via FTP (identifiants dans les secrets GitHub du repo :
`FTP_SERVER`, `FTP_USERNAME`, `FTP_PASSWORD`).

**Règle permanente** : après toute modification du site (PC ou Mac), commit + push
immédiatement, sans attendre de confirmation explicite de l'utilisateur — c'est le
comportement voulu (déploiement continu). Toujours `git pull` avant de commencer à éditer.

```bash
git add -A && git commit -m "..." && git push
```

Vérifier le déploiement : `gh run list --repo raphG13/home-staging-ingrid-molina` ou
directement https://mihomestaging.com après ~1 min.

## Structure
- `index.html`, `cgv.html`, `style.css` — le site
- `assets/` — images (portraits, avant/après, textures)
- `_archive_services_avant_experiences.html` — brouillon archivé, pas utilisé par le site

## Autre domaine sur le même hébergement OVH
`minsidebook.com` est réservé à un futur projet ebook, distinct de ce site — ne pas y toucher.
