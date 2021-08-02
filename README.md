# NYPD_shooting_incident
 
Warning, Knitting the document in MacOS will have issues due to version compatiblity issue 
for some of the librarys, macOS would not download them correctly in Rstudio and one would need to first go to terminal and install homebrew 

## mac knitting instruction

*  install brew
  https://brew.sh/

* type the following in terminal to install homebrew
* /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

## install missing libraries
* for example, sf library cannot be installed correctly in the most recent macos update, after install homebrew, type the following in the terminal
** brew install lwgeom
** brew install sf
** brew install tmap

** if the console prompt any missing component that could not be installed correctly, install it in brew and knit it again
** sf package is essential for geospatial mapping in R, somehow the support in MacOs lag behind that of windows

** Knitting in windows environment have no problem so far as there is more support.