# Pré-requis

- Créer un repository sur github pour le workshop (rendu obligatoire)
- Connaître les bases de la programmation en Java (cf: [workshop-java](https://github.com/alwyn974/workshop-java))

## Logiciels

Il vous faudra :
- Le JDK 8
- Intellij Idea (Community/Ultimate)
- Optionel : [Plugin Minecraft Development](https://plugins.jetbrains.com/plugin/8327-minecraft-development)

## MDK Forge

Avoir téléchargé le [MDK Forge 1.12.2](https://files.minecraftforge.net/net/minecraftforge/forge/index_1.12.2.html)
Prendre la version latest en **MDK** (normalement la 1.12.2-14.23.5.2860)

## Installation du MDK Forge

Extraire l'archive dans un dossier (contenant uniquement des lettres ou chiffres) et ouvrir ce dossier avec Intellij Idea, Intellij s'occupera de préparer le workspace
et de télécharger toutes les bibliothèques nécessaires

## Setup après l'installation

On va modifier le `build.gradle` pour y ajouter cela avant `version = '1.0'`

```groovy
apply plugin: 'idea'

idea { module { inheritOutputDirs = true } }

sourceSets {
    main {
        output.resourcesDir = output.classesDir
    }
}
```

On va aussi modifier ces 3 lignes :
```groovy
version = "1.0"
group= "com.yourname.modid" // http://maven.apache.org/guides/mini/guide-naming-conventions.html
archivesBaseName = "modid"
```

- La première ligne est la version de votre mod. Vous pouvez laisser 1.0 ou mettre autre chose.
- Le groupe sera le package de base de votre mod. (Pour moi, ça sera re.alwyn974.workshop)
- Et pour finir archivesBaseName est le nom du jar de votre mod. Il y sera ajouté -<version du mod>.jar lors de la compilation. Dans mon cas, ce sera WorkshopMod

## Création des configurations de lancement pour Intellij

Pour que vous puissiez lancer votre mod directement dans Intellij, il vous faudra exécuter ceci : <br>
*C'est cette commande qui va télécharger Minecraft*
```bash
# Si vous avez déjà gradle
gradle genIntellijRuns
# Sinon faire
./gradlew genIntellijRuns
```
