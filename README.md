# TechReport Template

This repo contains a template for building technical reports using LaTeX.

To use this template, first click the green "Use this template" button at the top of this page to create a copy of this repo in your own GitHub account.   You might want to rename this repo from "techreport" to a name indicating the project, such as "diversity-in-cs-proposal".

Next, install [TexLive](https://www.tug.org/texlive/). If you are on a Mac, install [MacTex](https://www.tug.org/mactex/).

Finally, clone this repo to your laptop, cd into the repo directory, and type "make" to ensure that everything is installed correctly and that you can create a copy of the template pdf file. For example:

```
[~/github/radgrad/techreport]-> make
= techreport.tex --> techreport.d techreport.dvi (1) =
Files techreport.toc and techreport.toc.make differ
=  techreport.aux --> techreport.bbl =
= techreport.tex --> techreport.dvi (2) =
= techreport.tex --> techreport.dvi (3) =
= techreport.tex --> techreport.dvi (4) =
= techreport.tex --> techreport.dvi (5) =
Success!  Wrote 4 pages, 17248 bytes
= techreport.dvi --> techreport.ps =
= techreport.ps --> techreport.pdf =
rm techreport.paper.make techreport.embed.make
[~/github/radgrad/techreport]-> make clean
[~/github/radgrad/techreport]-> make
NOTE: You may ignore warnings about the following files:

     techreport.d

Makefile:1528: techreport.d: No such file or directory
= techreport.tex --> techreport.d techreport.dvi (1) =
= techreport.bib techreport.aux --> techreport.bbl =
= techreport.tex --> techreport.dvi (2) =
= techreport.tex --> techreport.dvi (3) =
= techreport.tex --> techreport.dvi (4) =
= techreport.tex --> techreport.dvi (5) =
Success!  Wrote 4 pages, 17248 bytes
= techreport.dvi --> techreport.ps =
= techreport.ps --> techreport.pdf =
rm techreport.paper.make techreport.embed.make
[~/github/radgrad/techreport]->
```

Now you should be able to view the techreport.pdf file.  This document contains further information about how to design and implement your techreport. It also includes examples of the most common LaTex formatting commands---make words italicized, enumerated lists, figures, tables, sections, citations, etc.

To actually make your techreport, I recommend that you make an IntelliJ project for this repo, then edit the text there. I generally do not install the tex extensions for IntelliJ, but you can try them if you want.

Note that the PDF file is not committed to the repo.  This makes it easier for multiple people to collaborate on a single project without getting merge errors.
