# 🐍 Snake 3D

Un Snake old-school inspiré du Nokia, revisité en 3D avec Three.js.
Une seule page HTML statique — zéro dépendance, zéro build, déployable directement sur GitHub Pages.

---

## Aperçu

![Snake 3D](https://paullux.github.io/snake3d/)

- Terrain 3D avec éclairage et ombres
- Corps du serpent continu (tube + sphères)
- Pommes réalistes avec tige, feuille et reflet
- Caméra perspective adaptive (portrait et paysage)
- Accélération progressive au fil des pommes mangées
- Classement mondial via Firebase Realtime Database *(optionnel)*

---

## Jouer

**En ligne :** [paullux.github.io/snake3d](https://paullux.github.io/snake3d/)

**En local :**
```bash
# avec Node.js
npx serve .
# ou ouvrir index.html directement dans le navigateur
```

---

## Contrôles

| Dispositif | Commande |
|---|---|
| Clavier | Flèches directionnelles ou WASD |
| Mobile / Tablette | Swipe dans la direction souhaitée |
| D-pad tactile | Boutons affichés en bas à gauche |
| Démarrer / Rejouer | Entrée, Espace ou bouton PLAY |

---

## Classement mondial (Firebase)

Le classement est optionnel. Sans configuration, le jeu fonctionne normalement avec un meilleur score local.

Pour l'activer :

1. Créer un projet sur [console.firebase.google.com](https://console.firebase.google.com)
2. Ajouter une **Realtime Database** (mode test)
3. Copier l'URL de la base (ex. `https://mon-projet-default-rtdb.firebaseio.com`)
4. Dans `index.html`, remplacer la ligne :
   ```js
   const FIREBASE_URL = '';
   ```
   par :
   ```js
   const FIREBASE_URL = 'https://mon-projet-default-rtdb.firebaseio.com';
   ```

Les 10 meilleurs scores mondiaux sont affichés après chaque partie. Si le joueur entre dans le Top 10, son pseudo lui est demandé.

---

## Stack technique

| Élément | Détail |
|---|---|
| Rendu 3D | [Three.js r155](https://threejs.org/) via CDN |
| Backend scores | Firebase Realtime Database (REST, sans SDK) |
| Score local | `localStorage` |
| Déploiement | GitHub Pages (fichier unique `index.html`) |

---

## Licence

[MIT](LICENSE.md) — © 2026 Paullux
