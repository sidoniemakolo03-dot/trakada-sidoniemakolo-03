# trackada

Script Node.js qui vérifie l'avancement des projets du bloc 1 d'Ada Tech.

## Description

`checktrack.js` lit le fichier `track.json`, puis contrôle pour chaque projet :

- que le dossier existe dans `~/ada-tech/bloc1/projets/`
- que le repository git est initialisé (dossier `.git`)
- que tous les fichiers requis sont présents

Il affiche ✅ ou ❌ pour chaque projet, avec la liste des erreurs, puis le pourcentage de projets corrects.

## Prérequis

- [Node.js](https://nodejs.org/) (version 18 ou plus récente)
- Les projets du track placés dans `~/ada-tech/bloc1/projets/`

## Installation

```
git clone <url-du-depot>
cd trackada
```

## Utilisation

Lance le script depuis le dossier qui contient `track.json` :

```
node checktrack.js
```

### Exemple de résultat

```
✅ dossier ~/ada-tech/bloc1/projets
✅ adapage
❌ adaquiz
   - fichier manquant : README.md

1/2 projets corrects (50%)
```

## Structure du projet

```
trackada/
├── checktrack.js   # le script de vérification
├── track.json      # liste des projets et fichiers requis
├── package.json
└── README.md
```

## Format de track.json

```json
{
  "projects": [
    { "name": "adapage", "required": ["index.html", "style.css", "README.md"] }
  ]
}
```

- `name` : nom du dossier du projet
- `required` : fichiers qui doivent être présents

## Auteur

Ton prénom / ton pseudo GitHub
