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
# (TP) Réalisation pratique

Un goniomètre est un appareil qui sert à effectuer des mesures d'angles (de gônia ``angle'' et metron ``mesure, évaluation''). Il possède une plateforme pouvant tourner autour d'un axe et sur laquelle on placera un dispositif permettant de disperser la lumière: en 1ère année, un prisme. Un collimateur permet d'éclairer le prisme par un faisceau de lumière parallèle, le faisceau émergent pouvant être visé par une lunette autocollimatrice réglée à l'infini. L'oculaire de la lunette est muni d'un réticule pour réaliser le pointage du faisceau émergent. Un système de graduation sous la lunette permet une lecture de la position angulaire de la lunette.

```{figure} ./images/AnalyseSpec_Goniometre_Schema.jpg
:name: goniometre
:align: center
Goniomètre
```
## Réglage du goniomètre (30 min)
Un goniomètre nécessite deux types de réglages :
* des réglages optiques : réglage de la lunette (par auto-collimation) et du collimateur (grâce à la lunette).
* des réglages géométriques : orientation de la plateforme et de la lunette pour que les rayons ne dévient pas trop d'un plan "horizontal" (= perpendiculaire à l'axe de rotation de la plateforme).

```{warning}
Ne pas passer trop de temps sur ces réglages, le but est surtout de manipuler.
```

### Réglage de la lunette autocollimatrice

Une lunette autocollimatrice a pour rôle de permettre d'observer un objet à l'infini, grossi (rappel: l'étendue transversale d'un objet ou d'une image à l'infini est caractérisée par un angle). Comme l'observation se fait à l'oeil, la dernière image formée par la lunette doit être à l'infini elle aussi. Il s'agit donc d'un système afocal. Elle est constituée d'un objectif, d'un réticule et d'un oculaire (voir schéma ci-dessous). La distance réticule-oculaire est réglable, ainsi que la distance objectif-{réticule+oculaire} (bagues de réglage). Une lampe intégrée (source 6V) et une lame semi-réfléchissante qui peut être basculée à $45^{\circ}$ permettent, si besoin, d'éclairer de côté.

```{figure} ./images/AnalyseSpec_Lunette_Reglages.jpg
:name: lunette_auto
:align: center
Lunette auto-collimatrice.
```

