# Site de Confessions Anonymes - MVP

Un site web simple pour partager des confessions anonymes, avec modération et sécurité.

## Fonctionnalités

- Poster des confessions anonymes
- Lire les confessions des autres
- Liker et signaler les posts
- Modération via panneau admin
- Sécurité : rate limiting, sanitize, filtres automatiques

## Stack Technique

- Front-end : React + Tailwind CSS
- Back-end : Node.js + Express
- Base de données : MongoDB Atlas
- Déploiement : Vercel (front), Render (back)

## Installation

1. Cloner le repo
2. Installer les dépendances :
   ```
   cd client && npm install
   cd ../server && npm install
   ```
3. Configurer les variables d'environnement :
   - Créer `.env` dans `server/` :
     ```
     MONGODB_URI=mongodb+srv://...
     JWT_SECRET=votre_secret
     ```
4. Lancer le serveur :
   ```
   cd server && npm run dev
   ```
5. Lancer le front :
   ```
   cd client && npm start
   ```

## API Endpoints

### Posts
- `GET /api/posts` : Liste des posts
- `POST /api/posts` : Créer un post (body: {text, tags})
- `POST /api/posts/:id/like` : Liker un post
- `POST /api/posts/:id/report` : Signaler un post

### Admin
- `GET /api/admin/reports` : Liste des signalements (auth requise)
- `POST /api/admin/reports/:id` : Traiter un signalement

## Déploiement

1. **Back-end sur Render** :
   - Connecter le repo GitHub
   - Variables d'env : MONGODB_URI, JWT_SECRET
   - Build command : `npm install`
   - Start command : `npm start`

2. **Front-end sur Vercel** :
   - Connecter le repo
   - Build settings : root directory `client`
   - Variables : REACT_APP_API_URL=https://votre-api.render.com

## Sécurité

- Anonymat : pas d'email requis
- Sanitize input
- Rate limiting : 5 posts/heure/IP
- Filtres mots-clés pour contenu dangereux
- Logs minimaux, retention courte

## Conformité

- Avertissement pour urgences
- Politique de confidentialité incluse
- RGPD : minimiser les données collectées

## Tests

Utiliser Postman pour tester les endpoints.

## Contribution

Pour améliorer : ajouter pagination, commentaires, vraie reCAPTCHA, etc.
