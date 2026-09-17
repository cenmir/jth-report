# JTH Report Template

Quarto + LaTeX template for lab reports at Jönköping University, School of Engineering.
Swedish title page ("Labbrapport"), custom JTH cover, bibliography, figure handling, and code cells preconfigured.

**Example output:** [`JTH-Report-Template.pdf`](JTH-Report-Template.pdf) — what `report.ipynb` looks like rendered.

## How to use it

This repository is intended to be used as a **read-only reference**.
Copy it, then edit the copy — do not edit the files in `~/templates/jth-report/` directly.

```bash
cp -r ~/templates/jth-report ~/my-lab-1
cd ~/my-lab-1
quarto render report.ipynb --to pdf
```

**On jupyter.ju.se:** open `report.ipynb` in your copy and click **Render with Quarto** in the
toolbar (or menu **Quarto → Render with Quarto (PDF)**). The PDF appears next to the file.
Don't use *File → Save and Export Notebook As → PDF* — it doesn't use Quarto or this template.

To update your local copy of the template with the latest version:

```bash
update-templates
```

## What's inside

- `report.ipynb` — the notebook template for **PDF**, with sections, figures, equations, citations
- `report-html.ipynb` — the **HTML** variant: one self-contained file, with worked examples of
  animations (GIF, MP4, interactive player), interactive Plotly graphs, audio, tabsets and
  foldable code. Render it with **Render to html using Quarto**.
- `JTH-Report-Template.pdf` — the rendered template (regenerate: `quarto render report.ipynb --to pdf --output JTH-Report-Template.pdf`)
- `titlepage.tex` — custom Swedish title page, included via Quarto YAML
- `library.bib` — example bibliography
- `graphics/` — JTH school logo and example figures

## Source

The original template is published at
<https://python.ju.se/ProgrammingFundamentals/writing_documentation.html#report-template-swedish>.

This repo tracks that template for installation on JupyterHub (`jupyter.ju.se`) and elsewhere.
