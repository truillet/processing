# Lab0 - Introduction à <img src="https://github.com/truillet/upssitech/blob/master/SRI/3A/Code/Processing_2021_logo.png" width=64> Processing.org
## Introduction
[Processing.org](https://processing.org) est un langage (en réalité, une surcouche du langage Java) développé par Ben Fry et Casey Reas (MIT) et dédié à la programmation créative.	

Il permet entre autres de manipuler des images (fixes ou animées) et interagir avec elles. Processing permet aussi de générer des textes, des formes vectorielles, des images en trois dimensions (en utilisant OpenGL), du son et plus généralement … tout ce que vous souhaitez !

Processing peut aussi être étendu à l’aide de librairies (fichiers JAR – **J**ava **AR**chive) ou grâce à des projets "dérivés" comme [Arduino](https://www.arduino.cc) (projet directement issu de Processing) , [Wiring](http://wiring.org.co) pour la gestion de capteurs physiques.

Il existe actuellement de multiples versions de Processing dont [p5.js](https://p5js.org), [processing JS] (http://processingjs.org) écrits en javascript (reprenant la syntaxe de Processing), [py5](https://py5coding.org) en python, Processing R, etc.

Processing dans *sa version originale* s’appuie sur le langage Java, ce qui lui permet de fonctionner sur les systèmes d’exploitation Windows, MacOS X, Linux (et donc aussi sur Raspbian pour Raspberry Pi) et Android avec le mode idoine proposé à partir de Processing 3).	

Malgré encore quelques petites lacunes (de plus en plus corrigées), [Processing.org](https://processing.org) a de nombreux atouts dont notamment sa simplicité d’usage qui en fait un langage presque idéal pour le prototypage rapide. 

## Installer Processing
**Nota1** : Nous supposerons dans la suite du document que l’IDE (**I**ntegrated **D**evelopment **E**nvironment) Processing 4.4.10 est installé dans le répertoire ```C:/langages```

Si ce n’était pas le cas, la première chose à faire est de se rendre à l’adresse https://www.processing.org/download/?processing et télécharger une des versions proposées (**version stable 4.5.1 du 19 janvier 2026 en 64 bits**).
Une fois téléchargée, décompressez l’archive dans le répertoire de votre choix et lancez l’exécutable *processing*.
Déterminer ensuite le répertoire où seront sauvés vos programmes (sketches)
(cf. *File | Preferences*), choisissez l’emplacement dans le champ *sketchbook location* et appuyez sur *ok*.

**Nota2** : Cette étape est primordiale pour la suite ; c’est dans ce répertoire que toutes librairies externes seront téléchargées et vos *sketchs* sauvés.

**Nota3** : Un tutoriel pour intégrer [Processing.org](https://processing.org) dans [IntellijIDEA](https://www.jetbrains.com/idea) est proposé ici :	 https://github.com/ctruillet/ProcessingOnIntellijIDEA

**Nota4** : Une extenstion Procssing pour [VSCode](https://code.visualstudio.com/) existe : [extension VSCode](https://marketplace.visualstudio.com/items?itemName=processing-foundation.processing-vscode-extension)

## Mon Premier sketch
Il est possible d’utiliser Processing.org de différentes manières dont notamment en *mode script* (suites d’actions exécutées qu’une seule fois), et en mode *continu* (avec une boucle infinie – fonction **draw**).

Par convention, les mots réservés du langage sont affichés en bleu, vert, orange et rose dans l’IDE. 

### Manipuler des formes - Mode script
*	Créer la composition graphique suivante en respectant l’ordre d’apparition des formes et leur taille.
<p align="center">
<img src="https://github.com/truillet/processing/blob/master/data/img/lab1_figure1.png" align="center" width=400>
</p>

*	Composer un tableau simplifié de type **[Piet Mondrian](https://www.wikiart.org/en/piet-mondrian)** (père du néo-plasticisme) ou **[Sophie Taeuber-Arp](https://www.wikiart.org/en/sophie-taeuber-arp)**

**Tips** : [Primitives graphiques](https://processing.org/reference/#shape) sous Processing.org

**Solution** : [Paintings](./exemples/base/Paintings.zip)

### Manipuler des formes - Mode continu
Le mode *continu* demande d’implémenter au moins deux fonctions : **setup()** qui initialise les variables (depuis [Processing.org](https://processing.org), on peut en plus utiliser la fonction **settings()**) et **draw()**, boucle d’affichage de données (*mainLoop*).
Cette boucle permet d’afficher des animations graphiques complexes, réagir à des événements asynchrones provenant d’actions de l’utilisateur ou d’événements systèmes.

Pour ce sketch, recopiez le code ci-après et lancez le script

```java
/** 
  Utiliser des primitives graphiques dans un script Processing
**/

/* Variables "globales" du sketch [En réalité, attributs de la classe PApplet] */
color GREEN = color(0,255,0);
color BLUE = color(0,0,255);
color SEMI_TRANSPARENT_RED = color(255,0,0,120);

void settings() {
  size(400,300); // créer une fenêtre de taille 400x300
}

void setup(){ // initialiser le sketch
 /* rien à faire ici */
}
  
void draw(){ // boucle infinie de dessin
  background(0); // redessiner la fenêtre en noir - 0-->noir / 255-->blanc  
  noStroke(); // ne pas dessiner le contour des objets dessinés
  
  /** dessin des trois formes **/
  // dessin du cercle
  fill(GREEN);
  circle(200,200,100);  
  // dessin du carré bleu
  fill(BLUE);
  square(50,50,100);
  //dessun du triangle
  fill(SEMI_TRANSPARENT_RED);
  triangle(40,20,250,150,80,250); 
}
  
```
(vous trouverez le fichier source --> [ici](https://github.com/truillet/upssitech/blob/master/SRI/3A/Code/primitives_graphiques.zip) <--).

Les possibilités du langage [Processing.org](https://processing.org) sont quasi-infinies notamment avec la possibilité d’utiliser la programmation orientée-objet, d’ajouter des librairies externes et d’en écrire soi-même ! 
Enfin, l’IDE Processing propose plusieurs modes : Java (par défaut) mais aussi Android (ADB doit être installé), [p5.js](https://p5js.org), Python, R et REPL (**R**ead **E**val **P**rint **L**oop soit sous forme de *shell*).

Il suffit de choisir le mode (une installation peut être requise) que vous souhaitez sur le bouton à droite de l’IDE.
Les premiers exercices ci-après vous donnerons un aperçu de ce qui peut être fait en quelques lignes de code.



--> **[Aller à la suite](lab1.md)** <--
