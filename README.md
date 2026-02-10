# Chinmay Kulkarni — Resume

A modular LaTeX resume with each section in its own file for easy editing.

## Structure

```tree
LaTex-Resume/
├── main.tex                 # Driver file — compiles the full resume
└── sections/
    ├── preamble.tex         # Packages, fonts, spacing, formatting
    ├── header.tex           # Name & contact info
    ├── summary.tex          # Professional summary
    ├── experience.tex       # Work experience
    ├── skills.tex           # Technical skills
    └── education.tex        # Education
```

## How to Compile

### Prerequisites

Install a LaTeX distribution:

| OS      | Distribution                           | Install                                |
|---------|----------------------------------------|----------------------------------------|
| Windows | [MiKTeX](https://miktex.org/download)  | Download installer from site           |
| Windows | [TeX Live](https://tug.org/texlive/)   | `winget install TeXLive`               |
| macOS   | [MacTeX](https://tug.org/mactex/)      | `brew install --cask mactex`           |
| Linux   | TeX Live                               | `sudo apt install texlive-full`        |

### Compile

From the repository root:

```bash
pdflatex main.tex
```

This produces **main.pdf** in the same directory.

> **Note:** If the resume uses references or hyperlinks, you may need to run `pdflatex main.tex` twice for cross-references to resolve.

### Alternative: Overleaf

You can also compile without a local installation by uploading the repository to [Overleaf](https://www.overleaf.com/) — it will build the PDF automatically.

## Editing

Each section is independent — edit the relevant file under `sections/` and recompile. To add a new section, create a file in `sections/` and add `\input{sections/<filename>}` to `main.tex`.
