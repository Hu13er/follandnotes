# Notes on Real Analysis G. B. Folland

## Book Template

This text uses Latex template of book [A Programmer's Introduction to Mathematics](https://pimbook.org).

## Compiling

Compile with `latexmk book.tex` using the following `.latexmkrc`

```
$pdf_mode = 1;
$postscript_mode = 0;
$dvi_mode = 0;
$pdflatex = 'xelatex -interaction=nonstopmode';
$pdf_previewer = "open -a /Applications/Skim.app";
$clean_ext = "paux lox pdfsync out";
```

## File structure

```
.
├── about.tex
├── book.tex
├── chapters
│   ├── chapter_template.tex
│   ├── measures.tex
│   └── ...
├── copyright.tex
├── structure.tex
└── titlepage.tex
```

`book.tex` is the main entry point that includes the book templating files,
front/end matter, and the individual sources from each chapter. When creating
a new chapter, add a new file to `chapters` and add it to the `includeonly`
and `input` sections of `book.tex`.

`structure.tex` contains the main work of setting up formatting and style,
including margins and page size, code listings, theorem environments, etc.

The remaining files should be self-explanatory.
