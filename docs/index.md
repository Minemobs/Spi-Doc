# Bienvenue sur MCP Docs.

## Prérequis

* [BuildTools 1.17 ou plus](https://hub.spigotmc.org/jenkins/job/BuildTools/lastSuccessfulBuild/artifact/target/BuildTools.jar)
* [OpenJDK 16](https://adoptopenjdk.net/)
* [Eclipse](https://www.eclipse.org/downloads/packages/release/2021-03/r/eclipse-ide-java-developers) ou [Intellij](https://www.jetbrains.com/fr-fr/idea/download/)


C'est bon vous avez tout ?
Bon on peut commencer.

## Générer les sources de CraftBukkit et Spigot

Après avoir téléchargé BuildTools il faudra déplacer ce fichier dans un dossier spécifique car BuildTools va générer énormément de fichiers.

Maintenant vous devrez executer cette commande: 
`java -jar BuildTools.jar --rev latest`
Et voilà vous avez les sources de CraftBukkit

Après ça, créez un projet gradle et importez Spigot

```GROOVY

```