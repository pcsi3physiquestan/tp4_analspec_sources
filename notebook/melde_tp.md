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
Le but de ce TP est de mettre en place un dispositif créant un phénomène d'onde stationnaire sur une corde tendue. On observera et discutera ainsi la discrétisation attendue des fréquences qui occasionnent une amplitude de vibration importante. Il sera observé aussi le phénomène à proprement parlé d'onde stationnaire en observation le caractère fixe des ventres et des noeuds.

## Observation d'une onde stationnaire

````{admonition} Mise en place
:class: tip
1. Mesurer la longueur totale de la corde et la peser. En déduire la masse linéique $\mu$ de la corde et son incertitude.
1. Mesurer une longueur de corde d'environ 85cm à partir d'une extrémité et attacher une masse de $m=150\rm{g}$. Fixer l'autre extrémité au vibreur. Fixer le vibreur sur son support et placer le support avec tige à une distance $l\approx 80\rm{cm}$ (mesurer précisément la longueur de corde tendue). Régler la hauteur du montage pour que la corde soit horizontale.
1. On peut alors rebrancher l'amplificateur au vibreur.
````

````{attention} 
Le mode de fonctionnement de la corde est étudié dans un cadre d'oscillations de petites amplitudes. C'est pourquoi, on limitera l'amplitude des oscillations en diminuant l'amplitude de la tension du GBF si nécessaire. L'idéal est de ne pas dépasser 1cm/1,5cm d'amplitude de vibration

Il y a un moyen de vérifier que l'amplitude est correcte : __si la corde tourne, il faut la diminuer l'amplitude.__

````

````{admonition} Etude d'une onde stationnaire
:class: tip
1. Exciter le vibreur avec une tension sinusoïdale de 40Hz, puis ajuster la fréquence de vibration jusqu'à observer un maximum d'amplitude de vibration de la corde (phénomène de résonance).
2. Proposer une méthode simple permettant de vérifier que la corde vibre bien à 40Hz grâce au stroboscope. Le vérifier. La méthode doit permettre d'observer que l'onde est stationnaire, repérer la position des ventres et des noeuds.
3. Réaliser l'expérience et déterminer la fréquence de vibration de la corde et les positions des noeuds et des ventres.
````

````{admonition} Célérité des ondes mécaniques
:class: tip
1. Proposer une méthode de mesure de la célérité des ondes progressives à la fréquence fixée en utilisant la relation de dispersion.
2. __Comparer__ à la valeur attendue: $c= \sqrt{\frac{mg}{\mu}}$ où g est l'intensité de la pesanteur $g=9,81  \pm 0.05 \rm{m.s^{-2}}$.  ($m$ est la masse suspendue)
````

## Modes propres des ondes stationnaires.
````{admonition} Détermination des modes propres de la corde vibrante
:class: tip
On estime, dans les conditions expérimentales proposées, la fréquence du fondamental supérieur à 15Hz.
1. Proposer un protocole expérimental permettant de déterminer les fréquences des modes propres en commençant par le fondamental $f_0$ ainsi que les longueurs d'onde pour chaque mode.
1. Réaliser l'expérience pour déterminer des fréquences (autant qu'on peut) ET les longueurs d'onde des signaux pour ces fréquences.
1. Quand la fréquence devient nettement supérieure à 20Hz, que ``ressent''-on? Commenter.

````

````{admonition} Longueur effective de la corde
:class: tip
Les études théoriques habituelles d'une corde vibrante prévoit la présence de 2 noeuds aux extrémités (ou 2 ventres, ou 1 ventre+1 noeud). Dans ces conditions (cf. cours), on attend une relation entre la longueur de la corde et les longueurs d'onde des signaux: $l=n \frac{\lambda}{2}$

1. Les mesures effectuées précédemment sont-elles cohérentes avec la présence de 2 noeuds aux extrémités?
1. Dans le cas général, on peut exprimer une longueur effective de corde $l_{eff}$ qui correspond à la longueur qu'aurait une corde vibrante présentant les mêmes modes propres en longueur d'onde mais avec deux noeuds à ses extrémités. Proposer une représentation graphique simple permettant de déterminer au moyen d'une régression linéaire la longueur effective de cette corde vibrante. Réaliser la représentation graphique et la régression linéaire à l'aide d'un tableur. Il n'est pas demandé un calcul d'incertitude pour cette question.

````