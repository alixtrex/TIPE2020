# TIPE2020

Projet : TIPE 2020, NON abouti, En pause

[L'algorithme ne fonctionne pas pour des raisons non déterminées]

Bibliographie:

[1] “Texture analysis and Synthesis” par Li-Yi Wei et Marc Levoy 
http://graphics.stanford.edu/projects/texture/

[2] “Graphcut Textures: Image and Video Synthesis Using Graph Cuts” par GVU Center / College of Computing ,Georgia Institute of Technology
https://www.cc.gatech.edu/cpl/projects/graphcuttextures/gc-final.pdf


Description générale (fait en groupe):

Algorithme de synthèse de texture par regroupement d’images

Le but du tipe est de concevoir un algorithme qui soit capable avec deux images au départ, de créer une nouvelle image de taille plus grande sans avoir de démarcation. 
( Voir [1] pour des exemples)

Pour cela, on utilise des images en noir et blanc. On découpe l’algorithme en trois parties: le chevauchement des deux images, puis la coupure dans cette zone de chevauchement ,et enfin le recollement. 

I- Chevauchement

    Le chevauchement est la première étape du recollement d’image. Elle consiste à déterminer la zone où se superposeront  les images, c’est-à-dire l’endroit où sera cherchée la coupure. Cette zone se situe à l’extrémité droite d’une image, et à l'extrémité gauche de l’autre.
Pour cela, on cherche à minimiser la moyenne des
distances entre pixels. 

II- Coupure

    La coupure s’intéresse à la recherche d’un chemin allant du bord haut au bord bas de l’image minimisant les différences de teintes des deux images. Le chemin progresse entre les pixels et avance segment par segment, entre les deux images.

III-Recollement

    Pour la dernière partie, on crée l’image finale. Pour cela, on va “découper” les deux images en suivant la coupure avant de les recoller.
Finalement, l’image est plus grande et semble uni (on ne peut normalement pas voir la coupure).

Ce type d’algorithme peut permet de créer des images totalement artificiels. Ici, on se contente de traiter une image en 2D fixe. Mais on pourrait l’étendre à des vidéos pour faire un fondu entre deux scènes par exemple.
Une application peut être la possibilité pour un appareil photo de faire des panoramiques de manière automatique.

