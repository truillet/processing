# Lab1 - Initiation à Processing.org
## Introduction
[Processing](https://processing.org) est un langage (en réalité, une surcouche du langage Java) développé par Ben Fry et Casey Reas (MIT) et dédié à la programmation créative.	

Il permet entre autres de manipuler des images (fixes ou animées) et interagir avec elles. Processing permet aussi de générer des textes, des formes vectorielles, des images en trois dimensions (en utilisant OpenGL), du son et plus généralement … tout ce que vous souhaitez !

Processing peut aussi être étendu à l’aide de librairies (fichiers JAR – **J**ava **AR**chive) ou grâce à des projets "dérivés" comme [Arduino](https://www.arduino.cc) (projet directement issu de Processing) , [Wiring](http://wiring.org.co) pour la gestion de capteurs physiques.

Il existe actuellement de multiples versions de Processing dont [p5.js](https://p5js.org), [processing JS] (http://processingjs.org) écrits en javascript (reprenant la syntaxe de Processing), [Processing Python](https://py.processing.org), Processing R, etc.

Processing dans sa version originale s’appuie sur le langage Java, ce qui lui permet de fonctionner sur les systèmes d’exploitation Windows, MacOS X, Linux (et donc aussi sur Raspbian pour Raspberry Pi) et Android avec le mode idoine proposé à partir de Processing 3).	

Malgré encore quelques petites lacunes (de plus en plus corrigées), Processing.org a de nombreux atouts dont notamment sa simplicité d’usage qui en fait un langage presque idéal pour le prototypage rapide 

## Installer Processing
**Nota1** : Nous supposerons dans la suite du document que l’IDE (Integrated Development Environment) Processing 4.1.2 est installé dans le répertoire C:/langages

Si ce n’était pas le cas, la première chose à faire est de se rendre à l’adresse https://www.processing.org/download/?processing et télécharger une des versions proposées (version stable 4.1.2 du 16 janvier 2023 en 64 bits).
Une fois téléchargée, décompressez l’archive dans le répertoire de votre choix et lancez l’exécutable *processing*.
Déterminer ensuite le répertoire où seront sauvés vos programmes (sketches)
(cf. *File | Preferences*), choisissez l’emplacement dans le champ *sketchbook location* et appuyez sur ok (cf. Figure 2).

**Nota2** : Cette étape est primordiale pour la suite ; c’est dans ce répertoire que toutes librairies externes seront téléchargées et vos *sketchs* sauvés.

**Nota3** : Un tutoriel pour intégrer Processing.org dans IntellijIDEA est proposé ici :	 https://github.com/ctruillet/ProcessingOnIntellijIDEA

## Mon Premier sketch