````{admonition} Manipulation préliminaire
:class: tip
1. Réglage de la distance oculaire-réticule : Observer à travers l'oculaire et régler le tirage de l'oculaire jusqu'à observer une image nette R' du réticule R, sans accommodation.
2. Réglage de la distance objectif-{réticule-oculaire}: mise au point à l'infini : Le principe consiste à placer le foyer image de l'objectif au niveau du réticule. On utilise pour cela la méthode d'autocollimation, d'où le nom de lunette autocollimatrice.
    1. Positionner la lame semi-réfléchissante pour que l'éclairage provienne de l'intérieur de la lunette.
    2. Placer un miroir plan (MP) juste derrière l'objectif, perpendiculairement à l'axe optique. La lumière de la lampe est réfléchie sur la lame semi-réfléchissante, vers le MP, où elle se réfléchit et traverse la lame jusqu'à l'oculaire. On observe alors dans la lunette un disque lumineux dû à la lumière réfléchie par le MP (faire varier légèrement l'orientation du miroir ou de la lunette si besoin).
    3. Régler le tirage de l'objectif jusqu'à ce que le réticule et son image par le MP soient nettes (elles sont alors confondues). _Attention à l'erreur de parallaxe._
````

### Réglage du collimateur
Le rôle d'un collimateur est de former un objet à l'infini. Il est constitué d'un objectif et d'un objet (qui dans ce TP une fente F de largeur et d'orientation réglables), éclairé par une source placée en amont. Régler le collimateur consiste à ajuster la distance objet-objectif pour amener l'objet (fente ici) dans le plan focal objet de l'objectif. On obtiendra alors une image nette de la fente à l'infini.

````{admonition} Manipulation préliminaire
:class: tip
1. éclairer la fente du collimateur avec la lampe spectrale au mercure. Disposez la lampe correctement vis à vis de la fente de manière à disposer d'un éclairement maximal en sortie du collimateur.
2. Observer l'image de la fente-source à travers la lunette auto-collimatrice réglée et modifier la distance fente- objectif du collimateur pour que l'image vue à travers la lunette soit nette.
3. Ajuster la largeur de la fente et son orientation pour que son image dans la lunette soit fine et droite. 
````

### Direction du faisceau incident
Nous allons déterminer la direction du faisceau incident (non dévié par le prisme) pour se donner une origine des graduations angulaires. Cette origine correspond à la direction de propagation du faisceau sur le prisme.

````{admonition} Manipulation préliminaire
:class: tip
1. En déplaçant la lunette, venir viser la fente source avec la lunette autocollimatrice, c'est-à-dire que l'image de la fente doit se situer à la croisée du réticule de la lunette.
2. Relever alors la position de la lunette, repérée par un angle sur la graduation située sous la lunette autocollimatrice, angle que l'on notera $\theta_0$.
````

### Orientation de la plateforme et de la lunette
Ces réglages n'étant pas au programme, appeler le professeur pour qu'il les réalise.

## Goniomètre à prisme

### Mesure de l'angle A
````{admonition} Manipulation
:class: tip
1. Expliquer comment peut-on utiliser le d'autocollimation de la lunette (éclairage interne) pour déterminer l'angle correspond à la normale d'une face du prisme.
2. Proposez une méthode, utilisant la détermination de l'orientation des faces, pour mesurer l'angle A au sommet du prisme.
3. Réaliser cette manipulation et obtenir l'incertitude sur $A$ __par propagation des variances__ à partir des mesurandes directs et de leurs incertitudes.
````


### Observation qualitative du minimum de déviation
Le goniomètre est maintenant réglé, l'angle $\theta_0$ mesuré et le prisme posé correctement.

````{admonition} Manipulation : Variation de la déviation en fonction de l'angle d'incidence
:class: tip
On ne s'intéresse dans ce paragraphe qu'à la raie verte du mercure.

```{figure} ./images/AnalyseSpec_Prisme_Deviation.jpg
:name: deviation
:align: center
```
1. En vous inspirant de la [figure](deviation), proposer un protocole permettant de mesurer l'angle de déviation D pour un angle d'incidence donné (angle formé entre la direction du faisceau incident et celle du faisceau émergent).
2. Choisir un angle d'incidence permettant d'observer les rayons sortant par la lunette et faire tourner la plateforme pour observer le minimum de déviation.
2. Commencez par mesurer la déviation minimale $D_m$ observée pour la raie verte. Expliquer quel est l'intérêt de travailer au minimum de déviation.
````

  
### Minimum de déviation et longueur d'onde
Vous venez d'observer l'existence d'un minimum de déviation $D_m$, unique pour une onde monochromatique. Nous allons maintenant déterminer le minimum de déviation pour chaque longueur d'onde du mercure. Cette étude servira d'étalonnage pour mesurer la longueur d'onde du doublet du sodium.

On donne les longueurs d'onde des raies du mercure :

|Intensité | Couleur | Longueur d'onde (nm) |
|:-|:-:|-:|
|intense | Violet 2 | 404,7 |
|p âle | Violet 1 | 407,8 |
|intense | bleu violet | 435,8 |
|pâle | vert bleu | 491,6 |
|très intense | vert | 546,1 |
|intense | jaune | 577,0 et 579,1|

On rappelle qu'on peut relier l'angle de déviation minimal à l'indice de réfraction du prisme :

$$
n = \frac{\sin(\frac{D_m+A}{2})}{\sin(\frac{A}{2})}
$$

De plus, le verre est un milieu dispersif qui suit normalement la loi de Cauchy reliant l'indice de réfraction à la longueur d'onde :

$$
n(\lambda)=a+\frac{b}{\lambda^2}
$$

````{admonition} Manipulation : Etalonnage
:class: tip
1. Déterminez la déviation minimale $D_m(\lambda)$ pour chacune des raies du spectre visible du mercure ainsi que les incertitudes sur $D_m$ (pour chaque source non négligeable).
2. Utiliser la cellule ci-dessous pour déterminer les incertitudes sur les Dm, les indices de réfraction $n$ associés et leur incertitude. On utilisera une méthode de Monte-Carlo car les relations entre les grandeurs ne sont pas du tout linéaires.
3. Obtenir les coefficient $a$ et $b$ du modèle de Cauchy pour le prisme par régression linéaire. On pensera à vérifier avant et après régression la cohérence du modèle et à réaliser les représentations graphiques nécessaires. (On pourra négliger les incertitudes sur les longueurs d'onde).
````
__Pensez à stocker les vecteurs ou tableaux des N simulations pour utilisation ultérieur.__

```{code-cell}
"""Ne pas oublier les bibliothèques scientifiques"""

```

### Application à la spectrométrie
La spectrométrie consiste à déterminer le spectre d'un signal lumineux. On va déterminer la longueur d'onde du doublet du sodium attendu théoriquement aux __longueurs d'onde 589,0nm et 589,6nm__.

````{admonition} Manipulation
:class: tip
1. Remplacez la lampe au mercure par une lampe au sodium.
2. Déterminez expérimentalement la(les) longueur(s) d'onde du spectre de cette lampe, avec leurs incertitudes par simulation de Monte-Carlo. Préciser le protocole mis en place.
3. Comparez à la valeur tabulée
4. Peut-on distinguer le deux raies ou doit-on se contenter de la longueur d'onde moyenne du doublet?
````

```{code-cell}
"""Pensez à réutiliser les variables précédentes."""

```


## Augmentation de la résolution: utilisation d'un réseau

Remplacer le prisme par le réseau à disposition (_en toute rigueur, on devrait recommencer les réglages d'orientation mais on ne le fera pas ici par manque de temps, vérifier simplement que vous observer des raies en sortie_).

Comme précédemment, la mesure est plus précise au minimum de déviation mais pour gagner du temps sur l'exploitation. On va se placer en incidence normale $i = 0$.

````{admonition} Manipulation
:class: tip
1. Sachant que pour $p=0$, $i=0$ et que le réseau est partiellement réfléchissant. Proposer une méthode utilisant l'éclairage interne de la lunette pour bien placer le réseau tel qu'on soit en incidence normale puis réaliser cette manipulation.
2. Proposer puis réaliser un protocole permettant permettant de remonter aux valeurs des deux longueurs d'onde du doublet (il n'est pas demandé de calcul d'incertitude).
````