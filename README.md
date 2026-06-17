# Current Findings

This repository contains the source files for the Current Findings website.

Website:

https://robertslab.github.io/current-findings/

Source repository:

https://github.com/RobertsLab/current-findings

## Purpose

Current Findings hosts open, non-peer-reviewed scientific reports, technical notes, exploratory analyses, field reports, dataset notes, and working manuscripts from Roberts Lab.

The goal is to make small but useful scientific efforts visible, reusable, and citable.

## Adding a new report

Create a new report from the helper script:

```bash
./new-report.sh report-slug
```

Example:

```bash
./new-report.sh vibrio-eelgrass-mussels
```

This creates:

```text
reports/vibrio-eelgrass-mussels/
├── index.qmd
├── references.bib
└── figures/
```

Edit `index.qmd` to add the report content.

## Manual report creation

You can also create a report manually:

```bash
mkdir -p reports/vibrio-eelgrass-mussels/figures
touch reports/vibrio-eelgrass-mussels/index.qmd
touch reports/vibrio-eelgrass-mussels/references.bib
```

Use `templates/report-template.qmd` as the starting structure.

## Render the site

```bash
quarto render
```

## Preview locally

```bash
quarto preview
```

## Commit and push

```bash
git add .
git commit -m "Add new report"
git push
```

## Report status

Unless explicitly stated, reports are not peer reviewed.

## GitHub Pages setup

In the GitHub repository:

1. Go to Settings.
2. Go to Pages.
3. Under Build and deployment, choose "Deploy from a branch."
4. Choose branch `main`.
5. Choose folder `/docs`.
6. Save.

The site should then be available at:

https://robertslab.github.io/current-findings/

## Repository structure

```text
current-findings/
├── _quarto.yml
├── index.qmd
├── reports.qmd
├── about.qmd
├── styles.css
├── README.md
├── new-report.sh
├── reports/
├── templates/
└── docs/
```
