# AnimeVerse

An anime discovery platform where users can search for anime, view detailed
information, create an account, log in securely, and save favorite anime to
their own account.

## Tech stack

- React 19 + Vite
- React Router DOM
- Firebase Authentication (email/password) + Firestore (favorites storage)
- Jikan REST API (https://api.jikan.moe) via Axios

## Getting started

```bash
npm install
npm run dev
```

### Environment variables

Create a `.env` file in the project root (never commit this file) with your
Firebase project's web config:

```
VITE_FIREBASE_API_KEY=AIzaSyACflUcHAAOjemMIROQ9AFygdY3DET1yMQ
VITE_FIREBASE_AUTH_DOMAIN=animeverse-97b32.firebaseapp.com
VITE_FIREBASE_DATABASE_URL=https://animeverse-97b32-default-rtdb.asia-southeast1.firebasedatabase.app
VITE_FIREBASE_PROJECT_ID=animeverse-97b32
VITE_FIREBASE_STORAGE_BUCKET=animeverse-97b32.firebasestorage.app
VITE_FIREBASE_MESSAGING_SENDER_ID=917115972934
VITE_FIREBASE_APP_ID=1:917115972934:web:ac19c3da3f6744195dc947
VITE_FIREBASE_MEASUREMENT_ID=G-YL1WGDN74C
```

### Firestore security rules

Favorites are stored at `users/{uid}/favorites/{animeId}`. Apply this rule in
the Firebase console (Firestore → Rules) so each user can only read/write
their own favorites:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /users/{userId}/favorites/{favoriteId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
  }
}
```

## Available scripts

- `npm run dev` — start the local dev server
- `npm run build` — production build to `dist/`
- `npm run preview` — preview the production build locally
- `npm run lint` — run ESLint

## Project structure

```
src/
  components/   reusable UI components (cards, states, layout)
  pages/        route-level page components
  services/     API/Firestore access + data-mapping helpers
  hooks/        reusable hooks (auth, favorites)
  context/      React context providers
  firebase/     Firebase app initialization
```
