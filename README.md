### Français

## Introduction

La source du Guide d'utilisation de Manjaro Linux pour les débutant-e-s en LaTeX (en utilisant LyX)

Le style utilisé est [tufte-book](http://wiki.lyx.org/Layouts/Tufte-book). Il procure une disposition très professionnelle avec un minimum d'effort.

## Téléchargement

Envie d'avoir un PDF au lieu des fichiers source? La version anglaise du guide est disponible dans le [répertoire](http://sourceforge.net/projects/manjarolinux/files/release/) associé sur SourceForge.

## Installation

Afin d'avoir accès au style tufte-book dans LyX sur Manjaro, vous aurez besoin d'installer les paquets suivants :

    sudo pacman -S lyx texlive-latexextra texlive-pictures ttf-comfortaa ghostscript

Les dépendances de base devraient être téléchargées en même temps que LyX. Le style tufte-book requiert quant à lui des librairies supplémentaires. Rappelez-vous de reconfigurer LyX après avoir installé les nouvelles librairies!

## Couverture

La couverture actuelle a été créée avec Inkscape. LyX permet d'insérer des fichiers PDF sans anicroche. Afin de simplifier les choses, la couverture du guide devrait donc être exportée en fichier PDF.

![Manjaro User Guide cover](https://raw.githubusercontent.com/pattedetable/french-manjaro-user-guide/master/cover.png)

## Génération

Pour générer la version PDF du guide en ligne de commande au lieu de l'exporter à partir de LyX lui-même, vous pouvez utiliser la série de commandes suivante :

    lyx --export pdflatex manjaro-user-guide.lyx
    pdflatex manjaro-user-guide
    texindy --language english manjaro-user-guide.idx
    pdflatex manjaro-user-guide
    pdflatex manjaro-user-guide
    gs -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/printer -sOutputFile=manjaro-user-guide-printer.pdf manjaro-user-guide.pdf

Oui, ```pdflatex``` nécessite plusieurs exécutions.

### English

## Introduction

The Manjaro Linux Beginner's User Guide typeset in LaTeX (using LyX).

The style in use is [tufte-book](http://wiki.lyx.org/Layouts/Tufte-book). This provides a very professional layout with minimal fuss.

## Download

Want a PDF instead of the source? Grab it from the associated [release](http://sourceforge.net/projects/manjarolinux/files/release/) directory on SourceForge.

## Installation

To enable the tufte-book layout within LyX on Manjaro you will need to install the following packages:

    sudo pacman -S lyx texlive-latexextra texlive-pictures ttf-comfortaa ghostscript

Installing LyX should pick up the base dependencies; tufte-book requires the extra libraries. Remember to reconfigure LyX after installing the new libraries!

## Cover art

Current cover art is created in Inkscape. LyX will neatly insert/append PDF files - to make things easy cover art should therefore be exported as a PDF document.

![Manjaro User Guide cover](https://raw.githubusercontent.com/manjaro/manjaro-user-guide/master/cover.png)

## Generation

To generate the PDF from a command line rather than exporting from within LyX you can use the following:

    lyx --export pdflatex manjaro-user-guide.lyx
    pdflatex manjaro-user-guide
    texindy --language english manjaro-user-guide.idx
    pdflatex manjaro-user-guide
    pdflatex manjaro-user-guide
    gs -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/printer -sOutputFile=manjaro-user-guide-printer.pdf manjaro-user-guide.pdf

Yes, ```pdflatex``` does require multiple runs.
