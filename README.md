J'ai conteneurisé ma première application en partant de zéro. Voilà ce que ça m'a appris. 🧵
Cette semaine, j'ai dockerisé une app complète :
→ Un backend Flask (Python) qui expose une API REST
→ Un frontend PHP/Apache qui l'appelle
→ Le tout orchestré avec Docker Compose
Ce que j'ai compris grâce à ce projet :

1/ Les images vs les containers
Une image, c'est la recette. Un container, c'est le plat cuisiné.
Tu peux lancer 10 containers identiques depuis la même image.

2/ Le Dockerfile, c'est une liste d'instructions
Chaque ligne = une couche dans l'image.
J'ai appris que python:3.13-slim ne contient pas gcc.
Erreur → correction → compréhension. C'est comme ça qu'on apprend.

3/ Docker Compose, c'est le chef d'orchestre
Un seul fichier YAML pour dire :
"Lance ces 2 containers, connecte-les en réseau, partage ces fichiers."

4/ Les volumes changent tout
Modifier un fichier sur mon PC → le container le voit immédiatement.
Pas besoin de reconstruire l'image à chaque changement.

La vraie leçon :
Docker résout le "ça marche sur ma machine".
C'est la base de tout pipeline CI/CD moderne.
Prochain projet : Kubernetes ☸️
Parce qu'orchestrer 2 containers c'est bien.
En orchestrer 100 en production, c'est autre chose.

Tu débutes en DevOps ? Qu'est-ce qui t'a le plus bloqué au début ?