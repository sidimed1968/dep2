# Guide de Déploiement

Cette application est prête à être déployée. Voici comment faire :

## Option 1 : Déploiement sur Vercel (Recommandé)

1. **Créer un compte** sur [Vercel](https://vercel.com).
2. **Importer le projet** :
   - Connectez votre compte GitHub/GitLab/Bitbucket.
   - Sélectionnez ce dépôt.
3. **Configuration** :
   - Framework Preset : `Vite`
   - Build Command : `npm run build`
   - Output Directory : `dist`
4. **Variables d'environnement** :
   - Ajoutez vos clés API si nécessaire (ex: `VITE_GEMINI_API_KEY`).
5. **Déployer** : Cliquez sur "Deploy".

## Option 2 : Déploiement sur Netlify

1. **Créer un compte** sur [Netlify](https://netlify.com).
2. **Ajouter un nouveau site** : "Import an existing project".
3. **Paramètres de build** :
   - Build command : `npm run build`
   - Publish directory : `dist`
4. **Déployer**.

## Note Importante - Routage (SPA)

Le fichier `vercel.json` est déjà configuré pour gérer le routage (Single Page Application). Si vous utilisez Netlify, créez un fichier `_redirects` dans le dossier `public` avec ce contenu :

```
/*  /index.html  200
```
