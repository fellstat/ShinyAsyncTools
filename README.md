# The ipc Package

In computer science, asynchronous processing is critical for performing a wide array of tasks, from high performance computing to web services. Communication between these disparate asynchronous processes is often required. Currently the statistical computing language R provides no built in features to handle interprocess communication. Several packages have been written to handle the passing of text or binary data between processes (e.g. [@txtq], [@liteq], and [@rzmq]).

What is lacking is a framework to easily pass R objects between processes along with an associated signal, and have handler functions automatically execute them in the receiving process. Additionally, it is desirable to have a system that can be backed flexibly either through the file system or a database connection The `ipc` R package aims to fill this void.

There is particular focus on supporting asynchronous evaluation in Shiny applications. Examples are provided showing how to perform useful tasks such as:

* Updating reactive values from within future
* Progress bars for long running async tasks
* Interrupting async tasks based on user input.

## Installation
To install the latest version from CRAN
run:
```
install.packages("ipc")
```
To install the latest development version from the github repo run:
```
# If devtools is not installed:
# install.packages("devtools")

devtools::install_github("fellstat/ipc")
```

## Resources


* For a more detailed description of what can be done with the ``ipc`` package, **[see the introductory vignette](http://htmlpreview.github.io/?https://github.com/fellstat/ipc/blob/master/inst/doc/shinymp.html)**.

To run an example application locally use:
```
library(ipc)
shinyExample()
```
