# Bienvenue sur SpiDocs.

## Prérequis

* [BuildTools 1.17.1 ou plus](https://hub.spigotmc.org/jenkins/job/BuildTools/lastSuccessfulBuild/artifact/target/BuildTools.jar)
* [OpenJDK 16](https://adoptopenjdk.net/)
* [Eclipse](https://www.eclipse.org/downloads/packages/release/2021-03/r/eclipse-ide-java-developers) ou [Intellij](https://www.jetbrains.com/fr-fr/idea/download/)


C'est bon vous avez tout ?
Bon on peut commencer.

## Générer les sources de CraftBukkit et Spigot

Après avoir téléchargé BuildTools il faudra déplacer ce fichier dans un dossier spécifique car BuildTools va générer énormément de fichiers.

Maintenant vous devrez executer cette commande: 
`java -jar BuildTools.jar --rev 1.17.1`
Et voilà vous avez les sources de CraftBukkit

## Créer le plugin

Créez un projet gradle et importez Spigot

Dans le fichier build.gradle

```GROOVY
plugins {
    id 'java'
}

group 'fr.votrenom'
version '1.0-SNAPSHOT'

repositories {
    mavenCentral()
    mavenLocal()
}

dependencies {
    compileOnly('org.spigotmc:spigot:1.17.1-R0.1-SNAPSHOT')
    testImplementation 'org.junit.jupiter:junit-jupiter-api:5.7.0'
    testRuntimeOnly 'org.junit.jupiter:junit-jupiter-engine:5.7.0'
}

test {
    useJUnitPlatform()
}
```

Si jamais gradle vous donnes cette erreur <code style="color:red">General error during semantic analysis: Unsupported class file major version 60</code> allez dans le dossier `gradle` puis ouvrez `gradle-wrapper.yml`

Et changez la ligne contant <code style="color:orange">distributionURL=</code> par `distributionUrl=https\://services.gradle.org/distributions/gradle-7.2-bin.zip`
