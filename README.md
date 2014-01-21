# Introduction

I created source files for three documents, for a proper academic paper, for an essay and for a presentation slides.

You can see the source and output RAW-FILES thru the listing above. 

To see them *rendered* click the links from below:

- [essay_galigula.html](https://rawgithub.com/digieast/paperx/master/essay_galigula.html)
- [theory_paper.pdf](https://rawgithub.com/digieast/paperx/master/theory_paper.pdf)
- [slides.html](https://rawgithub.com/digieast/paperx/master/slides.html)

## Processing the source files

Each source file has a short command in within tags `<!--` and `-->` that converts the source code into html/pdf. To be able to run the commands you need to have **pandoc** and **latex** installed. Follow these directions:

- [Installing Pandoc](http://johnmacfarlane.net/pandoc/installing.html)  - duration of download and install approx. 30s.
- [Latex:in asentaminen linuxiin, Mac OS X:ään ja Windowsiin](http://www.latex-project.org/ftp.html) - duration of download and install approx. 60 min.

### Commands

**This has been tested in using pandoc 1.12.3 version in Windows 7 and Ubuntu linux 12.04**

Use following scripts to convert slides into desired format

For converting the **theory_paper.md**

- **pdf**: `pandoc --filter pandoc-citeproc theory_paper.md -o theory_paper.pdf --toc --number-sections`
- **docx**: `pandoc --filter pandoc-citeproc theory_paper.md -o theory_paper.docx --toc --number-sections`

For converting the **slides.md**

- **reveal.js html**: `pandoc -t revealjs -s slides.md -o slides.html -V revealjs-url=http://lab.hakim.se/reveal-js -V theme=simple -V transition=fade`
- **pdf**: `pandoc -t beamer slides.md -o slides.pdf`

For converting the **essay_galigula.md**

- **html**: `pandoc -s essay_galigula.md -o essay_galigula.html`

# Writing apps for Markdown

And of course, you need an application for writing text. **Notepad** is good, but for windows I recommend [Markdown Pad](http://markdownpad.com/) and for OS X maybe [Mou](http://mouapp.com/), [Clockwork Engine](http://clockworkengine.com/lightpaper-mac/) or perhaps [TEXTS](http://www.texts.io/).  

