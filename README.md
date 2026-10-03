# Biometric Verification & Performance Analysis (FAR, FRR, EER)

An end-to-end evaluation pipeline for biometric verification systems. This project calculates similarity scores between biometric feature vectors using Euclidean distance, analyzes Genuine and Imposter score distributions, and evaluates system performance via FAR, FRR, and EER metrics.

---

## Project Overview
Biometric authentication accuracy depends on distinguishing genuine users from imposters. This repository processes multidimensional biometric feature embeddings, normalizes the feature space, and simulates match verification across hundreds of subjects and sessions.

### Key Highlights
- **Feature Normalization:** Min-Max scaling of multi-dimensional feature tensors across subjects and capture instances.
- **Euclidean-Based Matcher:** Inverses Euclidean distance into a normalized similarity score (0 ≤ score ≤ 1).
- **Score Distribution Simulation:**
  - **Genuine Matches:** 4,500 intra-class matching combinations.
  - **Imposter Matches:** 445,500 inter-class matching combinations.
- **Performance Evaluation:** Threshold sweeping (1,000 points) to compute False Acceptance Rate (**FAR**) and False Rejection Rate (**FRR**).
- **Equal Error Rate (EER):** Automatically identifies the optimal operating threshold where FAR ≈ FRR.

---

##  Benchmark Results

| Metric | Measured Value | Description |
| :--- | :--- | :--- |
| **Mean Genuine Score** | **0.914** | High intraclass confidence |
| **Mean Imposter Score** | **0.766** | Distinct interclass separation |
| **Optimal Threshold** | **0.8639** | Decision boundary for balance |
| **EER (Equal Error Rate)** | **4.64% (0.0464)** | System accuracy benchmark |

---

## Visualizations
The analysis produces three key analytical plots:
1. **Score Distributions:** Genuine vs. Imposter histograms demonstrating separability.
2. **Threshold vs. Error Curves:** FAR and FRR intersection highlighting the EER point.
3. **Biometric ROC Curve:** Depicting the trade-off between False Accept and False Reject rates.

---

## Tech Stack
- **Language:** Python
- **Libraries:** NumPy, Matplotlib, Jupyter Notebook

---

## How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/melisaaleyna/biometric-verification-eer-analysis.git](https://github.com/melisaaleyna/biometric-verification-eer-analysis.git)
   cd biometric-verification-eer-analysis
