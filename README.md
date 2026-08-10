# Gestion BHDS — Application de bureau (Electron)

Ceci transforme `index.html` (ton app Gestion Scolaire BHDS) en un vrai logiciel installable
sur Windows, Mac et Linux, construit automatiquement par GitHub — sans que tu aies besoin
d'installer quoi que ce soit sur ton PC.

## 1. Mettre ce projet sur GitHub

1. Crée un nouveau dépôt (repository) sur GitHub, par exemple `gestion-bhds`.
   - Peut être privé (recommandé) ou public.
2. Sur ton PC, ouvre un terminal dans ce dossier et tape :

git init
git add .
git commit -m "Version initiale de l'app Gestion BHDS"
git branch -M main
git remote add origin https://github.com/TON-COMPTE/gestion-bhds.git
git push -u origin main

Remplace TON-COMPTE par ton nom d'utilisateur GitHub.

## 2. Lancer la construction automatique (build)

git tag v1.0.0
git push origin v1.0.0

Ensuite :
1. Va sur ton dépôt GitHub → onglet Actions → tu verras le build tourner (environ 5-10 min).
2. Une fois terminé, va dans l'onglet Releases : tu trouveras v1.0.0 avec les 3 installateurs.

## 3. Mettre à jour l'application plus tard

git add .
git commit -m "Description de ce qui a changé"
git push
git tag v1.0.1
git push origin v1.0.1

## 4. Tester en local avant de publier (optionnel)

npm install
npm start

## Structure du projet

- index.html — ton application
- main.js — le "cerveau" Electron
- package.json — config du nom de l'app, icône, et installateurs
- build/icon.png — icône de l'app
- .github/workflows/build.yml — recette de construction GitHub
