## Introduction

The Manjaro Linux Beginner's User Guide typeset in LaTeX (using LyX).

The style in use is [tufte-book](http://wiki.lyx.org/Layouts/Tufte-book). This provides a very professional layout with minimal fuss.

## Installation

To enable the tufte-book layout within LyX on Manjaro you will need to install the following packages:

    sudo pacman -S lyx texlive-pictures texlive-latexextra ttf-comfortaa

Installing LyX should pick up the base dependencies; tufte-book requires the extra libraries. Remember to reconfigure LyX after installing the new libraries!

## Cover art

Current cover art is created in Inkscape. LyX will neatly insert/append PDF files - to make things easy cover art should therefore be exported as a PDF document.

![Manjaro User Guide cover](https://raw.githubusercontent.com/manjaro/manjaro-user-guide/master/cover.png)
