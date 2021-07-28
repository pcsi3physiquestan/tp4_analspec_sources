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

(wobulation)=
# Wobulation en pratique

Le GBF TG500 possède une fonction wobulation qui permet de faire varier la fréquence du signal délivré. Les caractéristiques du réglages sont les suivantes:

* activation du balayage par le bouton `SWEEP IN/OUT` enfoncé.
* choix d'un balayage linéaire
* fréquence minimale $f_{\min}$ (maintien du bouton `START` + réglage de fréquence (_molette_))
* fréquence maximale $f_{\max}$ (maintien du bouton `STOP` + réglage de la molette `STOP`)
* temps mis pour aller d'une fréquence à l'autre $\Delta t$ (réglage `RATE`)

````{important}
La durée $\Delta t$ n'est pas affichée. Pour la régler. Il faut sortir le signal de la connectique BNC `SWEEP IN/OUT`. Il délivre une tension affine en la fréquence instantanée du signal :

$$u(t) = \frac{f_{\max}-f_{\min}}{\Delta t} t+f_{\min} $$

En pratique, $u$ vaut $3V$ pour $f_{max}$ et $0V$  pour $f_{min}$. 

Il faut donc : 
* brancher cette voie sur l'oscilloscope
* régler le `Rate` pour que la pente dure bien le temps voulu.

__Cette voit sera aussi utilisée pour la synchronisation de l'oscilloscope car vous serez obligé à ce stade de passer en synchronisation manuelle.__

````