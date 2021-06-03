Deploying midfielddata
================

![](../resources/p007-header.jpg) <small> <br> <i>Drat</i> by cranky
messiah is licensed under
<a href="https://creativecommons.org/licenses/by-nc/2.0/legalcode">CC
BY-NC 2.0</a> <br> </small>

## Introduction

We use the drat package to deploy the midfielddata package as a GitHub
repository instead of deploying it to CRAN because the package exceeds
the CRAN size limits.

These guidelines are a quick overview of how to go about updating the
midfielddata package when needed. You can read more about it at Dirk
Eddelbuettel’s [Drat basics for package
authors](https://eddelbuettel.github.io/drat/vignettes/dratforauthors/)

First time only,

-   Clone a local copy of the MIDFIELDR drat repo.
-   Install the drat package.

## Update the drat repo

-   Once the work in the midfielddata package is complete, run R CMD
    build to produce the `midfielddata_x.x.x.tar.gz` file, where `x.x.x`
    is the version number.
-   Note the path to the local drat repo, e.g., `C:/path/to/local/drat`.
-   In R change your working directory to the file location of the
    `.tar.gz` file and run:

``` r
        drat::insertPackage("midfielddata_x.x.x.tar.gz", "C:/path/to/local/drat")
```

-   Check by navigating to the local directory `drat\src\contrib`. You
    should see the latest `midfielddata_x.x.x.tar.gz` file there  
-   Commit and push to the GitHub repo
-   Check by installing the new version of midfielddata locally by
    running

``` r
       install.packages("midfielddata", repos = "https://MIDFIELDR.github.io/drat/", type = "source")
```

-   Run `library("midfieldata")` and open the data files to confirm that
    your changes appear.

## References

<div id="refs" class="references csl-bib-body">

<div id="ref-drat:2021" class="csl-entry">

1\. Eddelbuettel D (2021) <span class="nocase">drat: ’Drat’ R Archive
Template</span>. <https://CRAN.R-project.org/package=drat>

</div>

</div>
