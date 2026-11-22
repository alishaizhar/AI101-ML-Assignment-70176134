# AI Use Disclosure

This disclosure applies to all three tasks attempted for the AI-101 Machine Learning Assignment (Task A2: Predicting Concrete Compressive Strength, Task B3: Predicting Star Ratings of E-Commerce Clothing Reviews, and Task C2: Abstractive Summarisation of BBC News Articles).

## Statement of AI Assistance

I used **Google DeepMind Antigravity (powered by Gemini)** for explaining machine learning concepts, providing pipeline boilerplate code, assisting in debugging data processing workflows, structuring exploratory data analysis, and drafting the two-column IEEE LaTeX templates.

### Specific Parts Generated or Assisted by AI:
1. **Task A2 (Concrete Compressive Strength):**
   - Boilerplate structure for scikit-learn cross-validation pipelines (`A2_notebook.ipynb` Cells 7, 9).
   - Drafting LaTeX equations and tables in `A2_report.tex`.
2. **Task B3 (Clothing Review Ratings):**
   - Syntax for scikit-learn `ColumnTransformer` combining `TfidfVectorizer`, `OneHotEncoder`, and `StandardScaler` (`B3_notebook.ipynb` Cell 7).
   - Drafting LaTeX summary and ablation tables in `B3_report.tex`.
3. **Task C2 (BBC News Summarisation):**
   - Encoder-decoder recurrent model skeleton and PyTorch dataset collation routines (`C2_notebook.ipynb` Cells 9, 13).
   - Drafting LaTeX hyperparameter and ROUGE benchmark tables in `C2_report.tex`.

### Verification and Academic Integrity
I verified all content by:
- Executing every notebook end-to-end and saving all outputs locally.
- Auditing generated prediction outputs, checking confusion matrices, and inspecting misclassified examples directly against the raw datasets.
- Manually verifying the factual consistency of 20 abstractive summaries for the hallucination study.
- Cross-checking all reported metrics, tables, and figures against the saved output artifacts.

All experiments, results, and analyses presented in these notebooks and reports were produced and verified by me, and I take full responsibility for this work.
