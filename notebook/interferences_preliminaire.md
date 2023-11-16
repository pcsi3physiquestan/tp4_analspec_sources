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

# Préliminaires

Ce TP dure 2h. Au bout de 2h, vous échangerez de poste avec un groupe travaillant sur la corde de Melde.


## Analyseur de spectre SpectrOvio

Le capteur utilisé ici est un analyseur de spectre qui se base sur la décomposition de la lumière. Le capteur est d'abord composé d'une fibre optique dont l'entrée capte un signal lumineux et la sortie est reliée à un système dispersif (2 miroirs concaves et un réseau. On pourra s'imaginer le principe du prisme qui fonctionne de la même manière). La lumière est alors déviée suivant des angles différents suivant sa longueur d'onde. Un barrette CCD capte alors le signal dans les différentes directions et on obtient ainsi le spectre de la lumière étudiée. 

````{admonition} Mise en place du dispositif
:class: tip
1. Installer le support pour l'entrée de la fibre sur un cavalier qu'on fixera sur le banc optique.
1. Sortir la fibre (à manipuler délicatement) et enlever les capuchons protecteur. Visser alors une extrémité sur le support et l'autre extrémité sur le dispositif dispersif (boitier gris).
1. Relier le dispositif à l'ordinateur au moyen d'un c\^able USB puis allumer le dispositif.
1. Lancer le logiciel SpectrOvio.
1. Réaliser la correction du signal reçu (Demander la méthode).
1. Décocher le choix d'un temps d'intégration Automatique et choisir un temps d'intégration de 3ms. Suivant les conditions d'éclairement il conviendra d'augmenter ce temps d'intégration si les mesures sont faibles.
````

Le logiciel propose plusieurs mesures:
* Première partie:
    * _Graphique:_ Une représentation du spectre dans le visible dans un système d'unité arbitraire.
    * _Noir:_ Permet de réaliser les mesures de noir (minimum de luminosité).
    * _Blanc:_ Permet de définir le spectre de ce qui est considéré comme «blanc», il ne s'agit pas du spectre de la lumière blanche (pas de sens) mais du spectre de référence. Une telle mesure est très utile pour les mesures d'absorbance et de transmittance. Cela permet de mesurer le pourcentage d'intensité lumineuse qui ``passe''.
* Deuxième partie:
    * _Transmittance et Absorbance:_ Permet de renvoyer le pourcentage d'intensité lumineuse qui respectivement est transmis ou est absorbé/réfléchi (donc le «reste» de ce qui est transmis). Pour que ces deux modes soient accessibles il faut que les deux référence ``noir'' et ``blanc'' soient réalisés.
* Troisième partie : Non utilisé ici
* Quatrième partie:
    * _Spectrographe:_ Comme son nom l'indique, il permet d'obtenir les spectres des signaux lumineux reçu. C'est le seul mode où la correction choisie est effectivement réalisée.

## Diffraction et interférences
On va utiliser un jeton semblable à celui [ci-dessous](jeton_dif) pour étudier la diffraction et les interférences.

```{figure} ./images/jeton_diffraction.jpg
:name: jeton_dif
:align: center
Jeton diffraction et interférences
```
L'observation se fera :
* soit un écran situé à grande distance D
* soit par une barrette CCD permettant d'observer le profil d'intensité. On la placera à une distance suffisamment grande en veillant à ce que la figure ne dépasse pas la barette.