---
layout: page
title: Software
permalink: /Software/
---

<h1 class="page-title">{{ page.title | escape }}</h1>

#### Overview

The second half of the course will involve hands-on tutorials for methods in macroevolution. We will ensure that everyone has the necessary software installed before this part of the course begins. 

#### Required Software

<div class="divider"></div>

##### Text editor

Everyone should have a good text editor. Here are some that we recommend:

* [Sublime Text](https://www.sublimetext.com/) (Linux, Windows, Mac OSX)
* [Atom](https://atom.io) (Linux, Windows, Mac OSX)
* [BBEdit](https://www.barebones.com/products/bbedit/) (Mac OSX)
* [Notepad++](https://notepad-plus-plus.org/) (Windows)
* Of course Vim/vi or Emacs are great (if that is your thing)

<div class="divider"></div>


##### RevBayes

RevBayes is a program for Bayesian phylogenetic inference. You can download compiled binaries for Mac OSX and Windows here: [http://revbayes.github.io/software.html](http://revbayes.github.io/software.html). If you have the Linux operating system, please follow the instructions for compiling the program from source.

For Bayesian phylogenetic inference, it is also useful to have the program Tracer for visualizing MCMC samples of numerical parameters. You can download Tracer here: [http://tree.bio.ed.ac.uk/software/tracer/](http://tree.bio.ed.ac.uk/software/tracer/).

**Put RevBayes in your Path**

If you are working with a Unix operating system, it is recommended that you put RevBayes in your system path. You may also be able to do this on Windows using [CygWin](https://www.cygwin.com/).

To do this, open your terminal (in Mac OSX you can find this in /Applications/Utilities/Terminal). You will need to edit your `.bash_profile` file. Here is a simple way of doing this using the `nano` text editor:

Step 1: Save RevBayes in your favorite place to store such things on your computer. Find the absolute path to the directory containing the `rb` binary. If you downloaded the Mac OS X version, then this direcotry is called `RevBayes\ 3`. On way to find the absolute path to a directory is to drag the folder into your Terminal. If you do this, it will print the full path. For example, I put the directory on my `Desktop` and the full path is: `/Users/tracyh/Desktop/RevBayes\ 3`. Note that the `\ ` is a Unix way of saying there is a space in the path. Usually, it isn't good form to have spaces in directory or file names. 

Step 2: In the terminal make sure you are in your home directory:

```
cd ~
```

Step 3: Open the `.bash_profile` file using `nano`. If you don't already have one, this will create the file:

```
nano .bash_profile
```

Step 4: Add the export path line to the file. If the file already has stuff in it when you opened it, just add the line at the bottom. The part that says `<your path>` should be the absolute path to the RevBayes directory. For me, I would replace `<your path>` with `/Users/tracyh/Desktop`. (If your `rb` binary is in a folder that is not called `RevBayes\ 3`, then you would replace that part of the directory path, as well.)

```
export PATH=$PATH:<your path>/RevBayes\ 3
```

Step 5: Save the file using _control+o_ and exit `nano` using _control+x_. Then quit the Terminal application. 

Step 6: Re-open the Terminal. Your new `.bash_profile` file will be automatically sourced. Now you should be able to execute the `rb` binary from any directory. In the Terminal, just type:

```
rb
```

This should give you:

```
RevBayes version (1.0.6)
Build from master (e8e91f) on Sat Sep 23 17:41:05 CEST 2017

Visit the website www.RevBayes.com for more information about RevBayes.

RevBayes is free software released under the GPL license, version 3. Type 'license()' for details.

To quit RevBayes type 'quit()' or 'q()'.

> 
```

_It works!_

<div class="divider"></div>

##### R

Install R and the suite of comparative phylogenetic methods packages.

1. Download and R for your operating system: [https://cran.r-project.org](https://cran.r-project.org/)
2. We recommend using **RStudio** [https://www.rstudio.com](https://www.rstudio.com/) as your interactive development environment for `R`.

Once you have R installed and you can open the R terminal, you can install several packages needed for performing comparative phylogenetic analyses. We will do this using the CRAN [phylogenetics task view](https://cran.r-project.org/web/views/Phylogenetics.html) that was created by [Brian O'Meara](http://brianomeara.info/). To do this, open R and execute the following lines:

```
install.packages("ctv")
library("ctv”)
install.views("Phylogenetics”)
```

It is possible that there are dependencies that you may have to install before you can successfully execute the task view. (We can troubleshoot these issues in class.)

The CRAN phylogenetics task view uses the release version of the `geomorph` pacakge. For our class, we will be using some more advanced methods in this package. So we will install the development version. To do this execute these lines in R:

```
install.packages("devtools")
devtools::install_github("geomorphR/geomorph",ref = "Develop")
```


<div class="divider"></div>

