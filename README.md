# ConTeXt Résumé
My résumé as of early 2016, designed and rendered with ConText.

ConTeXt is a general-purpose document processor. It is especially suited for structured documents, automated document production, very fine typography, and multi-lingual typesetting. It is based in part on the TeX typesetting system, and uses a document markup language for manuscript preparation. The typographical and automated capabilities of ConTeXt are extensive, including interfaces for handling microtypography, multiple footnotes and footnote classes, and manipulating OpenType fonts and features. Moreover, it offers extensive support for colors, backgrounds, hyperlinks, presentations, figure-text integration, and conditional compilation. It gives the user extensive control over formatting while making it easy to create new layouts and styles without learning the low-level TeX macro language.

For more information please see the wonderful ConTeXt wiki here: http://wiki.contextgarden.net/Main_Page

to build: 

    context_directory=ConTeXt

    mkdir "$context_directory"
    (cd $_
      rsync -av rsync://contextgarden.net/minimals/setup/first-setup.sh .
      sh ./first-setup.sh --modules=all --engine=luatex
    )

    . "$context_directory"/tex/setuptex
    context resume.tex
