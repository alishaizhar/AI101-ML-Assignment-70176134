# What YOU must do (not in the repo submission, delete before submitting if you like)

## 0. Setup (10 min)
- Rename the folder to AI101-ML-Assignment-<YourRollNo>, create the GitHub repo (Private), copy these files in.
- Put name/roll/section into README.md and AI_DISCLOSURE.md.

## 1. A2 (laptop or Colab, about 5 min run)
1. Open A2_notebook.ipynb, Run All. Copy figures/ and results/ stay in the A2 folder.
2. Read the printed tables. Fill every red [..] (\TODO) in report/source/A2_report.tex with numbers from the notebook.
3. Write the Analysis paragraph in your own words (the questions are listed in the .tex).
4. Overleaf: upload the .tex and the figures/ folder, compile, check it is at most 2 pages (+ disclosure/references), download as <RollNo>_A2_Report.pdf into report/.

## 2. B3 (laptop or Colab, about 10-20 min run)
Same steps. Download the dataset first (see data/README.md). Write about the 3 misclassified reviews from results/b3_misclassified.csv.

## 3. C2 (Colab T4 GPU, about 1 hour)
1. Colab: Runtime -> T4 GPU. Upload the notebook, uncomment the pip line, Run All.
2. Download figures/ and results/ before the runtime disconnects (or mount Drive).
3. Manual work: read 20 summaries in results/c2_hallucination_sheet.csv and mark hallucination 1/0.
4. Fill the .tex, compile on Overleaf.

## 4. Commits (at least 5 per task, spread over days). Example for A2:
git add A2_Concrete_Strength/data; git commit -m "A2: data notes"
git add A2_Concrete_Strength/A2_notebook.ipynb; git commit -m "A2: EDA and statistics"
(run more cells, save, commit after each milestone: "A2: feature engineering", "A2: tuned models", "A2: figures and results", "A2: report")
Final: git tag -a submission -m "Final submission - AI101 ML Assignment"; git push origin main; git push origin submission

## 5. Before the deadline (30 Nov)
Repo Public, check in incognito, send link + roll no + name + section + A2/B3/C2 to the CR, confirm your row exists.
