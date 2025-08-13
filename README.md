# Promptopia ✨🧠

[![Next.js](https://img.shields.io/badge/Next.js-14.2-black?logo=nextdotjs)](https://nextjs.org)
[![React](https://img.shields.io/badge/React-18-149eca?logo=react)](https://react.dev)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-3.4-38bdf8?logo=tailwindcss)](https://tailwindcss.com)
[![NextAuth.js](https://img.shields.io/badge/Auth-NextAuth.js-2596be)](https://next-auth.js.org)
[![MongoDB](https://img.shields.io/badge/DB-MongoDB-4ea94b?logo=mongodb)](https://www.mongodb.com)
[![Mongoose](https://img.shields.io/badge/ODM-Mongoose-880000)](https://mongoosejs.com)

Application Next.js pour explorer, créer, éditer et partager des prompts. Authentification avec NextAuth, stockage des données dans MongoDB via Mongoose, et UI stylée avec Tailwind CSS.

---

## Sommaire 📚

- [Aperçu](#aperçu-)
- [Fonctionnalités](#fonctionnalités-)
- [Stack technique](#stack-technique-)
- [Prérequis](#prérequis-)
- [Installation](#installation-)
- [Configuration (env)](#configuration-env-)
- [Lancer le projet](#lancer-le-projet-)
- [Scripts NPM](#scripts-npm-)
- [Arborescence](#arborescence-)
- [Qualité & conventions](#qualité--conventions-)
- [FAQ](#faq-)
- [Roadmap](#roadmap-)
- [Contribuer](#contribuer-)
- [Auteur](#auteur-)

---

## Aperçu 👀

- Parcourez un flux de prompts inspirants.
- Recherchez par mot-clé ou tag.
- Créez, mettez à jour et supprimez vos prompts.
- Connectez-vous pour gérer votre profil et votre bibliothèque.
- Interface moderne avec App Router et Tailwind. ✨

---

## Fonctionnalités ✨

- 🔐 Authentification via NextAuth.js (sessions sécurisées)
- 🗃️ Persistance MongoDB avec Mongoose
- 📝 CRUD complet sur les prompts
- 🏷️ Recherche par tags et texte
- 📋 Copier le prompt en un clic
- 🌙 Thème moderne avec Tailwind CSS
- ⚡ SSR/ISR avec Next.js App Router

---

## Stack technique 🧰

- Framework: Next.js 14 (App Router)
- Langage: JavaScript (jsconfig)
- UI: React 18, Tailwind CSS 3.4, PostCSS 8
- Auth: NextAuth.js v4
- Base de données: MongoDB + Mongoose v8
- Divers: bcrypt (hash des mots de passe si Credentials)

---

## Prérequis ✅

- Node.js ≥ 18
- Une instance MongoDB (Atlas ou locale)
- Variables d’environnement pour NextAuth et MongoDB

---

## Installation 🛠️

```bash
git clone https://github.com/Okpeyemi/project_promptopia.git
cd project_promptopia
npm ci   # ou: npm install
```

---

## Configuration (env) 🔐

Créez un fichier `.env.local` à la racine avec, par exemple:

```bash
# Base URL de l'application
NEXTAUTH_URL=http://localhost:3000

# Secret NextAuth (générez-le: openssl rand -base64 32)
NEXTAUTH_SECRET=changeme

# Connexion MongoDB
MONGODB_URI=mongodb+srv://<user>:<password>@<cluster>/<db>?retryWrites=true&w=majority

# Optionnel: si vous utilisez un provider OAuth (ex: Google)
# GOOGLE_CLIENT_ID=
# GOOGLE_CLIENT_SECRET=
```

Notes:
- Ne commitez jamais `.env.local`.
- Si vous utilisez un provider Credentials, bcrypt est utilisé pour le hachage des mots de passe.

---

## Lancer le projet ▶️

Développement:
```bash
npm run dev
# http://localhost:3000
```

Build + production locale:
```bash
npm run build
npm start
# http://localhost:3000
```

---

## Scripts NPM 📜

```json
{
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "next lint"
}
```

- ▶️ dev: serveur de développement
- 🏗️ build: build production
- 🚀 start: serveur en production
- 🧹 lint: ESLint

---

## Arborescence 🌳

Aperçu des principaux éléments:

```
.
├─ app/                       # Routes App Router (pages, API routes)
├─ components/                # Composants UI réutilisables
├─ models/                    # Schémas Mongoose
├─ utils/                     # Helpers (ex: connexion MongoDB, etc.)
├─ public/                    # Assets statiques
├─ styles/                    # Styles globaux/Tailwind
├─ next.config.mjs
├─ tailwind.config.js
├─ postcss.config.mjs
├─ jsconfig.json              # Aliases/paths JS
├─ package.json
└─ README.md
```

---

## Qualité & conventions 🧹

- ESLint avec configuration Next.js → `npm run lint`
- Tailwind CSS 3.4 + PostCSS 8
- Organisation en modules: composants, modèles, utilitaires
- Bonnes pratiques:
  - Centralisez la connexion MongoDB (singleton)
  - Validez les entrées côté serveur sur les API routes
  - Ne stockez jamais de secrets côté client

---

## FAQ ❓

- Quelle version de Node utiliser ?
  - Node 18+ (recommandé: Node 20)
- Base de données requise ?
  - Oui, MongoDB via `MONGODB_URI`
- Le projet utilise TypeScript ?
  - Non, JavaScript avec `jsconfig.json`

---

## Roadmap 🗺️

- [ ] 🔎 Recherche avancée (filtres multi-tags)
- [ ] 🧑‍💻 Rôles/permissions (modération)
- [ ] 💾 Persistance des favoris
- [ ] 🧪 Tests (unitaires + e2e)
- [ ] ♿ Accessibilité & SEO
- [ ] 🌐 i18n

---

## Contribuer 🤝

Les contributions sont les bienvenues !

1. 🍴 Fork
2. 🌱 Branche: `git checkout -b feat/ma-fonctionnalite`
3. 💬 Commit: `git commit -m "feat: ajoute ma fonctionnalité"`
4. ⤴️ Push: `git push origin feat/ma-fonctionnalite`
5. 🔄 PR: ouvrez une Pull Request

---

## Auteur 👤

- GitHub: [@Okpeyemi](https://github.com/Okpeyemi)
