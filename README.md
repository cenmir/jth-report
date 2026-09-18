# JTH Report Template

Quarto + LaTeX template for lab reports at Jönköping University, School of Engineering.
Custom JTH cover, bibliography, figure handling, and code cells preconfigured.

It comes in two languages, one folder each:

| Folder | Language | Title page |
|---|---|---|
| [`sv/`](sv/) | Swedish | "Labbrapport" |
| [`en/`](en/) | English | "Lab report" |

The two folders are complete and independent: pick one, copy it, and everything
the template needs is in your copy.

**Example output:** [`sv/JTH-Report-Template.pdf`](sv/JTH-Report-Template.pdf) and
[`en/JTH-Report-Template.pdf`](en/JTH-Report-Template.pdf), what `report.ipynb`
looks like rendered.

## How to use it

This repository is intended to be used as a **read-only reference**.
Copy it, then edit the copy. Do not edit the files in `~/templates/jth-report/` directly.

```bash
cp -r ~/templates/jth-report/en ~/my-lab-1     # or sv
cd ~/my-lab-1
quarto render report.ipynb --to pdf
```

**On jupyter.ju.se:** use the **New lab report (English)** or **New lab report
(svenska)** card in the Launcher, which makes the copy for you and opens it.
Then click **PDF** in the toolbar (or menu **Quarto**). The PDF appears next to
the file. Don't use *File > Save and Export Notebook As > PDF*, it doesn't use
Quarto or this template.

To update your local copy of the template with the latest version:

```bash
update-templates
```

## What's inside each language folder

- `report.ipynb` the notebook template for **PDF**, with sections, figures, equations, citations
- `report-html.ipynb` the **HTML** variant: one self-contained file, with worked examples of
  animations (GIF, MP4, interactive player), interactive Plotly graphs, audio, tabsets and
  foldable code. Render it with **Render to html using Quarto**.
- `JTH-Report-Template.pdf` the rendered template (regenerate:
  `quarto render report.ipynb --to pdf --execute --output JTH-Report-Template.pdf`)
- `titlepage.tex` the custom title page, included via Quarto YAML
- `library.bib` example bibliography
- `graphics/` JTH school logo and example figures

Keeping the two in step: when you change something in one language, make the
same change in the other, or the folders drift apart.

## Source

The original template is published at
<https://python.ju.se/ProgrammingFundamentals/writing_documentation.html#report-template-swedish>.

This repo tracks that template for installation on JupyterHub (`jupyter.ju.se`) and elsewhere.
