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

(stroboscope)=
# Préliminaires

Ce TP dure 2h. Au bout de 2h, vous échangerez de poste avec un groupe travaillant sur les interférences.

## Effet stroboscope
Le principe des ondes stationnaires a été expliqué en cours. On présente ici l'utilisation du stroboscope pour observer la forme de la corde.

Un stroboscope est un instrument utilisé pour étudier des mouvements périodiques de période $T$ trop rapides pour être observés à l'oeil nu. Le stroboscope est constitué d'une lampe émettant des flashs (à l'aide d'un dispositif mécanique ou électronique) à une fréquence $f_0$ déterminée, variable. Le mouvement à étudier est alors illuminé pendant un temps très court, à intervalles de temps réguliers $T_0=1/f_0$. La trajectoire est en fait "échantillonnée" par le stroboscope. 

```{figure} ./images/Signaux_Stroboscope_2.jpg
:name: stroboscopef
:align: center
Différents cas.
```
Selon le rapport entre les valeurs de $T$ et $T_0$, plusieurs cas peuvent se présenter. Pour fixer les idées, nous prenons l'exemple du disque donc un rayon est marqué, tournant avec une période $T$ et observé à l'aide d'un stroboscope à la période $T_0$.

* Si les deux fréquences sont dans un rapport irrationnel, alors on observe une position du rayon marqué mobile.
* Immobilité apparente: Si maintenant, la période du stroboscope $T_0$ est un multiple entier de la période T du phénomène observé ($T_0=nT$), on n'observe alors qu'une et une seule configuration fixe. Le phénomène apparaît fixe. Si le rapport entre $T_0$ et $T$ est fractionnaire ($T_0= \frac{p}{q}T$ avec p et q entiers naturels dont le ppcm est 1), on observe q configurations fixes. Le phénomène apparaît q fois fixe.
* Mouvements apparents: Si la période $T_0$ du stroboscope est proche d'une des deux situations précédentes, on observe un mouvement apparent d'une ou des q configurations. Le phénomène apparaît en mouvement ralenti, direct ou rétrograde (c'est ce qui observé avec la cuve à ondes ou pour les roues des voitures dans les films).


## Utilisation du stroboscope.
Cette manipulation n'est pas à faire. On décrit simplement la méthode.

On s'efforce d'obtenir une unique configuration fixe ou en ralenti apparent. Cela permet d'observer le phénomène et d'en connaître la fréquence.

1. Dans la pratique, on se place initialement dans le cas où la fréquence $f_0$ du stroboscope est supérieure à la fréquence f du dispositif à étudier. On se place donc à la fréquence maximale délivrée par l'appareil. On diminue ensuite progressivement cette fréquence.
2. On observe alors plusieurs fois q configurations fixes et pour une valeur particulière de $f_0$ on observe une première fois une unique configuration fixe. Alors $f_0= f$. La fréquence du stroboscope est donc égale à la fréquence recherchée f au phénomène observé. Pour confirmer cette valeur, on peut continuer à diminuer la fréquence $f_0$. On doit retrouver une configuration fixe chaque fois que $f_0= f /n$ avec n entier.

````{admonition} Question
:class: tip
Pourquoi faut-il partir de la fréquence maximale en diminuant et non de la fréquence minimale en augmentant?
````

````{attention} 
Le stroboscope peut afficher une fréquence en bpm (battements par minute) au lieu d'une fréquence en Hz.
````
