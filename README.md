# README.md

This repository contains a Quarto project that is the website for SIPBS Internships and Internship Matching, at the University of Strathclyde.

- [live site](https://sipbs-compbiol.github.io/sipbs-internships/)

## Organisation

In Quarto, `.qmd` files are processed to render a static site. Here, most pages are written as top-level `.qmd` files, but the projects on offer in each year are written as `.qmd` files in the `projects` subdirectory (this is picked up by the `previous_projects.qmd` top-level page as a listing). Organising project lists in this way makes it easier to manage the site year-on-year.

Several reused pieces of text and other information are defined as variables in the `_variables.yml` file. This makes it easier to update the site year-on-year.

The `_quarto.yml` file defines configuration options, including theme and the top-level menu bar.

The `index.qmd` file is the landing page for the site.

Images and other assets are placed under the `assets` subdirectory.

The `_extensions` and `_freeze` subdirectories are included in the repo for functional reasons.

## Rendering the site

This Quarto website renders to the `_site` subdirectory. This subdirectory is excluded from the repository by the `.gitignore` file. This is done because the live site is build using a GitHub action that builds the site on each push to the `main` branch.

The GitHub action that publishes the site at GitHub Pages is `.github/workflows/publish.yml`.

Local rendering can be done through `RStudio` (Render button in the editor), or at the command-line with 

``` bash
quarto render
```