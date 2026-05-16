# Audit Tool — Guide de déploiement

## 1. Configurer le Client ID Google

Dans `index.html`, ligne ~170, remplace :
```
CLIENT_ID: 'REMPLACE_PAR_TON_CLIENT_ID.apps.googleusercontent.com',
```
par ton vrai Client ID OAuth (celui qui finit en `.apps.googleusercontent.com`).

## 2. Déployer sur GitHub Pages

1. Crée un repo GitHub (ex: `audit-tool`)
2. Upload tous les fichiers de ce dossier
3. Settings → Pages → Source: `main` branch → `/root`
4. Ton URL sera : `https://TON-COMPTE.github.io/audit-tool`

## 3. Ajouter l'URL dans Google Cloud Console

1. Console Cloud → APIs & Services → Identifiants → ton Client OAuth
2. **Origines JavaScript autorisées** → ajoute :
   - `https://TON-COMPTE.github.io`
3. **URI de redirection autorisées** → ajoute :
   - `https://TON-COMPTE.github.io/audit-tool`
4. Enregistrer

## 4. Icônes (optionnel)

Génère deux icônes PNG et place-les à la racine :
- `icon-192.png` (192×192)
- `icon-512.png` (512×512)

Tu peux utiliser https://favicon.io/favicon-generator/ avec le texte "A".

## 5. Partager avec l'équipe

Envoie juste l'URL GitHub Pages à ton équipe.
- Ils se connectent avec leur compte @getapony
- Sur mobile : "Partager → Sur l'écran d'accueil" pour l'installer

## Structure Drive

Les audits sont stockés dans le dossier Drive `Audit V7` :
```
Audit V7/
  grilles.json                    ← grilles partagées entre tous
  Lyon-Nord — 16/05/2025/
    rapport.json                  ← résultats complets
    c1_photo1.jpg                 ← photos par critère
    c2_photo1.jpg
  Bordeaux — 17/05/2025/
    ...
```
