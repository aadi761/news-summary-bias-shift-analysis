# Automatic News Summarization and Political Bias Analysis

**Measuring Ideological Shift Across Transformer-Based Models (BART, T5, Pegasus)**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📋 Project Overview

This project investigates whether popular transformer-based abstractive summarization models (BART, T5, and Pegasus) introduce **ideological shifts** when summarizing political news articles.

Using the `PoliticalBias_AllSides_Txt` dataset (~17,054 articles labeled Left/Center/Right), we:
- Fine-tuned **PoliticalBERT** (`buckethead777/political-bert` or similar) achieving **79.9% accuracy**.
- Generated summaries with BART, T5, and Pegasus.
- Detected high ideological shift rates (**65.5%** for BART, **61.6%** for T5, **61.0%** for Pegasus).
- Identified **1,620 trigger sentences** associated with shifts.
- Proposed and evaluated three correction strategies (sentence injection, prefix conditioning, hybrid) that improve the **Ideological Preservation Rate (IPR)** from 34.5% to **93.8%**.

This is a final year / capstone project from **Chandigarh University**.

## 👥 Team Members

- **Adithya** 
- **Fathimathu Rusfida** 
- **Savnmandeep Kaur**
- **Marupudi Rithika**
- **Ikram Ali**

**Department of CSE-AIT, Apex Institute of Technology, Chandigarh University, Punjab, India**

## 📁 Repository Contents

- `political_bias_analysis.ipynb` — Complete Jupyter notebook containing the full pipeline:
  - Data loading & leakage-proof preprocessing
  - PoliticalBERT fine-tuning & evaluation
  - Summarization with BART, T5, Pegasus
  - Shift detection, trigger sentence analysis
  - Correction strategies & metrics (CHR, IPR, etc.)
  - Visualizations

## 🛠️ Technologies Used

- **Transformers**: Hugging Face (PoliticalBERT, BART-large-cnn, T5-small, Pegasus)
- **Data Science**: pandas, numpy, scikit-learn, matplotlib, seaborn
- **NLP**: NLTK, ROUGE
- **Environment**: Google Colab / Jupyter Notebook

## 📊 Key Results

- Classifier Accuracy: **79.9%** (Macro F1: 0.790)
- Shift Rates: BART (65.5%), T5 (61.6%), Pegasus (61.0%)
- Correction Success (CHR): **90.5%**
- IPR Improvement: **+59.3 percentage points** (34.5% → 93.8%)

## 🚀 How to Run the Notebook

1. Open the notebook in **Google Colab** (recommended) or Jupyter.
2. Upload your dataset zip if needed (`PoliticalBias_AllSides_Txt.zip`).
3. Run cells sequentially (some sections require the dataset).
4. Install dependencies (first cell does this).

**Note**: The full dataset is not included in this repository due to size. Contact the team for access if needed.

## 📄 Associated Paper

**Title**: Automatic News Summarization and Political Bias Analysis: Measuring Ideological Shift Across Transformer-Based Models

Authors: Adithya, Fathimathu Rusfida, Savnmandeep Kaur, Marupudi Rithika, Ikram Ali

*(Paper PDF will be added once published/submitted)*

## 📝 Citation (if used)

```bibtex
@misc{political-bias-summarization-2026,
  author = {Adithya and Fathimathu Rusfida and Savnmandeep Kaur and Marupudi Rithika and Ikram Ali},
  title = {Automatic News Summarization and Political Bias Analysis},
  year = {2026},
  publisher = {GitHub},
  howpublished = {\url{https://github.com/FaRusfida/Political-Bias-Summarization-Analysis}}
}
