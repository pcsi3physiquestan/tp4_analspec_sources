---
jupytext:
  encoding: '# -*- coding: utf-8 -*-'
  formats: ipynb,md:myst
  split_at_heading: true
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Travaux pratiques

## Analyse du spectre de différentes sources lumineuses
````{attention} 
Les Lasers peuvent être extrêmement dangereux pour la vue. Il ne faut JAMAIS placé son oeil dans la direction de propagation du Laser et faire attention aux réflexions. Les lampes spectrales et les lampes à incandescence peuvent être très chaudes. Il faut les manipuler avec précautions et ne surtout pas toucher l'ampoule. D'une manière générale, le matériel d'optique est un matériel fragile qu'il faut manipuler avec soin.
````

````{admonition} Obtenir différents spectre lumineux
:class: tip
1. Eclairer le capteur au moyen de diverses sources lumineuses proposées et observer et décrire les spectres obtenus grâce à l'option "Spectrographe".
    * Commencer par la lampe à incandescence pour vérifier que la correction du capteur est bien réalisée. Si l'intensité chute pour les couleurs rouge-orange, c'est que la correction du capteur n'a pas été réalisée correctement.
    * Allumer la lampe spectrale (noter laquelle) quelques temps avant d'analyser son spectre car elle met un certain temps avant d'atteindre un régime permanent.
    * Vérifier que le LASER arrive bien sur la fibre (attention, il peut y avoir saturation du capteur).

````
## Etude de la diffraction

Il s'agit d'une étude purement qualitative. On utilisera un LASER. __Ne pas regarder le laser directement et attention aux réflexion.__

````{admonition} Etude de la diffraction
:class: tip
1. Eclairer les fentes simples de taille différentes avec le LASER et observer l'évolution de la tâche centrale sur un écran situé à bonne distance. Commenter le profil d'intensité observé à chaque fois.
2. Eclairer maintenant les trous simples et commenter à nouveau les observations.
3. Remplacer l'écran par la barette CCD et observer le profil d'intensité lorsqu'on éclaire une fente. Mesurer rapidement la taille de la tâche de diffraction. 

Concernant la barette CCD:
* La berette n'est située qu'au centre du cercle. Pensez à centrer le faisceau.
* Il est possible qu'il faille faire tourner les polariseurs fixés sur le capteur pour éviter la saturation. Si ça n'est pas suffisant, ajouter deux polariseurs entre le laser et les fentes puis en faire tourner un pour diminuer l'amplitude.
````

## Etude des interférences.
### Etude à distance finie
On utilise à nouveau le LASER.

````{admonition} Etude des interférences
:class: tip
1. Eclairer les fentes doubles avec le LASER et mesurer l'interfrange sur un écran situé à une distance D. Vérifier que l'interfrange a à peu près la valeur attendue (on ne demande pas de calcul d'incertitude) dans le cadre d'étude théorique. __Attention à ne pas confondre les variations d'amplitude liées à la diffraction à celles liées aux interférences.__
2. Faire la même manipulation avec les autres fentes doubles.
3. Remplacer l'écran par la barette CCD et reprendre la mesure précédente.
````

### Etude à l'infini

Pour étudier la figure d'interférence à l'infini, on va la projeter sur un écran situé dans le plan focal image d'une lentille.

````{admonition} Distance focale de la lentille
:class: tip
1. Commencer par éteindre le LASER et enlever le ainsi que le jeton d'interférences.
2. En utilisant la lampe à LED. Réaliser un dispositif {lentille+écran} où l'écran est dans le plan focal image de la lentille. On prendra la lentille de plus grande focale à disposition (utiliser la valisette bleue).
3. Enlever la lampe et replacer le LASER avec le jeton d'interférences.
4. Observer la figure d'interférences et mesurer l'interférence. La comparer à la valeur attendue (sans incertitude à nouveau).
````

### Complément : Perte de cohérence
> Remplacer le LASER par une lampe au sodium et revenir à des interférences à une distance D. Observe-t-on encore correctement les interférences ? On utilisera un diaphragme à iris pour limiter l'éclairage à une seule double fente.
> Remplacer la lampe par une lampe à LED. Observe-t-on encore correctement les interférences ?
