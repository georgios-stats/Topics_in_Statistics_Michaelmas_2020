<!-- -------------------------------------------------------------------------------- -->

<!-- Copyright 2020 Georgios Karagiannis -->

<!-- This file is part of Topics_in_Statistics_Michaelmas_2020 -->
<!-- (Topics in Statistics III/IV (MATH3361/4071) Michaelmas term 2020) -->
<!-- which is the material of the course (Topics in Statistics III/IV (MATH3361/4071) -->
<!-- taught by Georgios P. Katagiannis in the Department of Mathematical Sciences   -->
<!-- in the University of Durham  in Michaelmas term in 2020 -->

<!-- Topics_in_Statistics_Michaelmas_2020 is free software: you can redistribute it and/or modify -->
<!-- it under the terms of the GNU General Public License as published by -->
<!-- the Free Software Foundation version 3 of the License. -->

<!-- Topics_in_Statistics_Michaelmas_2020 is distributed in the hope that it will be useful, -->
<!-- but WITHOUT ANY WARRANTY; without even the implied warranty of -->
<!-- MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the -->
<!-- GNU General Public License for more details. -->

<!-- You should have received a copy of the GNU General Public License -->
<!-- along with Topics_in_Statistics_Michaelmas_2020 If not, see <http://www.gnu.org/licenses/>. -->

<!-- -------------------------------------------------------------------------------- -->



Aim
===

The handout aims at familiarising students with the statistical package
RJAGS, and with more ‘sophisticated’ Bayesian hierarchical models than
those in the Lecture handouts.

Students will be able to:

-   use cvd package in R, by using the reference material, for the
    statistical analysis of contingency tables.

------------------------------------------------------------------------

Material:
========

Handouts and Exercises  for [Contigency tables, and Log linear models](https://github.com/georgios-stats/Topics_in_Statistics_Michaelmas_2020/tree/master/Contigency_Tables#handouts)  


Handouts and Exercises  for [Likelihood methods](https://github.com/georgios-stats/Topics_in_Statistics_Michaelmas_2020/blob/master/Likelihood_methods#handouts)  


Sheet for Computer practical 1 [(questions)](https://htmlpreview.github.io/?https://github.com/georgios-stats/Topics_in_Statistics_Michaelmas_2020/blob/master/Computer_practicals/saved_output/Computer_practical_1.nb.html)  ;  [(solutions)](https://htmlpreview.github.io/?https://github.com/georgios-stats/Topics_in_Statistics_Michaelmas_2020/blob/master/Computer_practicals/saved_output/Computer_practical_1_full.nb.html)  

Sheet for Computer practical 1a [(questions)](https://htmlpreview.github.io/?https://github.com/georgios-stats/Topics_in_Statistics_Michaelmas_2020/blob/master/Computer_practicals/saved_output/Computer_practical_1a.nb.html)  ;  [(solutions)](https://htmlpreview.github.io/?https://github.com/georgios-stats/Topics_in_Statistics_Michaelmas_2020/blob/master/Computer_practicals/saved_output/Computer_practical_1a_full.nb.html)  

Sheet for Computer practical 2 [(questions)](https://htmlpreview.github.io/?https://github.com/georgios-stats/Topics_in_Statistics_Michaelmas_2020/blob/master/Computer_practicals/saved_output/Computer_practical_2.nb.html)   ;   [(solutions)](https://htmlpreview.github.io/?https://github.com/georgios-stats/Topics_in_Statistics_Michaelmas_2020/blob/master/Computer_practicals/saved_output/Computer_practical_2_full.nb.html)   

------------------------------------------------------------------------

Reference list
==============

*The material below is not examinable material, but it contains
references that students can follow if they want to further explore the
concepts introduced.*

-   Reference for *R*:
    -   [Cheat sheet with basic commands for
        *R*](https://www.rstudio.com/wp-content/uploads/2016/10/r-cheat-sheet-3.pdf)
-   Reference of *rmarkdown* (optional)
    -   [R Markdown
        cheatsheet](https://www.rstudio.com/wp-content/uploads/2016/03/rmarkdown-cheatsheet-2.0.pdf)  
    -   [R Markdown Reference
        Guide](http://442r58kc8ke1y38f62ssb208-wpengine.netdna-ssl.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf)  
    -   [knitr options](https://yihui.name/knitr/options)
-   Reference for *Latex* (optional):
    -   [Latex Cheat
        Sheet](https://wch.github.io/latexsheet/latexsheet-a4.pdf)

------------------------------------------------------------------------

Setting up the computing environment
====================================

### CIS computers

1. Go to [Appsanywhere](https://appsanywhere.durham.ac.uk/login) and log in with your CIS account details  

    + <https://appsanywhere.durham.ac.uk/login>  

From AppHub, load the modules:

2. Git  (wait until it opens)   

3. LaTex (Latex - Miktex Texworks 2.9.6753)   (wait until it opens)    

4. rstudio (RStudio 1.2.5003 with RStan and Rtools)    (wait until it opens)   

<!--
### CIS computers

From AppHub, load the modules:

1.  LaTex

2.  rstudio
-->

### Your personal computers (Do not do it on CIS computers)

There is not need to do this in CIS computers as the required foftware
is (supposed to be) properly installed.

The instructions below are at your own risk…

We recommend the use of LINUX operation system.

Briefly, you need to do the following:

1.  Install LaTex (optional but recommended)
    -   Source: download it from
        <https://www.tug.org/texlive/acquire-netinstall.html>
    -   Debian: *apt-get install texlive-full*  
    -   Fedora: *yum install texlive texlive-latex*  
    -   windows: download it from
        <https://miktex.org/howto/install-miktex>
    -   macos: download it from <https://www.tug.org/mactex/>
2.  Install R computing environment version R 3.6.3 or later.
    -   Source: download the installer from: <https://cran.r-project.org/>, and install it according to the installation instructions   
    -   Debian: *sudo apt install r-base*  
    -   Fedora: *yum install -y R*  
    -   windows: download it from <https://cran.r-project.org/>
        -   I recomend tyou to install *Rtools* as well, for you to be
            able to instal R packages.  
    -   macos: download it from <https://www.tug.org/mactex/>
3.  Install the latest Rstudio (recommended)
    -   Any OS: Download it from here:
        <https://www.rstudio.com/products/rstudio/download/>

 