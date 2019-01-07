Welcome to the Module Data Collection, Data Storage, Data Management.

## To-Do list first day
1. Create a Github account and join the students team of the `data-hydenv` (see invitation link per e-mail).
2. Enroll with course password on Moodle (http://www.lehre-hydro.uni-freiburg.de).
3. Prepare your computer with software (e.g. R Studio) and ensure that you are able to install and load packages. Be sure that you know the main features of R Studio App (console, load/save scripts, getting help, `View()`, Main preferences, Connection to CRAn server)
4. Install following packages: 
    - `tidyverse`, 
    - `lubridate`,
    - `skim`
    - `padr`
    - `rio` 
    - `zoo`
    - `sf` 
    - other packages will follow...
5. Use your HOBO measurement protocol and go to the _HOBO Meta table_ and insert your HOBO meta information there.
6. Go to https://rmarkdown.rstudio.com/authoring_quick_tour.html and make sure that your R Studio is "R Markdown"-ready. Check if you are able to `knitr` a R Markdown file (HTML, PDF).
7. Read the HOBO Manual (Download PDF above) to learn how the sensor/logger works (i.e. precision, uncertainty, ranges).

## Important Links

- Moodle http://www.lehre-hydro.uni-freiburg.de
- HOBO Meta table https://tinyurl.com/hobometa2019
- Exercises: https://data-hydenv.github.io/exercises/ (Webpage with all Exercises)

## System requirements

### For the time series data analysis part following software/resources are needed:

- R Studio (with Internet access)
- An up-to-date R Version (must not be the latest version)
- Texteditor (normal TextEdit is enough, but you can look for more advanced editors)
- MS Excel (helpful) or comparable software
- MS Word or word processor (to write report) or comparable software
- Internet access is really important (eduroam Wi-Fi).

### For the (Geo)-databases part the following software is needed:

- QGIS 3.x (or QGIS 2.14/2.18 if you have experienced problems with version 3.x).
- pgAdmin 3

QGIS (https://qgis.org/de/site/forusers/download.html). QGIS is available for Windows, Mac and Linux.

On top you will need a software for managing PostgreSQL database servers. There are two options:
pgAdminIII (Caution: not pgAmin4!!!!). For Windows/Mac: https://www.pgadmin.org/download/ ; Linux userswill find pgAdminIII in the software repositories of Debian, Ubuntu, CentOS/Redhat/Fedora and OpenSuse, always called 'pgadmin3'

__DataGrip__: This is the preferred software, but it is a proprietary chargeable software. For students it is free, in case you register using a university mail adress. DataGrip is available for Windows, Mac and Linux. 
DataGrip is way more powerful than pgAdmin, but not open Source. You can accomplish the lecture with both products.


## Install packages in R

Normally the CRAN server is used to install `install.packages("a_package_name")` from the console. Packages are then loaded with `library(a_package_name)`. Check for error- or warning-messages in the console.

If you want to install a pre-release of a package or a package that is not supported by CRAN but available on Github you use `devtools`. The command is a combination of github account (here: `r-lib`) and name of the package/repository (here: `devtools`). 

```{r}
install.packages("devtools")
devtools::install_github("r-lib/devtools")
```



