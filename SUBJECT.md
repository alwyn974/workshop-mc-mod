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
Le reste à vous de modifier

En suite, on va rename le package de base créer par le MDK, renommé donc `com.example.examplemod` par votre package.
Renommez aussi la classe `ExampleMod` par votre `Modid`Mod

#hint(Pensez aussi à faire les modifications dans le fichier ExampleMod.java)

## Création d'un Item Simple