---
module:         B-INN-000
title:          Workshop Mod Minecraft
subtitle:       Créer son premier mod Minecraft

language:		java
build:			gradle

noFormalities:	false
noCleanRepo:	false
noBonusDir:		true
noErrorMess:	true

author:			Alwyn
version:		1.0
---

# Workshop Mod Minecraft

## Pré-requis

Si vous n'avez pas déjà installé les outils nécessaires à ce workshop suivez les instructions situées ici : #br
[https://github.com/alwyn974/workshop-mc-mod/blob/master/REQUIREMENTS.md](https://github.com/alwyn974/workshop-mc-mod/blob/master/REQUIREMENTS.md)

## Configuration du workspace

On va commencer par modifier le `mcmod.info` pour y mettre les informations nécessaires.
Il faut modifier le `modid` pour mettre le vôtre (uniquement des lettres minuscules, sans espace).
Le reste à vous de modifier en fonction:

- modid : le modid de votre mod, remplacez donc examplemod par votre modid
- name : le nom du mod, à nouveau ce que vous avez mis dans la classe principale de votre mod
- description : une courte description du mod, vous pouvez ne rien mettre en laissant juste "".
- version : la version du mod, ne changez rien ici ${version} est automatiquement remplacé par la valeur se trouvant dans le build.gradle
- mcversion : la version de minecraft, comme pour la version, le remplacement est automatique
- url : le lien vers la présentation de votre mod
- updateUrl : l’url pour télécharger le mod
- authorList : la liste des auteurs. [“auteur1”, “auteur2”, “auteur3”] pour plusieurs auteurs, [“auteur”] pour un seul auteur
- credits : créditez ici les éventuels contributeurs.
- logoFile : le chemin à partir du début de l’archive vers le logo du mod. Si votre logo se trouve directement dans src/main/resouces et s’appelle logo.png il faudra mettre logo.png
- screenshots : une liste de screenshots, fonctionne comme pour le logo (chemin à partir du début de l’archive)
- dependencies : les dépendances, je conseille plutôt d’utiliser le String dépendance de l’annotation @Mod.

En suite, on va rename le package de base créer par le MDK, renommé donc `com.example.examplemod` par votre package.
Renommez aussi la classe `ExampleMod` par votre `Modid`Mod

#hint(Pensez aussi à faire les modifications dans le fichier ExampleMod.java)

## Création d'un Item Simple

On va devoir déclarer chaque item dans une classe spéciale, pour cela on va créer `ModidItems.java` qui contiendra:

- Une ArrayList<Item> en publique, statique et finale
- 

