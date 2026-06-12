# JTH Report Template

Quarto + LaTeX template for lab reports at Jönköping University, School of Engineering.
Swedish title page ("Labbrapport"), custom JTH cover, bibliography, figure handling, and code cells preconfigured.

## How to use it

This repository is intended to be used as a **read-only reference**.
Copy it, then edit the copy — do not edit the files in `~/templates/jth-report/` directly.

```bash
cp -r ~/templates/jth-report ~/my-lab-1
cd ~/my-lab-1
quarto render report.ipynb --to pdf
```

To update your local copy of the template with the latest version:

```bash
update-templates
```

## What's inside

- `report.ipynb` — the notebook template, with sections, figures, equations, citations
- `titlepage.tex` — custom Swedish title page, included via Quarto YAML
- `library.bib` — example bibliography
- `graphics/` — JTH school logo and example figures

## Source

The original template is published at
<https://python.ju.se/ProgrammingFundamentals/writing_documentation.html#report-template-swedish>.

This repo tracks that template for installation on JupyterHub (`jupyter.ju.se`) and elsewhere.
