updating the R habitat
================

![](../resources/p003-header.jpg) <small> <br> <i>Habitat</i> by Kylie
Jaxxon is licensed under
<a href="https://creativecommons.org/licenses/by-sa/2.0/legalcode">CC
BY-SA 2.0</a> <br> </small>

If you already have R and RStudio installed, please update to the most
recent releases and update your R packages as well.

-   Running old software can be considerably harder than running new
    software.
-   Get current at the start of a new project, but avoid updating if you
    are approaching a project deadline.
-   Read more about it at
    <a href="https://whattheyforgot.org/maintaining-r.html" target="_blank">Maintaining R</a>,
    a chapter in (Bryan and Hester, [2019](#ref-Bryan+Hester:2019)).

## update R

To determine the most recent version of R, navigate to the R website
[(link)](https://www.r-project.org). To see the version of R on your
local machine, run the following line in the console,

``` r
R.version
```

You should see an output something like,

    ##                _                           
    ## platform       x86_64-w64-mingw32          
    ## arch           x86_64                      
    ## os             mingw32                     
    ## system         x86_64, mingw32             
    ## status                                     
    ## major          4                           
    ## minor          1.0                         
    ## year           2021                        
    ## month          05                          
    ## day            18                          
    ## svn rev        80317                       
    ## language       R                           
    ## version.string R version 4.1.0 (2021-05-18)
    ## nickname       Camp Pontanezen

To update, install the installr package using the RStudio *Packages &gt;
Install*, and type `installr` in the dialog box or you can just type
`install.packages("installr")` in the console.

> Note. For some users the following guidelines work only by logging as
> an administrator.

Next (on a Windows machine) we update R using the R GUI

-   Close RStudio
-   Navigate to your most recent `Rgui.exe` file located in your
    Programs directory, e.g.,
    `C:\Program Files\R\R-4.0.5\bin\x64\Rgui.exe`  
-   Run `Rgui.exe`

In the window that appears, run the commands

    library("installr")
    updateR()

OK all defaults with one possible exception. If you have designated a
directory for R packages (for example, I store all my R packages in a
`C:/R/library` directory) then answer “no” to the library questions in
the R update.

## update RStudio

Check for updates from the RStudio menu *Help &gt; Check for Updates*.

If *Check for Updates* does not appear in the menu,

-   Find the current version of RStudio from the menu *Help &gt; About
    RStudio*  
-   Navigate to the
    <a href="https://www.rstudio.com/products/rstudio/#Desktop" target="_blank">RStudio website</a>,
    find out what the current version is.

If you decide to update RStudio, close RStudio on your machine, download
the new version, and run the `RStudio-n.n.n.exe` as an administrator
(`n.n.n` is the current version number).

## update R packages

**Update CRAN packages**

-   From the RStudio pane, Select *Packages &gt; Update*
-   OR, from the menu, *Tools &gt; Check for Package updates …*

When updating packages, if a window pops up asking about compilation,

<img src="../resources/cm904-01.png" width="40%" />

-   NO saves time
-   YES gets you the latest version but can be time-consuming. Don’t say
    yes if you are in a hurry to get some work done.

**Update without permission prompts**

Run

``` r
update.packages(ask = FALSE)
```

**Update and include packages in GitHub repositories**

Install the remotes package. Then run,

``` r
remotes::update_packages()
```

------------------------------------------------------------------------

<a href="#top">▲ top of page</a>  
[◁ main page](../README.md)
