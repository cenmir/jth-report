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

## On jupyter.ju.se

Nothing to install and no terminal needed. Python, Jupyter, Quarto and LaTeX
are already there, and this template is already in your account.

1. Sign in at [jupyter.ju.se](https://jupyter.ju.se).
2. On the start page (the **Launcher**, opened with the **+** button above the
   file browser) look under **JTH templates** and click **New lab report
   (English)** or **Ny labbrapport (svenska)**. Your own copy is created
   (`lab1`, `lab2`, … one per lab) and opened for you.
3. Write in `report.ipynb`: text and equations in markdown cells, figures from
   code cells.
4. Click **PDF** in the toolbar. The same choices are in the **Quarto** menu,
   and right-clicking the file in the file browser renders it to PDF. A panel
   opens and shows the progress; when it says `Output created: report.pdf`, the
   PDF is next to your file. The first render can take a minute while LaTeX
   packages are installed, later ones take seconds.
5. **HTML** does the same for `report-html.ipynb`, and **Preview** opens a live
   preview in a browser tab that updates every time you save. Stop it with
   **Quarto → Stop the preview**.

Two things to avoid: do not work inside `~/templates/jth-report`, which is a
read-only reference that is updated for you, and do not use *File > Save and
Export Notebook As > PDF*, which ignores this template.

The copy in `~/templates` is refreshed automatically. To pull the latest
version yourself, open a terminal and run `update-templates`.

## On your own computer

You need [Quarto](https://quarto.org/docs/get-started/), Python with Jupyter,
and a LaTeX distribution (`quarto install tinytex` is the small option). Then
copy a language folder out of this repository and render it:

```bash
cp -r en ~/my-lab-1     # or sv
cd ~/my-lab-1
quarto render report.ipynb --to pdf
```

Copy the folder first and edit the copy; treat the repository itself as a
read-only reference.

## What's inside each language folder

- `report.ipynb` the notebook template for **PDF**, with sections, figures, equations, citations
- `report-html.ipynb` the **HTML** variant: one self-contained file, with worked examples of
  animations (GIF, MP4, interactive player), interactive Plotly graphs, audio, tabsets and
  foldable code. Render it with **Render to html using Quarto**.
- `JTH-Report-Template.pdf` the rendered template (regenerate:
  `quarto render report.ipynb --to pdf --execute --output JTH-Report-Template.pdf`)
- `titlepage.tex` the custom title page, included via Quarto YAML
- `library.bib` example bibliography
- `ieee.csl`, `apa-7th.csl` citation styles; IEEE is the default, and the `csl:` line in the
  YAML block switches to APA (same files and wording as jth-thesis)
- `graphics/` JTH school logo and example figures

Keeping the two in step: when you change something in one language, make the
same change in the other, or the folders drift apart.

## Source

The original template is published at
<https://python.ju.se/ProgrammingFundamentals/writing_documentation.html#report-template-swedish>.

This repo tracks that template for installation on JupyterHub (`jupyter.ju.se`) and elsewhere.
