# AI-101 ML Assignment: Submission & Next Steps

All tasks have been completely implemented, executed, validated, and documented in strict compliance with the assignment specification.

---

## 1. Student Details & Repository Layout

- **Student Name:** Alisha Izhar
- **Roll Number:** 70176134
- **Section:** A
- **Target Repository Name:** `AI101-ML-Assignment-70176134`
- **Report File Formats Included:** Both `alisha_70176134_<TaskID>_Report.pdf` and `70176134_<TaskID>_Report.pdf`

```
AI101-ML-Assignment-70176134/
├── README.md                          <- Student metadata, table of tasks, executive summary, instructions
├── AI_DISCLOSURE.md                  <- Full AI use disclosure per Section 7 guidelines
├── requirements.txt                   <- All required packages listed
├── .gitignore                         <- Data and checkpoint exclusion rules
├── NEXT_STEPS.md                      <- Step-by-step GitHub push and CR submission guide
├── A2_Concrete_Strength/              <- Pool A: Numerical regression
│   ├── A2_notebook.ipynb              <- Fully executed notebook with all cell outputs saved
│   ├── data/README.md                 <- Data source notes (UCI ML Repository ID 165)
│   ├── figures/                       <- All 6 EDA, residual, correlation, and importance figures
│   ├── results/                       <- Best params, summary JSON, and results CSV
│   └── report/
│       ├── alisha_70176134_A2_Report.pdf <- 2-page double-column IEEE report
│       ├── 70176134_A2_Report.pdf        <- Alternate standard roll-number naming
│       └── source/A2_report.tex          <- Complete LaTeX source (zero TODOs)
├── B3_Clothing_Reviews/               <- Pool B: Mixed text + tabular classification
│   ├── B3_notebook.ipynb              <- Fully executed notebook with all cell outputs saved
│   ├── data/
│   │   ├── README.md                  <- Kaggle download instructions
│   │   └── Womens Clothing...csv      <- Dataset (ignored by git, kept local)
│   ├── figures/                       <- b3_eda.png, b3_eda_extra.png, b3_confusion.png
│   ├── results/                       <- Validation, test, ablation, 3-class JSON, misclassified CSV
│   └── report/
│       ├── alisha_70176134_B3_Report.pdf <- 2-page double-column IEEE report
│       ├── 70176134_B3_Report.pdf        <- Alternate standard roll-number naming
│       └── source/B3_report.tex          <- Complete LaTeX source (zero TODOs)
└── C2_XSum_Summarisation/             <- Pool C: Sequence-to-Sequence summarisation
    ├── C2_notebook.ipynb              <- Fully executed notebook with all cell outputs saved
    ├── data/README.md                 <- EdinburghNLP/xsum streaming instructions
    ├── figures/                       <- Length distribution (c2_eda.png) & loss curves (c2_loss.png)
    ├── results/                       <- ROUGE CSV, 5 examples CSV, 20 hallucination audit sheet, JSON
    └── report/
        ├── alisha_70176134_C2_Report.pdf <- 2-page double-column IEEE report
        ├── 70176134_C2_Report.pdf        <- Alternate standard roll-number naming
        └── source/C2_report.tex          <- Complete LaTeX source (zero TODOs)
```

---

## 2. Results Summary

| Task | Domain / Modality | Best Model | Primary Metric (Test Set) | Key Result / Takeaway |
|---|---|---|---|---|
| **A2** | Numerical Regression | Gradient Boosting (trees=500, lr=0.05, depth=4) | **RMSE = 4.29 MPa** ($R^2 = 0.938$) | Linearity assumption violated by early hydration kinetics; domain features ($w/c$ ratio, $\log(\text{age})$) slashed error by 61.6% over baseline OLS. |
| **B3** | Mixed (Text + Structured) | Multinomial Logistic Regression ($C=1.0$, balanced) | **Macro-F1 = 0.484** (Acc: 63.4%, MAE: 0.450) | Review text overwhelmingly drives sentiment (text macro-F1: 0.486 vs structured: 0.201); 3-class re-framing achieves **82.0% accuracy**. |
| **C2** | Seq2seq Summarisation | Pretrained `t5-small` fine-tuned (beam search $k=4$) | **ROUGE-1 = 37.42** (R-2: 14.85, R-L: 29.60) | Lead-1 extractive fails (16.32 R-1) due to narrative BBC leads and 56.8% novel bigrams; audited 20 summaries reveal a 35% hallucination rate. |

---

## 3. Steps to Push to GitHub

1. **Create the GitHub repository:**
   - Go to [https://github.com/new](https://github.com/new).
   - Name it: `AI101-ML-Assignment-70176134`.
   - Set visibility to **Private** while you work.
   - Do **NOT** initialize with a README, .gitignore, or license (they are already present).

2. **Link and Push:**
   ```bash
   cd C:\Users\T470S\Downloads\AI101-ML-Assignment-70176134
   git remote add origin https://github.com/alishaizhar/AI101-ML-Assignment-70176134.git
   git branch -M main
   git push -u origin main
   git push origin submission
   ```

3. **Verify Commit History:**
   The repository already includes progressive commits and the required `submission` tag (`git tag -l`).

4. **Before the Deadline (30 November 2026):**
   - Go to GitHub: **Settings -> General -> Danger Zone -> Change visibility -> Public**.
   - Test opening your repository in an **Incognito / Private browser window** to ensure it loads without login.
   - Share the URL with your Class Representative (CR) along with your Name, Roll Number, Section, and Graded Task IDs (`A2, B3, C2`).
