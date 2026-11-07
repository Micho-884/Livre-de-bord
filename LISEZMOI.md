# Livre de bord – Sorties voile

Application autonome (sans compte, sans Claude) pour iPhone et Android.
Les données restent **sur votre téléphone**. Elle fonctionne **hors ligne** une fois installée.

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `index.html` | L'application |
| `manifest.webmanifest` | Nom, couleurs et icône pour l'installation |
| `sw.js` | Fonctionnement hors ligne |
| `icon-180.png`, `icon-192.png`, `icon-512.png` | Icônes |

## 1. Mettre l'application en ligne (une seule fois, gratuit)

Pour s'installer sur un téléphone, l'application doit être servie par une adresse **https**.

**Option la plus simple : Netlify Drop**
1. Sur un ordinateur, dézippez le dossier `livre-de-bord`.
2. Allez sur https://app.netlify.com/drop
3. Glissez-déposez le dossier `livre-de-bord` dans la page.
4. Netlify vous donne une adresse du type `https://nom-au-hasard.netlify.app`.
   Créez un compte gratuit pour que le site ne soit pas supprimé, et vous pourrez renommer l'adresse.

**Autre option : GitHub Pages**
1. Créez un dépôt sur GitHub et envoyez-y les fichiers du dossier.
2. Paramètres du dépôt → *Pages* → Source : branche `main`, dossier `/ (root)`.
3. L'adresse sera `https://votre-nom.github.io/nom-du-depot/`.

Personne ne voit vos données : le site ne contient que l'application, pas vos sorties.

## 2. Installer sur le téléphone

Ouvrez l'adresse obtenue sur le téléphone, puis :

- **iPhone** (dans Safari obligatoirement) : bouton Partager → **« Sur l'écran d'accueil »** → Ajouter.
- **Android** (Chrome) : menu ⋮ → **« Installer l'application »** ou « Ajouter à l'écran d'accueil ».

L'icône apparaît avec vos autres apps. Ouvrez-la une première fois avec du réseau ; ensuite elle fonctionne en mer, sans connexion.

## 3. Sauvegarder et restaurer

Onglet **Sauvegarde** :

- **Sauvegarder les données** : crée un fichier `livre-de-bord-AAAA-MM-JJ.json` contenant toutes les sorties et la fiche du bateau.
  Sur téléphone, le menu de partage s'ouvre : choisissez *Enregistrer dans Fichiers* (iCloud Drive), Google Drive, ou envoyez-le par e-mail.
- **Restaurer** : choisissez un fichier `.json` de sauvegarde, puis
  - **Fusionner** : ajoute les sorties absentes et garde la version la plus récente de chaque sortie ;
  - **Tout remplacer** : efface les données actuelles et les remplace par la sauvegarde.
- **Exporter en CSV** : pour Excel / Numbers / Google Sheets (lecture seule, ne sert pas à restaurer).

L'application vous rappelle quand la dernière sauvegarde date de plus de 30 jours.

**Changer de téléphone :** sauvegardez sur l'ancien, installez l'app sur le nouveau, puis *Restaurer → Tout remplacer*.

## Important

- Si vous supprimez l'application de l'écran d'accueil ou effacez les données du navigateur, **les sorties sont perdues** : faites des sauvegardes régulières.
- Sur iPhone, les données de l'app installée sur l'écran d'accueil sont séparées de celles de Safari. Utilisez toujours l'icône.
- Pour mettre à jour l'application, remplacez les fichiers sur Netlify / GitHub ; vos données sur le téléphone ne sont pas touchées.
