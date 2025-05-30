==============================
Projet Snake - README (TP1 à TP5)
==============================

Auteur : ANEBAJAGAN ERIC
Contact : Eric.anebajagan@edu.esiee.fr

------------------------------
Présentation générale du projet
------------------------------
Ce projet consiste à programmer le jeu classique "Snake" en langage C, en partant de zéro, à travers 5 TPs progressifs. 
Chaque TP introduit de nouvelles notions de programmation en C, jusqu’à aboutir à un mini-projet complet, modulaire, et gérant la mémoire dynamiquement.

Le jeu se joue en console, avec une interface simple, et propose deux niveaux. Le joueur gagne lorsqu’il termine le niveau 1 après avoir mangé suffisamment de fruits.

------------------------------
Contenu des TPs
------------------------------

TP1 : Compilation séparée
- Mise en place des premiers fichiers .c et .h
- Structuration du projet
- Apprentissage de la compilation modulaire avec un makefile

TP2 : Fonctions de base
- Affichage d'une grille en console
- Manipulation de tableaux à deux dimensions
- Introduction des structures de données (struct Snake, etc.)

TP3 : Mouvement et interactions
- Déplacement du serpent à l’aide du clavier
- Gestion de la direction
- Détection des collisions avec les murs et le corps

TP4 : Lecture de fichiers
- Chargement des niveaux depuis des fichiers texte (ex: levels/default)
- Utilisation de la fonction getline() pour gérer les tailles variables
- Adaptation du jeu à des grilles de dimensions non fixes

TP5 : Allocation dynamique
- Suppression des constantes de taille
- Création d’une structure Grid contenant :
    -> char** grid
    -> int nbl, nbc
- Allocation mémoire avec malloc et free
- Séparation propre entre allocation de la structure et allocation des lignes
- Validation avec valgrind (aucune fuite mémoire)

------------------------------
Fonctionnement du jeu
------------------------------

Compilation :
-------------
Depuis la racine du projet (Jeu_SNAKE_2025_FINAL), entrez la commande :

> make clean  : Cela suprime l'ancien exe bin/game si présent

> make        : Cela creer executable game dans bin

> make run    : Cela lance l' executable ./bin/game 


Le jeu commence par le niveau "default".
Après 10 fruits mangés, vous accédez au "niveau 1".
Si vous réussissez également ce niveau, vous avez gagné !

Commandes :
-----------
- haut
- bas
- gauche
- droite

------------------------------
Fichiers et dossiers utiles
------------------------------
- src/        : fichiers source .c et .h
- levels/     : fichiers de niveaux jouables
- bin/        : fichiers compilés et exécutable
- makefile    : pour compiler le jeu
- doc/        : documentation utilisateur et développeur

------------------------------
Vérification mémoire
------------------------------
Le programme est compatible avec Valgrind. Pour tester :

> valgrind ./bin/game

Aucune fuite mémoire détectée.

------------------------------
Remarques finales
------------------------------
Le projet respecte l’ensemble des consignes pédagogiques :
- Bonne séparation du code
- Utilisation de la mémoire dynamique
- Code commenté, lisible et structuré
- Utilisation de getline() sans fuite

Merci d’avoir testé le jeu !
