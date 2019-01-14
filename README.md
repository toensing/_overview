Welcome to the Module Data Collection, Data Storage, Data Management.

## To-Do list first day
1. Create a Github account and join the students team of the `data-hydenv` (see invitation link per e-mail).
2. Enroll with course password on Moodle (http://www.lehre-hydro.uni-freiburg.de).
3. Prepare your computer with software (e.g. R Studio) and ensure that you are able to install and load packages. Be sure that you know the main features of R Studio App (console, load/save scripts, getting help, `View()`, Main preferences, Connection to CRAn server)
4. Install following packages: 
    - `tidyverse`, `lubridate`, `zoo`, `sf`,
    - `skimr`, `padr` (might be helpful),
    - `RPostgreSQL` (see details below),
    - see also R Markdown section below.
5. Use your HOBO measurement protocol and go to the _HOBO Meta table_ and insert your HOBO meta information there. Double check your Lon/Lat information (in decimal number) if really the correct location is described.
6. Check the HOBO Manual (Download PDF above) to learn how the sensor/logger works (i.e. precision, uncertainty, ranges).

## Important Links

- Moodle http://www.lehre-hydro.uni-freiburg.de
- HOBO Meta table https://tinyurl.com/hobometa2019
- Exercises: https://data-hydenv.github.io/exercises/ (Webpage with all Exercises and Code snippets)
- Visit the Course Resources section https://github.com/data-hydenv/cheatsheets_resources

## System requirements

### For the time series data analysis part following software/resources are needed:

- R Studio (with Internet access)
- An up-to-date R Version (must not be the latest version)
- Texteditor (normal TextEdit is enough, but you can look for more advanced editors)
- MS Excel (helpful) or comparable software
- MS Word or word processor (to write report) or comparable software
- Internet access is really important (eduroam Wi-Fi).

### For the (Geo)-databases part the following software is needed:

- QGIS 3.x. **It is highly recommended to use QGis 3.4**, as this version is used for demonstration. In case you use any 2.x, it has to be > 2.12 and note that the software changed substantially from version 2 to 3. Examples during class might work different in version 2.x. However, QGis >2.12 and 3.x are all technically capable of solving the tasks.  
QGIS download: https://qgis.org/de/site/forusers/download.html. QGIS is available for Windows, Mac and Linux.

On top you will need a software for managing PostgreSQL database servers. There are two options:
- **pgAdmin3**: 
  pgAdminIII (Caution: not pgAmin4!!!!). For Windows/Mac: https://www.pgadmin.org/download/ ; Linux users will find             pgAdminIII in the software repositories of Debian, Ubuntu, CentOS/Redhat/Fedora and OpenSuse, always called 'pgadmin3'

- **DataGrip**: This is the preferred software, but it is a proprietary chargeable software. For students it is free, in case   you register using a university mail adress. DataGrip is available for Windows, Mac and Linux. 
  DataGrip is way more powerful than pgAdmin, but not open Source. **You can accomplish the lecture with both products**.

You can install either of both, or both products.

Finally, a R package is needed:

- `RPostgreSQL`, make sure that the R package RPostgreSQL is installed and can be imported. Linux users might have to         additionally install the package *postgresql-server-10-dev* to make RPostgreSQL work properly as R fails to install all       dependencies in some circumstances.

- other useful packages beside `sf` for spatial data analysis in R: `leaflet`, `mapview`, `ggmap`, `tmap`, `raster`

## Install packages in R

Normally the CRAN server is used to install `install.packages("a_package_name")` from the console. Packages are then loaded with `library(a_package_name)`. Check for error- or warning-messages in the console.

If you want to install a pre-release of a package or a package that is not supported by CRAN but available on Github you use `devtools`. The command is a combination of github account (here: `r-lib`) and name of the package/repository (here: `devtools`). 

```{R}
install.packages("devtools")
devtools::install_github("r-lib/devtools")
```

A third possibility is to use the dialog _Install packages_ in the _Tools_ menu in R Studio. To get an overview on your R session and the attached packages use:

```{R}
search()
sessionInfo()
```

If an older version of a package is needed you can often download archived version from the package homepage (search for package name + CRAN). Archives can be installed with:

```{R}
install.packages("http://cran.r-project.org/src/contrib/Archive/RNetLogo/RNetLogo_0.9-6.tar.gz", repo=NULL, type="source")
install.packages("C:\\Downloads\RNetLogo_0.9-6.tar.gz", repos = NULL, type="source")
```

## R Markdown ready?

Install the packages `rmarkdown` and `radix` in R Studio. Go to https://rmarkdown.rstudio.com/authoring_quick_tour.html and make sure that your R Studio is "R Markdown"-ready. Check if you are able to `knitr` a R Markdown file (HTML, PDF).
 - Go To _New File_ in R Studio and select _R Markdown_. There you can choose a new _Radix Article_ from the _Template_menu. An example file is loaded. Save it and try to `Knit` it into HTML or PDF. The `radix` package offers R Markdown files with scientific features.



## R for Data Science

Book: R for Data Science (Wickham & Grolemund) https://r4ds.had.co.nz/

<img src="https://d33wubrfki0l68.cloudfront.net/b88ef926a004b0fce72b2526b0b5c4413666a4cb/24a30/cover.png" width="200">

