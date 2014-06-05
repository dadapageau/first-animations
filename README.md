first-animations
================
Règles générales d’utilisation

La librairie CSS animation_lib_DaniellePageau.css contient des classes CSS permettant de faire cinq animations qui seront supportées par les différents navigateurs (Chrome, Opera, Safari, Firefox et Explorer10 et +). Son utilisation est simple, il suffit :
* de mettre le lien vers cette librairie dans l’entête (<head>) de votre fichier HTML;
<head>
  <link rel="stylesheet" ref="animation_lib_DaniellePageau.css">
</head>
  * d’utiliser la classe .animation avec le nom de la classe de l’animation que vous voulez utiliser.
<div class= "animation grossir"> </div>
* d’ajouter la classe .infinie pour une animation en continu.
<div class= "animation infinie grossir"> </div>
LES CLASSES .animation et .infinie
Nous avons créé deux classes que vous devez ou pouvez ajouter lors de vos animations selon l’effet que vous voulez obtenir.
La classe .animation contient la majorité des propriétés nécessaires au bon fonctionnement des animations. Les valeurs par défaut comprises dans ces propriétés sont les suivantes :
* La durée des animations : 1 seconde (animation-duration : 1s);
* Nombre d’itérations : 1 seule (animation-iteration-count : 1);
* Le délai avant l’animation : aucun délai (animation-delay : 0s);
* L’état à la fin de l’animation : revient à l’état de départ (animation-fill-mode : backwards);
* La courbe d’accélération : linéaire (animation-timing-function : linear).
La classe .infinie permet quant à elle à ce que l’animation se répète à l’infini (animation-iteration-count : infinite) et à ce que cette animation à l’infini se fasse selon une direction alternée (animation-direction : alternate).
Les cinq animations
1. Grossir : scale, rotate, opacity
Appliquée à un élément « block » ou « inline », l’animation fait grossir graduellement l’élément jusqu’à deux fois sa taille initiale tout en diminuant son opacité. Lorsque l’élément atteint sa taille maximale, soit à 90% de l’animation, il y a un petit effet de « frisson » ou de « swing » selon la forme de l’élément.
Cette animation doit être utilisée avec la classe .animation. On peut lui ajouter la classe .infinie si on désire une durée infinie de l’animation.
Exemple : <div class= "animation infinie grossir"> </div>
		<p class= "animation grossir" Bonjour </p>
2. Presenter : translate, opacity, scale
Presenter est une animation plus intéressante pour un élément « inline » texte que pour un élément de type « block ». L’animation est prévue pour une exécution en 2 secondes afin de permettre l’entrée de l’élément et sa présentation. Appliquée sur un titre, elle permet une présentation, un peu comme une entrée sur une scène suivie d’une salutation. Le titre entre en effet par la droite de l’écran, grossit en arrivant au centre de l’écran, puis produit un effet de recul en s’affichant à 100%. Cette animation  est plus ou moins appropriée pour une animation à l’infini. Il est donc préférable de ne pas ajouter la classe .infinie.
 Exemple : <h1 class= "animation presenter"> </h1>
3. QuatreCoins : translate, opacity, scale
L’animation .quatreCoins, comme son nom l’indique, permet de promener un élément de type « inline » ou « block » sur les quatre coins d’un losange invisible. Lors de cette promenade de l’élément, on obtient également comme un effet de rebond et de clignotement. L’animation a une durée d’exécution de 2 secondes et, lorsque l’animation est utilisée avec une répétition à l’infini, la direction de l’animation a été mise en mode normal pour que l’élément fasse sa promenade en continu.
Exemple : <h1 class= "animation infinie quatreCoins"> </h1>
		<div class= "animation quatreCoins"> </div>
4. Urgence : scale, opacity, rotate
Urgence est une animation rapide qui apporte un sentiment d’urgence ou d’importance de par son exécution en 0,5 seconde et sa durée qui a été définie pour s’exécuter à l’infini. Il n’est donc pas nécessaire d’ajouter la classe .infinie. Appliquée à un élément de type « block », cette animation donne un peu l’effet d’une cloche qui sonne. L’élément grossit et reprend sa taille normale très rapidement en changeant de forme et en bougeant légèrement. Il peut être intéressant de mettre la couleur de fond en rouge (background-color : red) pour augmenter le sentiment d’urgence. Sur un élément de type « inline », l’effet est semblable et peut également être renforcé en utilisant la couleur rouge (color : red).
Exemple : <div style="background-color: red" class= "animation urgence"></div>
<p style="color: red" class= "animation urgence"> Bonjour </p>
5. A) Lettres : letter-spacing, translate, scale
L’animation .lettres est plus intéressante pour les éléments « texte » que les éléments « block ». L’animation .lettres s’exécute en 2 secondes et fait en sorte que les mots arrivent par le haut de l’écran avec un grand espacement entre les lettres. En arrivant au centre de l’écran, le ou les mots grossissent puis donnent un effet de recul en reprenant leur taille à 100%. En « reculant », les lettres s’écartent entre elles à nouveau. Cette animation n’est pas vraiment prévue pour être exécutée à l’infini.
Utilisée avec un élément de type « block », l’animation perdra son effet d’espacement des lettres. Ainsi, l’élément arrivera par le haut, grossira, puis reprendra sa taille à 100%.
Exemple : <h1 class= "animation lettres"> Bienvenue sur notre site </h1>
5. B) RectoVerso : translate, rotate, scale
L’ animation .rectoVerso est une animation plus appropriée pour les éléments « block » à cause de l’effet du changement de la couleur de fond. Sur un élément de type « block », l’animation aura pour effet de grossir l’élément puis de le tourner pour qu’il montre son verso. L’animation s’exécute en 2 secondes et fait apparaître le verso en noir.  
	Exemple : <div class= "animation infinie rectoVerso"> </div>
Changer la valeur d’une propriété
* Pour changer la valeur d’une ou plusieurs des propriétés de l’animation, il vous faudra attribuer un identifiant à votre élément HTML (id= «monIdentifiant ») et ajouter les propriétés d’animation que vous voulez modifier ainsi que leurs nouvelles valeurs dans votre feuille de style CSS, comme ceci par exemple :
#monIdentifiant {
  -prefixeDeNavigateur-animation-duration: 3s;
  -prefixeDeNavigateur-animation-delay: 2s;
  -prefixeDeNavigateur-animation-iteration-count: 5;
Etc.
}
Pour que l’animation fonctionne bien dans tous les navigateurs, il faudra ajouter le préfixe de chacun d’entre eux à la propriété que vous voulez changer. Voici la liste des préfixes et de leurs navigateurs correspondants : 
-webkit-: (opéra, chrome, safari);
-moz- : firefox;
-o- : opera;
-ms- : internet Explorer.
Dans l’exemple précédant, on aurait alors :
#monIdentifiant {
  -webkit-animation-duration: 3s;
  -moz-animation-duration: 3s;
  -o-animation-duration: 3s;
  -ms-animation-duration: 3s;
   animation-duration: 3s;

 -webkit-animation-delay: 2s;
 -moz-animation-delay: 2s;
 -o-animation-delay: 2s;
 -ms-animation-delay: 2s;
  animation-delay: 2s;

 -webkit-animation-iteration-count: 5;
 -moz-animation-iteration-count: 5;
 -o-animation-iteration-count: 5;
 -ms-animation-iteration-count: 5;
  animation-iteration-count: 5;
Etc.
}

