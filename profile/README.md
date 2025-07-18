# Unix Filters

Ce projet a été réalisé pendant mon stage de troisième année de licence d'Informatique à l'Université de Lille, en collaboration avec l'association France-IOI. Il vise à faciliter l'apprentissage des filtres Unix (`grep`, `tr`, `cut`,...) via une interface de programmation par blocs basée sur Blockly.


## Dépôts

- [unixfilters-franceIOI](https://github.com/UnixFilters/unixfilters-franceIOI) :  
  Librairie principale en **JavaScript/Blockly** + communication avec le back Python.
- [checker](https://github.com/UnixFilters/checker) :  
  Exécution des commandes et évaluation des résultats en **Python**.

## Documentation complète

La documentation détaillée du projet (structure, blocs, ajouts, architecture, etc.) est disponible ici :
**[https://unixfilters.github.io/unixfilters-docs/](https://unixfilters.github.io/unixfilters-docs/)**

## Arborescence
### unixfilters-franceIOI

#### Dossier /public - Interface Blockly/JavaScript

```bash
.
├── blocklyUnixFilters_lib.js # Librairie contenant la définition des blocs
├── index.css # Style de la page html
├── index.html # Contenu de la tâche
├── jsongenerator.js # Génération du code pour chaque bloc
├── task.js # Contient les paramètres de la tâche (blocs disponibles, nombre de blocs autorisés,...)
└── unixfilters.js # Logique de l'affichage et de l'envoi de la commande au serveur
```

#### Dossier /python_lib - Serveur Python

```bash
.
└── server.py # Reçoit le code généré par les blocs et utilise le checker pour renvoyer le résultat au front
```

### checker
```bash
.
├── blocklyUnixFilters_lib.js
├── docs
│ ├── documentation_checker.md
│ └── documentation_checker.py
├── exemple_checker
│ └── tests
│  ├── copie de la librairie blockly
│  │ └── ...
│  ├── files
│  │ ├── test01.in # Fichier pris en entrée par le checker
│  │ ├── test01.out # JSON obtenu après exécution du code
│  │ └── test01.solout # Résultat attendu
│  └── gen
│    ├── checker.py # Logique permettant d'évaluer le score et renvoyer le feedback
│    ├── commands.py # Librairie exécutant les commandes
│    ├── livres.txt # Exemple de fichier d'entrée
│    └── solution.py # Contient le code généré par les blocs
├── index.css
├── index.html
├── jsongenerator.js
├── task.js
└── unixfilters.js
```
