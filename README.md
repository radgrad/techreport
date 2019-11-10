# TechReport Template

This repo contains a template for building technical reports using LaTeX.

### Setup

To use this template, first click the green "Use this template" button at the top of this page to create a copy of this repo in your own GitHub account.   You might want to rename this repo from "techreport" to a name indicating the project, such as "diversity-in-cs-proposal".

Next, install [TexLive](https://www.tug.org/texlive/). If you are on a Mac, install [MacTex](https://www.tug.org/mactex/).

Finally, clone your new repo to your laptop.

### Building your first PDF (Mac, Linux)

To build the techreport.pdf file on a Mac or Linux box, just type "make". For example:

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
### Building your first PDF (Windows)

Since make files don't work by default on Windows, you need to invoke the following LaTeX programs manually:

```
> pdflatex techreport.tex
> bibtex techreport
> pdflatex techreport.tex
```

The first invocation of pdflatex creates a number of intermediate files providing information about the structure of the document which are then used by a second invocation of pdflatex to generate the table of contents. There is a separate program, bibtex, which is used to generate the bibliography section.  So, in all, you need to run these three commands in sequence to generate the document from scratch. (If the bibliography hasn't changed, then you don't have to run bibtex each time.)

For more information, you can see the [Testing the installation section of TexLive](https://www.tug.org/texlive/doc/texlive-en/texlive-en.html#x1-380003.5).

### Developing your tech report

There are only two files you need to edit from this template to create your tech report:

  1. techreport.tex.  This file contains the text of your tech report.
  2. techreport.bib.  This file contains the references that you cite in your techreport, and is used by LaTeX to construct the bibliography section.

The techreport.pdf document contains further information about how to design and implement your techreport. It also includes examples of the most common LaTex formatting commands---make words italicized, enumerated lists, figures, tables, sections, citations, etc. Don't worry about writing over this file, you can always refer to the original source file [here](https://raw.githubusercontent.com/radgrad/techreport/master/techreport.tex).

To actually make your techreport, I recommend that you make an IntelliJ project for this repo, then edit the text there. I generally do not install the tex extensions for IntelliJ, but you can try them if you want.

Whatever editor you use, be sure it provides a spelling checker!

Note that the PDF file is not committed to the repo.  This makes it easier for multiple people to collaborate on a single project without getting merge errors.

### Avoid the GUIs

There are a number of GUI and cloud-based tools for TeX and LaTeX that you will find via Google. You might be tempted to think these will make your life easier. Please avoid them for now and just use a regular editor and the command line.  For the simple documents you are creating, I believe this template and the command line will get you to the finished report the fastest, and allow others to help you author the document and debug issues the easiest.
