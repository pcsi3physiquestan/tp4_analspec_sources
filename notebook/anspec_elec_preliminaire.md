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

## Principe général

On considère un signal électrique $e(t)$ à analyser, c'est-à-dire dont on veut connaître les fréquences qui le composent ET les amplitudes associées. Pour ce faire, nous allons réaliser un montage à plusieurs étages qui doit:

* sélectionner, suivant les réglages, une des composantes fréquentielles du signal $e(t)$
* donner une information sur son amplitude.

On assemble alors un multiplieur analogique et un filtre passe-bande sélectif de fréquence centrale fixe de bande passante $\Delta f$ comme indiqué sur [le schéma de principe](analspec_principe).

```{figure} ./images/AnalyseSpec_Analyseur_Principe.jpg
:name: analspec_principe
:align: center
Principe de construction d'un analyseur de spectre
```

Caractéristiques du montage:

* La tension $v(t)$ est un signal sinusoïdale d'amplitude V et de fréquence $f_v$ connues et réglables.
* Le multiplieur est un circuit intégré dont la fonction est de sortie une tension: $u(t)=ke(t)v(t)$.
* la fréquence propre $f_0$ du filtre passe-bande est fixe et connue.
* On impose $f_vf_0$ dans la manipulation.
* On admet qu'un tel dispositif ne peut correctement mesurer des fréquences que jusqu'à $2f_0$

## Etude théorique

Dans l'étude théorique proposée ici, on assimile le filtre passe-bande à son comportement idéal: seules les fréquences $f \in [f_0 - \frac{\Delta f}{2}, f_0+ \frac{\Delta f}{2} ]$ sont transmises par ce filtre avec un gain réel $G_{\max}$ constant.

````{admonition} Exercice
:class: tip

1. Cas d'un signal à analyser sinusoïdal: $e(t)=Ecos(2 \pi f t)$ avec f inconnue et d'un filtre idéal sélectif: $\Delta f =0$ (seule la fréquence de résonance $f_0$ passe).
    1. Déterminer $u(t)$. En déduire son spectre. Comparer ce spectre à celui de $e(t)$ et $v(t)$. Pourquoi cela montre-t-il que le multiplieur n'est pas un composant linéaire?
    2. A quelle condition sur $f_v$, la fréquence $f_v - f$ peut-elle être sélectionnée par le filtre (notée Condition 1)? Peut-on, avec les caractéristiques imposée sélectionner la fréquence $f_v+ f$?
    3. Sachant que $f_v$ est connue, proposer un protocole pour déterminer la fréquence f inconnue.
    4. On suppose la condition 1 réalisée, donner l'expression temporelle de $s(t)$ puis son spectre. En déduire que la connaissance de $G_{\max}$, V et k permet de remonter à l'amplitude E.
    5. On définira le rapport: $G_T= \frac{\textrm{Amplitude(s(t))à la résonance}}{\textrm{Amplitude de la composante de e(t)sélectionnée}}$. D'après l'étude précédente, ce gain $G_T$ dépend-il de la composante sélectionné? Expliquer l'intérêt expérimental de cette observation.
2. Cas d'un signal quelconque $e(t)=\sum E_n \cos(2 \pi f_n t+ \phi_n)$. On suppose toujours $\Delta f=0$.	
    1. Expliquer grâce à l'analyse précédente qu'un tel dispositif permet de remonter au spectre de $e(t)$ en faisant varier la fréquence $f_v$. On représentera notamment l'évolution de l'amplitude de $s(t)$ notée sm ($f_v$) en fonction de $f_v$ pour le justifier.
3. Prise en compte de la bande passante finie $\Delta f >0$.
    1. Pour un signal sinusoïdale, représenter à nouveau l'évolution de l'amplitude $s_m$ ($f_v$) en fonction de $f_v$ Quelle différence observe-ton?
    2. En reprenant le cas d'un signal quelconque, expliquer pourquoi la sélectivité du filtre (largeur de la bande-passante) va influer sur la résolution de l'analyseur de spectre.
4. Le filtre ne sera pas idéal. Cela joue-t-il en faveur ou en défaveur de la résolution de l'analyseur de spectre?

````