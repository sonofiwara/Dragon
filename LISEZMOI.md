# Détecteur d'Orbes — APK Android

Ce dossier contient l'app Android complète. GitHub la compile pour toi :
aucun outil à installer sur ton PC.

## Obtenir l'APK (environ 10 minutes la première fois)

1. Crée un compte sur https://github.com si tu n'en as pas.
2. Crée un nouveau dépôt (bouton **New**), nomme-le par ex. `detecteur-orbes`. Laisse-le vide.
3. Sur la page du dépôt vide, clique **uploading an existing file**, puis glisse
   **le contenu** de ce dossier (pas le dossier lui-même). Vérifie que le dossier
   caché `.github` est bien inclus (sur Windows/Mac, affiche les fichiers cachés),
   puis **Commit changes**.
   > Si `.github` ne passe pas par le glisser-déposer : clique **Add file > Create new file**,
   > tape le nom `.github/workflows/build-apk.yml` et colle le contenu du fichier.
4. Onglet **Actions** : la compilation « Compiler l'APK » démarre (environ 5 min).
   Si GitHub demande d'activer les workflows, accepte.
5. Quand elle est verte, va dans **Releases** (colonne de droite de la page du dépôt) :
   le fichier `detecteur-orbes.apk` s'y trouve. Ouvre cette page depuis ton téléphone
   pour le télécharger directement.

## Installer sur le téléphone

- Ouvre l'APK téléchargé. Android demande d'autoriser l'installation depuis le
  navigateur ou le gestionnaire de fichiers : accepte pour cette source.
- Au premier lancement, touche « Allumer le détecteur » et accepte la localisation
  (choisis « Position exacte »).

C'est un APK « debug » : parfait pour toi et tes proches, mais pas pour le Play Store
(il faudrait une clé de signature dédiée).

## Modifier l'app

Le code de l'app est dans `www/index.html`. Après une modification, renvoie le fichier
sur GitHub : un nouvel APK est compilé automatiquement.

Pour compiler sur ton PC à la place : installe Node 20 et Android Studio, puis
`npm ci`, `npx cap sync android`, et ouvre le dossier `android` dans Android Studio.
