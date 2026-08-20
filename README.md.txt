# MOVECOIN

Jeu plateforme 2D (React + Canvas) avec **Oasis** : monde parallèle, PNJ autonomes, commerce, VIP, comptes joueurs.

Fichier unique : `index.html` (tout est inclus — pas de build complexe).

## Avatars

- Spectre, Robot, Ninja, Alien, Chat, Crâne, Mage, Cosmonaute
- **Musclé** 💪 — avatar mâle torse large
- **Pretty** 💋 — avatar femme, visage soft, grosses lèvres

## Lancer en local

Ouvre simplement `index.html` dans un navigateur, **ou** :

```bash
npx serve .
```

## GitHub

```bash
cd movecoin-deploy
git init
git add .
git commit -m "MOVECOIN v4 — Oasis + avatars"
git branch -M main
git remote add origin https://github.com/TON_USER/movecoin.git
git push -u origin main
```

## Render

### Option A — Static Site (recommandé)

1. [render.com](https://render.com) → **New +** → **Static Site**
2. Connecte le repo GitHub
3. Réglages :
   - **Build Command** : laisse vide ou `echo static`
   - **Publish Directory** : `.` (racine)
4. Deploy

### Option B — Blueprint

Si le repo contient `render.yaml` :

1. **New +** → **Blueprint**
2. Sélectionne le repo
3. Render lit `render.yaml` et déploie

### Option C — Web Service Node

1. **New +** → **Web Service**
2. Runtime : Node
3. Build : _(vide)_
4. Start : `npx serve -s . -l $PORT`
5. Deploy

## Comptes & données

- Comptes, scores, oasis : **localStorage** du navigateur
- Mode secret (33 clics silencieux sur le logo) : coffre admin
- Salle détente / Oasis : **compte requis**

## Structure

```
movecoin-deploy/
├── index.html      # jeu complet
├── package.json    # scripts optionnels
├── render.yaml     # blueprint Render
├── README.md
└── .gitignore
```
