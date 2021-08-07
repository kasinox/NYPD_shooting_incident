# NYPD_shooting_incident

## Video showing the knitting done correctly in macOS

* http://youtu.be/rdbo0caUAZw?hd=1

## Video showing a fresh install of Rstudio in windows and going through the knitting

<iframe width="560" height="315" src="https://www.youtube.com/embed/ynpqcxFjM0A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

* Rstudio will prompt to install the required packages, click yes
* If the file doesn't knit the first time, the prompt will show there is no pdf - latex output library, it recommend tinytex so that's what I've included in the library.
* you will need to manually install tinytex, the script doesn't automatically install tinytex
* in the console of Rstudio, type the following to install tinytex, then the rest should be fine
* tinytex::install_tinytex()

## Knitting in windows environment have no problem so far as there is more support.

* download all the files for knitting the RMD, as there are dependence on the files stored in the folders

if you have any questions about the instructions, please email me at chenning.xu@colorado.edu
 
## Warning, Knitting the document in MacOS will have issues due to version compatiblity issue between R and the sf library

* "SF" package is essential for geospatial mapping in R, somehow the support in MacOs lag behind that of windows, I would not recommend knitting this in macOS. I got it to work in windows first, then took me another 4-5 hours to figure out the package dependencies and knit it in macOS.

* MacOS would not load the sf lib correctly in Rstudio and one would need to first go to terminal and install homebrew.

## mac knitting instruction

*  install brew
*  https://brew.sh/
* type the following in terminal to install homebrew
* /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"


## install missing libraries

full instruction from this website to install https://r-spatial.github.io/sf/

for example, sf library cannot be installed correctly in the most recent macos update, after install homebrew, type the following in the terminal

* brew install pkg-config 
* brew install gdal

Once gdal is installed, you will be able to install sf package from source in R. With the current version of proj (7.0.0) on homebrew, installation requires additional configuration:

install.packages("sf", configure.args = "--with-proj-lib=/usr/local/lib/")

if the console prompt any missing component that could not be installed correctly, install it in either Rstudio or brew and knit it again


