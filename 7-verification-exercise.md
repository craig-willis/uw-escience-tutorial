#  Exercise: Verifying Published Research

Let's take a real-world example and look at what it takes to verify computational reproducibility of someone else's work. This is an example from the American Journal of Political Science. From the [AJPS verification policy](https://ajps.org/ajps-verification-policy/):

> When the final draft of the manuscript is submitted, the materials will be verified to confirm that they do, in fact, reproduce the analytic results reported in the article.

Imagine that you are assigned to review the submitted package for computational reproducibility. A common operationalization of computational reproducibility is to confirm that the data and code provided can be used to recreate the figures and tables in the article.

The file [compendium.zip](https://github.com/craig-willis/uw-escience-tutorial/raw/master/compendium.zip) contains the following replication package:

> Lelkes, Yphtach; Sood, Gaurav; Iyengar, Shanto, 2015, "Replication Data for: The Hostile Audience: The Effect of Access to Broadband Internet on Partisan Affect", https://doi.org/10.7910/DVN/W1YJZQ, Harvard Dataverse, V1

* Download and extract the [compendium.zip](https://github.com/craig-willis/uw-escience-tutorial/raw/master/compendium.zip)
* Download the [paper](https://onlinelibrary.wiley.com/doi/abs/10.1111/ajps.122370) associated with this dataset
* Read the `readme.txt`
* Start an RStudio instance in Whole Tale
* Upload the contents of the extracted archive
* Try to reproduce Figure 1 and Table 1

Questions:
* Were you able to reproduce the the figure and table in the paper?
* What version of R was used to create this package?
* What other libraries are used?
* Was it easy to understand which files were associated with the figure and table?
* What could be improved?
* What is the source of the data used in the map?
