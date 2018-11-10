---
layout: post
title:  "Bibliographie APA"
date:   2018-10-09 10:34:57 +0200
---

Il y a [un site de l'ENS](https://www.tuteurs.ens.fr/logiciels/latex/bibtex.html) très bien foutu qui explique tout en détail le principe de la bibliographie de LaTeX.

Il faut donc placer la bibliographie là où elle est censée se trouver dans le document (logiquement à la fin) intégrant les différents fichiers .bib

    \bibliography{file1.bib}
    \bibliography{file2.bib}    

Etc.

S'agissant de la norme APA, il suffit d'intégrer le style avec APA like.

    \bibliographystyle{apalike}

J'obtiens par exemple avec :

     \cite[pp. 132-137]{bach}

Soit bach la référence de l'ID correspondant dans le fichier bib, ce qui donne dans le texte :

Lorem ipsum in dolor ipset [Bachelard, 1938, pp. 132-137]

Je ne sais pas si cela vient de ma distribution (Tex Live) mais je me suis retrouvé avec des crochets. Du coup j'ai intégrer un package qui me fait une mise en forme plus standard.

    \usepackage{natbib}

Attention, natbib utilise un système de citations différent, il utilise soit citet soit citep. Avec citet, on obtient l'auteur en dehors des parenthèses et avec citep l'auteur dedans.

    \citet{bach}	    -->    	Bachelard (1938)
    \citep{bach}	    -->    	(Bachelard, 1938)

Dans tous les cas, la bibliographie sera tout aussi bien abondée. En résumé : 

<script src="https://gist.github.com/stephmnt/1bbc9de56706c624c1a6e43abf441c1f.js"></script>
