# Template for reproducible manuscripts using Quarto

A template for reproducible manuscripts using [Quarto](https://quarto.org/). It provides some infra that I commonly use in my projects, including

- an RStudio [Project](https://support.posit.co/hc/en-us/articles/200526207-Using-RStudio-Projects) 
  - With sensible defaults like never saving the workspace
- [renv](https://rstudio.github.io/renv/index.html)
  - For ensuring a reproducible R environment
- a [Makefile](https://www.gnu.org/software/make/)
  - Clear instructions on building the project; simply run `make` in terminal
  - I do not use Docker, so system requirements are up to the user
- [quarto-preprint](https://github.com/mvuorre/quarto-preprint/) extension
  - Quarto output formats
- a starter Quarto markdown file (`index.qmd`) with some commonly used code snippets
  - Refers to an `.Renviron` that by default has environment variables suitable for my computer
  - knitr chunk options, ggplot2 theme

## Install

Click "Use this template" on [GitHub](https://github.com/mvuorre/quarto-preprint-template).

## Use

After "installing" the template, modify contents to your liking. This probably includes rewriting README.md, modifying .Renviron, writing your content in index.qmd, changing LICENSE, and editing _quarto.yml.

After adding your content, "publish" your work:

1. Run `make`
   1. `make clean` to remove intermediates and start from a clean slate
   2. `make clean-hard` to additionally remove cache/, which typically includes estimated models and results from other time-consuming computations
2. Add, commit, and push desired files to GitHub
   1. Don't forget to make use of .gitignore
3. Make the GitHub repo public
4. Configure GitHub pages to display content from docs/ in the main branch
5. Connect your OSF project to the GitHub repo
6. Create a registration on OSF to archive the GitHub repo on OSF

There will also be occasional updates to [quarto-preprint](https://github.com/mvuorre/quarto-preprint/). To get those, run `quarto update extension mvuorre/quarto-preprint`.
