# TODO - MVP Site de Confessions Anonymes

## 1. Structure du Projet
- [x] Créer dossiers : client/, server/, shared/
- [x] Initialiser package.json pour client et server

## 2. Front-end (React + Tailwind)
- [x] Installer React, Tailwind CSS, Axios
- [x] Créer App.js avec routing (React Router)
- [x] Composant PostList : afficher liste posts paginée
- [x] Composant PostItem : afficher post individuel avec like, report
- [x] Composant CreatePostForm : formulaire pour poster confession
- [x] Page Admin : vue modérateur (protégée)
- [x] Intégrer reCAPTCHA pour formulaire (simulé)

## 3. Back-end (Express + MongoDB)
- [x] Installer Express, Mongoose, bcrypt, jsonwebtoken, express-rate-limit, helmet
- [x] Configurer connexion MongoDB Atlas
- [x] Modèle Post : id, text, tags, createdAt, likes, commentsCount, status
- [x] Modèle Report : postId, reason, notes, handled
- [x] Routes /api/posts : GET (liste), POST (créer)
- [x] Routes /api/posts/:id/like : POST
- [x] Routes /api/posts/:id/report : POST
- [x] Routes /api/admin/reports : GET (auth)
- [x] Middleware : rate limiting, sanitize, CORS, auth JWT pour admin

## 4. Sécurité et Conformité
- [x] Implémenter sanitize input (DOMPurify côté front, validator côté back)
- [x] Rate limiting : 5 posts par heure par IP
- [x] Filtres automatiques : mots-clés pour contenu dangereux
- [x] Logs minimaux : retention 7 jours, hash IPs
- [x] Ressources aide : afficher liens urgences si mots-clés détectés
- [x] Politique confidentialité et CGU : pages statiques

## 5. Tests et Déploiement
- [ ] Tester endpoints avec Postman
- [ ] Tester UI : poster, lire, like, report
- [ ] Configurer Vercel pour front, Render pour back
- [ ] Instructions déploiement dans README.md

## 6. Finalisation
- [x] README.md avec setup, API docs, déploiement
- [x] Vérifier RGPD et avertissements légaux

## 7. Extensions
- [x] Ajouter page de connexion (pour admin)
- [x] Améliorer design : thème sombre, responsive, logo "WAKH NIOU"
- [x] Intégrer mode de paiement (Stripe pour dons)
- [x] Créer pages détachées : Politique, CGU, Aide
- [x] Ajouter inscription/connexion utilisateur (fin de l'anonymat)
- [ ] Tester extensions
- [ ] Déployer version finale
