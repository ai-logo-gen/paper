# The Minimalist Revolution: Democratizing High-Quality Logo Design with Efficient AI

This repository contains the LaTeX source code for the paper:  
**"The Minimalist Revolution: Democratizing High-Quality Logo Design with Efficient AI"**

**Author:** Paul Hornig  
**Keywords:** Generative AI, Logo Design, Stable Diffusion, LoRA, ControlNet, Parameter-Efficient Fine-Tuning

---

## Overview

This research explores the resource-efficient fine-tuning of Stable Diffusion models for generating minimalist logos. By combining text-to-image generation with structural control via ControlNet, the project demonstrates how high-quality, controllable design automation is achievable on consumer-grade hardware.

## Repository Structure

- `thesis_main.tex`: The main LaTeX document.
- `kapitel/`: Directory containing individual chapters:
  - `einleitung.tex` (Introduction)
  - `grundlagen.tex` (Theoretical Background)
  - `methodik.tex` (Methodology)
  - `implementierung.tex` (Implementation)
  - `ergebnisse.tex` (Results)
  - `diskussion.tex` (Discussion)
  - `fazit.tex` (Conclusion)
  - `declarations.tex` (Declarations & Availability)
  - `anhang.tex` (Appendix)
- `abbildungen/`: Figures and charts used in the manuscript.
- `literatur/`: Bibliography database (`.bib`).
- `sn-jnl.cls`: Springer Nature journal document class.

## Getting Started

### Prerequisites

To compile the manuscript, you need a standard LaTeX distribution (e.g., TeX Live) installed on your system.

**On Ubuntu/Debian:**
```bash
sudo apt update
sudo apt install texlive-latex-base texlive-latex-extra texlive-science texlive-bibtex-extra latexmk
```

### Compiling the Paper

The most efficient way to build the PDF is using `latexmk`, which handles cross-references and bibliographies automatically.

```bash
latexmk -pdf thesis_main.tex
```

Alternatively, you can run `pdflatex` manually:
```bash
pdflatex thesis_main.tex
bibtex thesis_main
pdflatex thesis_main.tex
pdflatex thesis_main.tex
```

The output will be generated as `thesis_main.pdf`.

## Data and Code Availability

- **Dataset:** The processed minimalist logo dataset is available on Kaggle: [Minimalistic Logos, Sketches and Prompts](https://www.kaggle.com/datasets/paulhornig/minimalistic-logos-sketches-and-prompts).
- **Code (Data Prep):** [ai-logo-gen/data-prep](https://github.com/ai-logo-gen/data-prep)
- **Code (Modeling):** [ai-logo-gen/modeling](https://github.com/ai-logo-gen/modeling)
