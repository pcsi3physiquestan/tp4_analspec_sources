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
# Etude préliminaire


## Goniomètre à réseau
La théorie sous-jacente est vue dans le cours sur les ondes. On retiendra que :
* le réseau est constité d'un grande nombre de fentes (comme les fentes d'Young). Il est caractérisé par N, le nombre de fente par unité de longueur. Comme un grand nombre de rayons sortent de ces fentes, ils vont interférer.
* Il existe dans conditions sur l'angle en sortie pour observer des interférences constructives :

$$\sin \theta = \sin i + p N \lambda$$

où $i$ est l'angle du faisceau incident sur le réseau, $\theta$ l'angle du faisceau sortant donnant lieu à des interférences constructives, $\lambda$ la longueur du faisceau et $p$ un nombre entier relatif appelé __ordre d'interférence.__

Pour chaque ordre $p=-2, p=-1, p=0, p=1, p=2...$ on observera des interférences constructives : une raie lumineuse de la couleur correspondant à $\lambda$. Comme $\theta$ dépend de $\lambda$ on peut distinguer plusieurs composantes spectrales d'un même signal lumineux.

_La démonstration de la relation des réseaux est identique à la recherche d'interférence constructives entree 2 fentes (s'il y a interférences constructives entre deux fentes successives, il y aura interférences constructives entre toutes les fentes). La distance entre les deux fentes étant alors $a = \frac{1}{N}$, on retrouve la relation proposée._ __S'entrainer à la retrouver.__

## Goniomètre à prisme
L'étude préliminaire a déjà été réalisée dans le cours d'optique. On reprendra l'exercice en s'attardant notamment sur les points suivants :
* trajets qualitatif des rayons
* cas d'existence d'une réflexion totale
* existence d'un minimum de déviation et relation entre ce minimum et la longueur d'onde.

__Il est aussi vivement conseillé de reprendre les instruments d'optique pour se rappeler le principe de fonctionnement et de réglage d'une lunette et d'un collimateur.__