msni
====

MathSciNetImport: import metadata (and article) via MathSciNet to a file-based library


Why
---

Bibliography reference managers *could* be awesome if not for the
tremendous bloat (Oracle JVM? Srsly?). Using software like RefTeX,
most features of bibliography reference managers *might* be
superfluous in a number of cases. msni is a tiny hack closing an
annoying gap: the process of importing articles from the MathSciNet.

Workflow
--------

1. Find your favourite article on the MathSciNet, e.g. Tate's [The
   arithmetic of elliptic
   curves](http://www.ams.org/mathscinet-getitem?mr=419359).
1. Find the number of the review, in our case **MR0419359**.
1. Execute `msni MR0419359`.
1. A browser opens. Follow the MathSciNet links until you can download
   a PDF file. Just click *Save* (don't bother with *Save As*) and
   close the browser.
1. A terminal will start up in the directory
   `~/bib/msni/Tate-TheArithmeticOfEllipticCurves`. `ls` will reveal a
   file `MR0419359.bib` containing the BibTeX information pulled from
   MathSciNet and a file called `art%3A10.1007%2FBF01389745.pdf`
   containing the article.

Why is that a good workflow?
----------------------------

In general there should be almost no need to keep more metadata at
hand, the MathSciNet provides great options for searching articles and
there is no need to replicate that. Articles show up in `locate` if
you search for author, title or review number.

Dependencies
------------

- midori
- bibtex-ruby
