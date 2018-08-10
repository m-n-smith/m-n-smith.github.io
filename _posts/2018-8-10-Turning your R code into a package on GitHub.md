---
layout: post
title: Turning your R code into a package
---

### This is a simple tutorial on how to turn your R code into a package hosted on GitHub.

First you need to install and then load a couple of packages.

`install.packages("devtools")`   
`install.packages("roxygen2")`   

`library(devtools)`   
`library(roxygen2)`   

Next, set the folder where you want to create your package. I usually just set the working directory.

`setwd("./NameOfTheFolderToPutYourPackageIn")`   

Now we can create all the files needed to create the package.

`devtools::create("NameOfYourPackage")`   


