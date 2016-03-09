# report

# Recomended texlive installation

## Ubuntu 12.04 (Precise)

Add the texlive-backports PPA and update the repositories:

```
$ sudo add-apt-repository ppa:texlive-backports/ppa
$ sudo apt-get update
``` 

Install texlive and required packages:

```
$ sudo apt-get install biblatex texlive texlive-humanities texlive-latex-extra texlive-publishers texlive-science
``` 

## Ubuntu 14.04 (Trusty)

Install texlive and required packages:

```
$ sudo apt-get install biber texlive texlive-bibtex-extra texlive-humanities texlive-latex-extra texlive-publishers texlive-science
``` 

# Compilation

Use `scons` to compile. First install it:
```
$ sudo apt-get install scons
``` 

You can build the pdf simply by running from the parent directory (e.g. `~/git/report`) this command:
```
$ scons -Q && scons -c
``` 
