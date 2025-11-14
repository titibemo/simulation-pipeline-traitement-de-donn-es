# TP de la muerte - simulation d'une pipeline de traitement de données

## Installation

*prérequis : Docker et git doit être installé*

Pour intaller le projet, créer un nouveau dossier avec le nom de votre choix et faites :

```bash
git clone https://github.com/titibemo/simulation-pipeline-traitement-de-donn-es
```
Une fois le repo cloné, sur VSCode ou un terminal de votre choix, ouvrez un terminal, faites :
```bash
cd exercice4
```
puis
```bash
docker compose up --build
```

## fonctionnement de la pipeline

Vous allez apercevoir dans le terminal dans un premier temps la créations des bucket "bronze", "silver" et "gold" ci ceux-ci n'ont pas été créés précedemment puis les différents conteneurs se lancer dans un laps de temps précis :

1. [generator]: Générant tous les 5 secondes des fichiers, avec un message d'upload dans votre console indiquant que l'upload a bien été effectué dans le bucket bronze 
2. [cleaner]: Va récupérer les fichiers dans le bucket bronze pour les nettoyer et les envoyer dans le bucket silver tous les 10 secondes.
3. [generator]: va récupérer les fichiers dans le bucket bronze pour les nettoyer et les envoyer dans le bucket gold tous les  20 secondes.

Vous pouvez ainsi voir le fonctionnement de la pipeline.

Vous pouvez aussi vous amusez à nettoyer les differents fichiers entre les transtision bronze-> silver et silver->gold. Cette pipeline n'effectuant que la récupération et l'envoi des fichiers.
