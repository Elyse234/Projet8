# Portfolio – Jaona Elysé RAKOTOMAMPIANDRA

## Présentation

Ce portfolio présente mon parcours, mes compétences et mes différents projets. Il a été développé en HTML, CSS et JavaScript, avec une API Node.js/Express pour gérer le formulaire de contact.

## Fonctionnalités

- Présentation responsive et navigation entre les différentes sections.
- Affichage dynamique des compétences et des projets à partir des données définies dans `client/js/data.js`.
- Consultation des fiches détaillées des projets dans une fenêtre modale.
- Mode clair et mode sombre.
- Formulaire de contact connecté à une API Node.js/Express, permettant l'envoi de messages via Resend.
- Navigation accessible au clavier.

## Technologies utilisées

- HTML5
- CSS3
- JavaScript
- Node.js
- Express
- Resend
- Bootstrap

## Structure du projet

```text
.
├── client/
│   ├── index.html
│   ├── css/                  # Feuilles de style
│   ├── js/
│   │   ├── data.js           # Données des compétences et projets
│   │   └── main.js           # Affichage, navigation et formulaire
│   └── assets/
│       ├── icons/            # Icônes des technologies
│       ├── images/           # Images et captures des projets
│       └── cv/               # Curriculum Vitae
│
└── server/
    ├── server.js             # API Node.js/Express
    └── package.json
```

## Prérequis

Avant de lancer le projet, assurez-vous de disposer des éléments suivants :

- Node.js version 18 ou ultérieure.
- npm.
- Un navigateur web récent.
- Un compte Resend et une clé API pour l'envoi des messages du formulaire de contact.

## Installation et lancement en local

### 1. Lancer le frontend

Le frontend est un site web statique.

1. Ouvrir le dossier du projet dans Visual Studio Code.
2. Ouvrir le fichier `client/index.html` avec l'extension **Live Server**.
3. Configurer Live Server pour utiliser le port `5500` si nécessaire.

### 2. Installer et lancer l'API

Depuis un terminal, exécuter les commandes suivantes :

```bash
cd server
npm install
```

Créer ensuite un fichier `.env` dans le dossier `server/` :

```env
RESEND_API_KEY=re_xxxxxxxx
CONTACT_RECEIVER=adresse@example.com
PORT=3000
```

Remplacer les valeurs d'exemple par votre clé API Resend et l'adresse e-mail destinée à recevoir les messages.

**Important :** Ne jamais publier le fichier `.env` ni partager votre clé API. Assurez-vous qu'il est ajouté au fichier `.gitignore`.

### 3. Démarrer le serveur

Exécuter l'une des commandes suivantes :

```bash
npm start
```

Ou :

```bash
node server.js
```

L'API sera accessible à l'adresse suivante :

http://localhost:3000

Pour vérifier son fonctionnement, consulter :

http://localhost:3000/api/health

**Remarque :** Le serveur autorise les origines locales sur le port `5500`.

## Déploiement

Le projet est déployé en deux parties :

1. **Frontend :** hébergé sur GitHub Pages à partir de la branche `main`, grâce à un workflow GitHub Actions.
2. **Backend :** l'API Node.js/Express est déployée séparément sur Render.

Les variables d'environnement suivantes doivent être configurées dans les paramètres de l'hébergeur Render :

- `RESEND_API_KEY`
- `CONTACT_RECEIVER`

## Lien du projet en ligne

[Consulter le portfolio](https://elyse234.github.io/Projet8/)

## Personnalisation

Pour personnaliser le portfolio :

- Modifier `client/js/data.js` pour mettre à jour les compétences et les projets.
- Ajouter les captures des projets dans `client/assets/images/`.
- Ajouter le CV dans `client/assets/cv/`.
- Mettre à jour les liens des réseaux sociaux et les informations de présentation dans les fichiers du dossier `client/`.