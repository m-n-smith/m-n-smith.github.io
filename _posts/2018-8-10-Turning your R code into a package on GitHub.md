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

All the files that you need should now be in your folder. Open the DESCRIPTION file in RStudio so that you can edit the appropriate lines.
It should look like this:

`Package: Name of your package`
`Title: Give it a short title that explains your package`
`Version: 1.0`
`Authors: Your name`
`Description: Short description about what your package does and why it is important`
`Depends: put the names of the libraries your package needs to run. They should be listed like this: fields, raster, rgdal, etc.`
`License: Name of the open source license you are using`
`Encoding: UTF-8`
`LazyData: FALSE`
`LazyLoad: yes`
`RoxygenNote: 6.0.1`


