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

L'objectif du TP est de construire un analyseur de spectre analogique, c'est-à-dire un dispositif capable de tracer (ici à l'oscilloscope) le spectre d'un signal électrique entrant.

## Etude de chaque étage

### Filtre sélectif
```{figure} ./images/AnalyseSpec_Passe_Bande.jpg
:name: filtre
:align: center
Filtre passe-bande
```

Pour réaliser un filtre suffisamment sélectif, on choisit ce [montage](filtre) appelé filtre à structure de Rauch. Les valeurs des composants sont: $R_1 = 10k\Omega; R_2 = 220\Omega; R_3 = 330k\Omega; C = 10nF$. _On s'assurera que l'A.O. ne sature pas durant les manipulations._

````{admonition} Manipulation
:class: tip
1. Vérifier que le filtre est bien du type attendu puis déterminer expérimentalement la fréquence de résonance ainsi que la bande passante du filtre et le gain à la résonance.

On donne les valeurs théoriques pour comparaison :

\begin{align*}
  f_0 &= \frac{1}{2 \pi C} \sqrt{\frac{R_1+R_2}{R_1R_2R_3}}\\
  \Delta f &= \frac{1}{\pi R_3 C}\\
  H_{\max}&=\frac{R_3}{2R_1}
\end{align*}
````

### Etude du multiplieur
Le principe et l'utilisation du multiplieur a déjà été réalisée précédemment. Vérifier simplement son bon fonctionnement en vérifiant que la multiplication de deux signaux de fréquences éloignées (_ce ne sera pas le cas ensuite par contre_) réalise bien une modulation d'amplitude.

* Le multiplieur a un coefficient de multiplication d'environ $k=0,1\rm{V^{-1}}$
* On rappelle qu'il doit être alimenté par une alimentation symétrique.

### Etalonnage de l'analyseur de spectre

````{admonition} Manipulation
:class: tip
1. Réaliser le montage complet et choisir comme signal $e(t)$ à analyser un signal sinusoïdal de fréquence $500Hz$.
2. Prendre pour $v(t)$ un signal sinusoïdal d'amplitude 5V. On démarrera avec une fréquence $f_0$ pour $v(t)$.
3. Visualiser à l'oscilloscope les tensions $e(t)$ et $s(t)$. Quand on fait varier la fréquence $f_v$ (avec on le rappelle $f_v \geq f_0$), observe-t-on ce qu'on attend théoriquement? On précisera les similitudes et les différences.
4. À l'aide de l'analyseur de spectre que vous avez monté, vérifier la(les) fréquence(s) contenues dans $e(t)$.
5. Étalonner l'analyseur de spectre en déterminant le rapport $G_T =S / E$ (où S est l'amplitude du signal de sortie $s(t)$ et E celle du signal d'entrée $e(t)$) lorsque S est maximale. Rappeler pourquoi peut-on considérer que ce rapport sera le même quelque soit le signal et quelque soit la composante fréquentielle observée? En pratique, quelle sont les limites de cette hypothèse?
6. Estimer l'incertitude sur $G_T$ par propagation des variances.
````

### Analyse manuelle d'un signal créneau
On peut maintenant réaliser l'analyse spectrale de différents signaux $e(t)$. Le signal $e(t)$ que nous allons analyser est un créneau symétrique, de valeur moyenne nulle, et de fréquence 200Hz et d'amplitude 5V. __ATTENTION AUX PHENOMENES DE SATURATION – DIMINUER L'AMPLITUDE DE $e(t)$ SI BESOIN MAIS SURTOUT PAS DE $v(t)$__ (à cause de l'étalonnage).

On rappelle la décomposition de Fourier d'un signal créneau de période T et d'amplitude $E_0$ :

\begin{equation}
  e(t) = \frac{4E_0}{\pi} \sum\limits_{p=0}^{+\infty} \frac{1}{2p+1} \sin((2p+1)\frac{2 \pi}{T}t)
\end{equation}

Cette analyse manuelle permettra de bien comprendre le principe de sélection de l'analyseur.

````{admonition} Manipulation
:class: tip
1. Préciser le protocole permettant de déterminer les fréquences et les amplitudes du fondamental et des harmoniques du signal.
2. Réaliser les mesures pour le fondamental et une harmonique. Commenter la précision des mesures? Quels sont les facteurs qui causent ces imprécisions? (On ne demande pas de mesure d'incertitude).
````

### Analyse automatique d'un signal créneau

Pour automatiser l'analyser précédente, nous allons faire varier automatiquement la fréquence $f_v$ sur une plage choisie: on parle de wobulation.

Avant de réaliser l'automatisation, il convient d'observer ce que le GBF délivre en wobulation.

````{admonition} Manipulation préliminaire
:class: tip
1. Débrancher le GBF délivrant $v(t)$ du circuit et observer ce signal sur l'oscilloscope.
2. Activer la wobulation en démarrant à $f_0$ jusqu'à $5kHz$ en faisant en sorte que le balyage en fréquence dure 1 secondes. Des explications sur les réglages sont donnés [ici](wobulation). On déterminera la relation $u(f)$ donnant la tension délivrée par la sortie `SWEEP IN/OUT` en fonction de la fréquence.
3. Observer que la fréquence du signal varie effectivement au cours du temps. Vous pouvez rebrancher le GBF sur le multiplieur et observer la sortie. Observe-t-on "l'amplitude" en sortie ?
````

Pour palier à ce problème, on propose de placer un [montage détecteur de crête](detecteur) en sortie.

```{figure} ./images/AnalyseSpec_Detecteur_Crete.jpg
:name: detecteur
:align: center
Détecteur de crêtes
```

On rappelle que pour qu'il réalise sa fonction, il faut que :
* $RC \gg \frac{1}{f}$ où f est la fréquence instantanée de $s(t)$
* $RC \ll \Delta t$ où $\Delta t$ est le temps mis par le wobulateur pour aller de $f_{\min}$ à $f_{\max}$

````{admonition} Manipulation
:class: tip
1. Proposer des valeurs cohérentes pour R et C avec les contraintes imposées.
2. Observer alors le tracé expérimental du spectre et retrouver les valeurs des fréquence du fondamental et des harmoniques des signaux avec leurs incertitudes (on utilisera __la propagation des variances__ pour estimer les incertitudes des mesurandes indirectes). Représenter graphiquement (à la main) le spectre avec les incertitudes.
````