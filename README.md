# Network Intrusion Detection System (CNN-LSTM)

A CNN-LSTM based Network Intrusion Detection System (NIDS) with a stacking
ensemble classifier and a Flask web interface for real-time, secure model
interaction.

<!-- Add a screenshot once you have one:
![Dashboard](screenshots/dashboard.png)
-->

## Overview

This project detects malicious network traffic by combining deep learning
(CNN-LSTM) feature extraction with a stacking ensemble of classical models
(ExtraTrees, LinearSVC, Logistic Regression). To address class imbalance in
intrusion datasets, it uses CDAAE-KNN synthetic data augmentation before
training.

## Results

| Dataset   | Metric              | Score  |
|-----------|----------------------|--------|
| KDD-CUP   | F1-score             | 98.9%  |
| UNSW-NB15 | Accuracy             | 99.6%+ |
| —         | F1 improvement vs. baseline SVM | +10.7% |

## Architecture

- **Feature extraction:** CNN-LSTM
- **Classification:** Stacking ensemble — ExtraTrees + LinearSVC + Logistic Regression
- **Class imbalance handling:** CDAAE-KNN synthetic data augmentation
- **Web interface:** Flask, with SQLite-backed user authentication for secure,
  real-time model interaction

## Tech Stack

Python · Pandas · Scikit-learn · Flask · SQLite

## Getting Started

```bash
git clone https://github.com/Drakendvk28/Intrusion-Detection-CNN-LSTM.git
cd Intrusion-Detection-CNN-LSTM
pip install -r requirements.txt
python app.py
```

Then open `http://localhost:5000` in your browser.

> Adjust the commands above if your actual folder structure or entry-point
> filename is different — update this section to match how you run the
> project locally.

## Datasets

- [KDD-CUP](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html)
- [UNSW-NB15](https://research.unsw.edu.au/projects/unsw-nb15-dataset)

## Author

**Dakara Venkata Kishore Aditya**
[LinkedIn](https://www.linkedin.com/in/dvk-venkat/) · [GitHub](https://github.com/Drakendvk28)
