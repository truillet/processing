# Lab0 - Introduction à <img src="https://github.com/truillet/upssitech/blob/master/SRI/1A/Code/Processing_2021_logo.png" width=64> Processing.org
## Introduction
[Processing.org](https://processing.org) est un langage (en réalité, une surcouche du langage Java) développé par Ben Fry et Casey Reas (MIT) et dédié à la programmation créative.	

Il permet entre autres de manipuler des images (fixes ou animées) et interagir avec elles. Processing permet aussi de générer des textes, des formes vectorielles, des images en trois dimensions (en utilisant OpenGL), du son et plus généralement … tout ce que vous souhaitez !

Processing peut aussi être étendu à l’aide de librairies (fichiers JAR – **J**ava **AR**chive) ou grâce à des projets "dérivés" comme [Arduino](https://www.arduino.cc) (projet directement issu de Processing) , [Wiring](http://wiring.org.co) pour la gestion de capteurs physiques.

Il existe actuellement de multiples versions de Processing dont [p5.js](https://p5js.org), [processing JS] (http://processingjs.org) écrits en javascript (reprenant la syntaxe de Processing), [Processing Python](https://py.processing.org), Processing R, etc.

Processing dans sa version originale s’appuie sur le langage Java, ce qui lui permet de fonctionner sur les systèmes d’exploitation Windows, MacOS X, Linux (et donc aussi sur Raspbian pour Raspberry Pi) et Android avec le mode idoine proposé à partir de Processing 3).	

Malgré encore quelques petites lacunes (de plus en plus corrigées), Processing.org a de nombreux atouts dont notamment sa simplicité d’usage qui en fait un langage presque idéal pour le prototypage rapide 

## Installer Processing
**Nota1** : Nous supposerons dans la suite du document que l’IDE (**I**ntegrated **D**evelopment **E**nvironment) Processing 4.1.2 est installé dans le répertoire ```C:/langages```

Si ce n’était pas le cas, la première chose à faire est de se rendre à l’adresse ```https://www.processing.org/download/?processing``` et télécharger une des versions proposées (version stable 4.3 du 26 juillet 2023 en 64 bits).
Une fois téléchargée, décompressez l’archive dans le répertoire de votre choix et lancez l’exécutable *processing*.
Déterminer ensuite le répertoire où seront sauvés vos programmes (sketches)
(cf. *File | Preferences*), choisissez l’emplacement dans le champ *sketchbook location* et appuyez sur *ok*.

**Nota2** : Cette étape est primordiale pour la suite ; c’est dans ce répertoire que toutes librairies externes seront téléchargées et vos *sketchs* sauvés.

**Nota3** : Un tutoriel pour intégrer [Processing.org](https://processing.org) dans [IntellijIDEA](https://www.jetbrains.com/idea) est proposé ici :	 ```https://github.com/ctruillet/ProcessingOnIntellijIDEA```

## Mon Premier sketch
Il est possible d’utiliser Processing.org de différentes manières dont notamment en mode « script » (suites d’actions exécutées qu’une seule fois), et en mode *continu* (avec une boucle infinie – fonction **draw**).

Le mode *continu* demande d’implémenter au moins deux fonctions : **setup()** qui initialise les variables (depuis [Processing.org](https://processing.org), on peut en plus utiliser la fonction **settings()**) et **draw()**, boucle d’affichage de données (*mainLoop*).
Cette boucle permet d’afficher des animations graphiques complexes, réagir à des événements asynchrones provenant d’actions de l’utilisateur ou d’événements systèmes.

Par convention, les mots réservés du langage sont affichés en bleu, vert et orange dans l’IDE. 

Pour ce premier sketch, recopiez le code ci-après (vous trouverez le fichier source ici -->	 ```https://github.com/truillet/upssitech/blob/master/SRI/1A/Code/primitives_graphiques.zip```) et	 lancez le script.

Les possibilités du langage [Processing.org](https://processing.org) sont quasi-infinies notamment avec la possibilité d’utiliser la programmation orientée-objet, d’ajouter des librairies externes et d’en écrire soi-même ! 
Enfin, l’IDE Processing propose plusieurs modes : Java (par défaut) mais aussi Android (ADB doit être installé), [p5.js](https://p5js.org), Python, R et REPL (**R**ead **E**val **P**rint **L**oop soit sous forme de *shell*).

Il suffit de choisir le mode (une installation peut être requise) que vous souhaitez sur le bouton à droite de l’IDE.
Les premiers exercices ci-après vous donnerons un aperçu de ce qui peut être fait en quelques lignes de code.

