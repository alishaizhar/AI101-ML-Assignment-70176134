# AI-101 Machine Learning Assignment: Three Data Modalities
**The University of Lahore • Department of Intelligent Systems • Fall 2026**  
**Instructor:** Dr. Muhammad Awais, AI Architect

---

## Student Identification
| Field | Value |
|---|---|
| **Student Name** | Alisha Izhar |
| **Roll Number** | 70XXXXXX *(Update to your exact roll number if needed)* |
| **Section** | A |
| **GitHub Repository** | `https://github.com/alishaizhar/AI101-ML-Assignment-70XXXXXX` |

---

## Attempted Graded Tasks (One per Pool)
| Pool | Modality | Task ID & Title | Executed Notebook | 2-Page IEEE Report |
|---|---|---|---|---|
| **Pool A** | Numerical | **Task A2: Predicting Concrete Compressive Strength** | [`A2_Concrete_Strength/A2_notebook.ipynb`](A2_Concrete_Strength/A2_notebook.ipynb) | [`A2_Concrete_Strength/report/70XXXXXX_A2_Report.pdf`](A2_Concrete_Strength/report/70XXXXXX_A2_Report.pdf) |
| **Pool B** | Mixed (Text + Structured) | **Task B3: Predicting Star Ratings of Clothing Reviews** | [`B3_Clothing_Reviews/B3_notebook.ipynb`](B3_Clothing_Reviews/B3_notebook.ipynb) | [`B3_Clothing_Reviews/report/70XXXXXX_B3_Report.pdf`](B3_Clothing_Reviews/report/70XXXXXX_B3_Report.pdf) |
| **Pool C** | Sequence-to-Sequence | **Task C2: Abstractive Summarisation of BBC News (XSum)** | [`C2_XSum_Summarisation/C2_notebook.ipynb`](C2_XSum_Summarisation/C2_notebook.ipynb) | [`C2_XSum_Summarisation/report/70XXXXXX_C2_Report.pdf`](C2_XSum_Summarisation/report/70XXXXXX_C2_Report.pdf) |

**Bonus Tasks:** None (Focusing on 3 complete, high-precision graded tasks).

---

## Executive Summary of Results

### Pool A: Task A2 — Concrete Compressive Strength
- **Best Model:** Gradient Boosting Regressor with Domain Feature Engineering ($w/c$ ratio and $\log(\text{age})$).
- **Test Set Metrics:** RMSE = **4.29 MPa** (61.6% lower than the raw linear baseline of 11.19 MPa), MAE = **2.83 MPa**, $R^2$ = **0.938**.
- **Key Finding:** Linearity assumptions are heavily violated by early concrete hydration kinetics. Log-transforming age and calculating the water/cement ratio (Abrams' law) linearizes curing growth and drastically reduces error across all models.

### Pool B: Task B3 — E-Commerce Clothing Reviews Star Rating
- **Best Model:** Multinomial Logistic Regression with Balanced Class Weighting ($C=1.0$).
- **Test Set Metrics:** Macro-F1 = **0.484**, Accuracy = **63.4%**, Weighted-F1 = **0.643**, Ordinal MAE = **0.450 stars**.
- **Key Finding:** Feature ablation proves natural language review text overwhelmingly drives predictive accuracy (Text-only macro-F1: 0.486 vs Structured-only: 0.201). Re-framing into 3 operational sentiment tiers (Negative 1–2, Neutral 3, Positive 4–5) raises accuracy to **82.0%** and macro-F1 to **0.656**.

### Pool C: Task C2 — Abstractive BBC News Summarisation (XSum)
- **Best Model:** Pretrained `t5-small` fine-tuned with beam search ($k=4$, `no_repeat_ngram_size=3`).
- **Test Set Metrics:** ROUGE-1 = **37.42**, ROUGE-2 = **14.85**, ROUGE-L = **29.60**.
- **Key Finding:** Extractive Lead-1 fails on XSum (ROUGE-1: 16.32) because BBC leads are narrative and target summaries contain 56.8% novel bigrams. While fine-tuned T5 outperforms recurrent models by ~19 ROUGE-1 points, an audit of 20 generations revealed a 35% hallucination rate, demonstrating the need for factuality-guided evaluation.

---

## Environment Setup and Reproduction Instructions

### 1. Environment Installation
Ensure Python 3.11+ is installed. Clone the repository and install dependencies:
```bash
git clone https://github.com/alishaizhar/AI101-ML-Assignment-70XXXXXX.git
cd AI101-ML-Assignment-70XXXXXX
pip install -r requirements.txt
```

### 2. Dataset Acquisition
- **Task A2:** Automatically loaded via `ucimlrepo` or downloaded directly from [UCI Machine Learning Repository (ID 165)](https://archive.ics.uci.edu/dataset/165).
- **Task B3:** Downloaded from [Kaggle: Women's E-Commerce Clothing Reviews](https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews) and placed as `B3_Clothing_Reviews/data/Womens Clothing E-Commerce Reviews.csv`.
- **Task C2:** Automatically streamed and partitioned via Hugging Face `datasets` (`EdinburghNLP/xsum`).

### 3. Notebook Execution
- All notebooks are configured with fixed random seed `SEED = 42` and strict no-leakage pipelines.
- **A2 and B3** run directly on CPU within 5–15 minutes.
- **C2** can be run on Google Colab or Kaggle with a T4 GPU.

### 4. Compiling the LaTeX Reports
LaTeX source code for all three reports is located in each task's `report/source/` directory:
- `A2_Concrete_Strength/report/source/A2_report.tex`
- `B3_Clothing_Reviews/report/source/B3_report.tex`
- `C2_XSum_Summarisation/report/source/C2_report.tex`

To compile on Overleaf:
1. Create a new Overleaf project for each task.
2. Upload the respective `.tex` file and the `figures/` folder.
3. Select pdfLaTeX or XeLaTeX and compile. Each report strictly conforms to the 2-page double-column IEEE conference format.

---

## Compliance and Integrity Checklist
- [x] One task attempted per pool: Pool A (A2), Pool B (B3), Pool C (C2).
- [x] All notebooks executed from top to bottom with full outputs saved.
- [x] Zero data leakage: scalers, imputers, encoders, and vocabularies fitted strictly on training splits.
- [x] Evaluated once on held-out test sets using uniform seeds (`seed = 42`).
- [x] Every number in the IEEE reports matches notebook outputs exactly.
- [x] All three reports are strictly 2 pages of double-column content in IEEE style.
- [x] AI usage disclosed comprehensively in `AI_DISCLOSURE.md` and in every report.
