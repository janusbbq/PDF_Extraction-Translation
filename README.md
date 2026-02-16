# Translate long PDF-Reports in Python.
![Style](https://img.shields.io/badge/Style-Flake8-brightgreen.svg)
[![Continuous Integration](https://github.com/pcschreiber1/PDF_Extraction-Translation/actions/workflows/CI.yml/badge.svg)](https://github.com/pcschreiber1/PDF_Extraction-Translation/actions/workflows/CI.yml)
[![codecov](https://codecov.io/gh/pcschreiber1/PDF_Extraction-Translation/branch/main/graph/badge.svg?token=R2T8WEHXL8)](https://codecov.io/gh/pcschreiber1/PDF_Extraction-Translation)

Translate many large PDF Reports for free using Python. You can find the corresponding *Towards Data Science* article [here](https://towardsdatascience.com/translate-long-pdf-reports-in-python-eab3be08ceb4) or follow the Jupyter Notebook `Article_PDF-Translation` - the Central Bank Report is stored in `examples`.

This repo stores the pipeline developed for work, where a large number of official reports from different OECD countries had to be translated. To translate free of charge, the `GoogleTranslate` API is used. The main python packages are: `pdfplumber`, `deep_translator`, and `pyfpdf2`.

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/pcschreiber1/PDF_Extraction-Translation.git
cd PDF_Extraction-Translation
```

### 2. Create the Conda Environment
```bash
conda env create -f environment.yml
```

### 3. Activate the Environment
```bash
conda activate pdftranslation
```

### 4. Install the Jupyter Kernel
```bash
$CONDA_PREFIX/bin/python -m ipykernel install --user --name=pdftranslation --display-name "Python (pdftranslation)"
```

### 5. Download NLTK Data
```bash
$CONDA_PREFIX/bin/python -c "import nltk; nltk.download('punkt')"
```

### 6. Create the Output Directory
```bash
mkdir -p output
```

## Running the Notebook

### In VS Code
1. Open `Article_PDF-Translation.ipynb`
2. Select the **Python (pdftranslation)** kernel from the top-right corner
3. Click **Run All** or run cells individually with `Shift+Enter`

### In Jupyter Notebook/Lab
1. Launch Jupyter: `jupyter notebook` or `jupyter lab`
2. Open `Article_PDF-Translation.ipynb`
3. Select **Kernel** → **Change kernel** → **Python (pdftranslation)**
4. Run all cells

The translated PDF will be saved to `output/trans_1978-geschaeftsbericht-data.pdf.pdf`.
