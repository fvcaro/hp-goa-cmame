# A Painless Multi-level Automatic Goal-Oriented $hp$-Adaptive Coarsening Strategy for Elliptic and non-Elliptic Problems

This repository contains the LaTeX code for compiling the research paper titled "A Painless Multi-level Automatic Goal-Oriented $hp$-Adaptive Coarsening Strategy for Elliptic and non-Elliptic Problems." The paper can be accessed [here](https://www.sciencedirect.com/science/article/pii/S0045782522005965).

## Introduction

The research paper presents a novel approach for achieving multi-level automatic goal-oriented adaptive coarsening in solving elliptic and non-elliptic problems. It proposes a strategy that simplifies the process and minimizes the effort required for achieving highly efficient mesh coarsening.

## Instructions

To compile the paper, follow these steps:

1. Clone this repository to your local machine:

```
git clone https://github.com/fvcaro/hp-goa-cmame.git
```

## Tikz

This project contains a set of externalized tikz with the **list and make** mode.

When you compile the general latex file, it will generate a makefile that lists all the figures and their recipes. You then need to make it and compile again.

1. pdflatex unref_general.tex
1. make -f unref_general.makefile
1. pdflatex unref_general.tex

Note that the repo already contains the external figures compiled. You should not have to run the makefile. You will need to do it only if you modify the externalized figures.

Note that only the **named** figures will be externalized thanks to :

```
\tikzset{external/only named=true}
```

To name a figure and externalize it place **just before** the _\begin{tikzpicture}_:

```
\tikzsetnextfilename{filename}
\begin{tikzpicture}
... figure code ...
\end{tikzpicture}
```

It will generate a **filename.pdf** that will later be included automatically.

For details on this feature see, section 5.6 of the manual: http://mirrors.ctan.org/graphics/pgf/contrib/pgfplots/doc/pgfplots.pdf
