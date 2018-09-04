---
layout: post
title: Turning your R code into a package
---

*This is a simple tutorial on how to turn your R code into a package hosted on GitHub.*

First you need to install and then load a couple of packages.

```ruby
install.packages("devtools")   
install.packages("roxygen2")   

library(devtools)   
library(roxygen2) 
```

Next, set the folder where you want to create your package. I usually just set the working directory...

```ruby
setwd("./NameOfTheFolderToPutYourPackageIn")
```

Now we can create all the files needed to create the package.

`devtools::create("NameOfYourPackage")`   

All the files that you need should now be in your folder. Open the DESCRIPTION file in RStudio so that you can edit the appropriate lines. It should look like this:

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

Now that the DESCRIPTION file is set, we can load our R functions (as individual R scripts) into the R folder that was created by the above line of code.
Next, open the R script because we need to add a couple of lines of code to the top so that there will be help documentation when the package is downloaded. These are the lines we need to add:

`#' Insert a short description about what this function does.`   
`#'`   
`#' Insert a longer description about this function; what it does, how it works, any references, etc.`   
`#'`   
`#' @param NAME.OF.THE.FUNCTION.PARAMETER insert a short description of what the parament is`   
`#' @return A short description of what is returned by the function`   
`#' @export`   

Now that these lines are added to the top of the function there are just a couple more steps to complete the process. First, we need to set the working directory to the actually folder that the package is in.

`setwd("./The folder your package is in")`   

Then we can run this line so that a markdown document is created for the function.

`devtools::document()`   

Now your just need to push your package to GitHub using whichever method you prefer, I've been using GitHut Desktop lately.














