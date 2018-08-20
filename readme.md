# AJP template for LaTeX
Updates to the template for manuscripts for the [American Journal of Physics](https://aapt.scitation.org/journal/ajp) to use BibTeX and include hyperlinks, by Ted Corcovilos (2014).  Also, includes configuration file for `latexmk` to simplify compiling the document and a working `.gitignore` configuration.

## Usage

1. Edit AJPTemplate.tex with the text of your document.
2. Edit AJPTemplate.bib to contain BibTeX bibliography entries for the reference of your text.
3. (Optional) Place figures in the `fig` folder to preserve them during cleanup.
4. Compile the document with one of these methods:
    * Manually: run `pdflatex AJPTemplate`, followed by `bibtex AJPTemplate`, then two more times `pdflatex AJPTemplate`.
    * Automagically: run `latexmk AJPTemplate` (requires `latexmk` to be installed).
5. When ready to submit the manuscript, manually copy the contents of the `AJPTemplate.bbl` file into the place indicated near the end of the `AJPTemplate.tex` file.  Then compile again by running `pdflatex AJPTemplate` (probably 3 times) or `latexmk AJPTemplate`.  (This final step is a work-around for the submission instructions for AJP: `.bbl` files are not permitted.)