# ARP Poisoning Detection using Gradient Boosting Machines

> **Course:** Research Methods in Computer Science (CoSc3101)
> **Institution:** Hawassa University Institute of Technology
> **Department:** Computer Science, Year III Semester II — 2018/2026 A/Y
> **Advisor:** Mr. Birhane Bekele
> **Student:** Dagim Abate (ID: 1716/16)

---

## Abstract

Address Resolution Protocol (ARP) poisoning is one of the most prevalent Man-in-the-Middle (MitM) attack vectors in enterprise Wireless Local Area Networks (WLANs), enabling attackers to silently intercept, alter, or drop network traffic between legitimate hosts. Traditional rule-based and signature-driven ARP protection mechanisms fail against sophisticated, low-rate poisoning attempts that evade static detection thresholds. This proposal presents a machine learning approach to ARP poisoning detection using Gradient Boosting Machines (GBM), leveraging network flow-level features extracted from enterprise WLAN traffic. Using the CIC-IDS2017 and a custom-generated ARP poisoning dataset captured in a controlled lab environment, the study trains and evaluates XGBoost, LightGBM, and CatBoost classifiers, comparing their detection accuracy, precision, recall, F1-score, and false positive rate against baseline methods including Random Forest and SVM. The proposed GBM-based detection framework aims to achieve a detection accuracy exceeding 98% and a false positive rate below 2%, providing a practical, deployable solution for enterprise network administrators to detect MitM ARP poisoning attacks in real time.

---

## Repository Contents

```
ARP-Poisoning-Detection-GBM/
├── README.md          ← Project overview and abstract
├── main.tex           ← Full LaTeX source of the research proposal
└── references.bib     ← BibTeX file with all cited references
```

---

## How to Compile the Proposal

### Option 1 — Overleaf (Recommended, no installation needed)

1. Go to [overleaf.com](https://overleaf.com) → **New Project → Blank Project**
2. Delete the default `main.tex` content and paste the content of `main.tex`
3. Upload `references.bib` as a separate file (Upload icon on the left panel)
4. Set compiler to **pdfLaTeX** → Menu → Compiler → pdfLaTeX
5. Click **Recompile** → download the compiled PDF

### Option 2 — Local Compilation (requires TeX Live or MiKTeX)

```bash
# Clone the repository
git clone https://github.com/Dagi7d/ARP-Poisoning-Detection-GBM.git
cd ARP-Poisoning-Detection-GBM

# Compile the LaTeX document (run 3 times for references to resolve)
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

---

## Research Overview

| Item | Detail |
|---|---|
| **Topic** | MitM ARP Poisoning Detection in Enterprise WLANs |
| **Approach** | Gradient Boosting Machines (XGBoost, LightGBM, CatBoost) |
| **Datasets** | CIC-IDS2017 (IEEE DataPort) + Custom WLAN capture |
| **Baselines** | Random Forest, SVM |
| **Explainability** | SHAP feature importance analysis |

## Evaluation Metrics

| Metric | Target |
|---|---|
| Accuracy | ≥ 98% |
| F1-score | ≥ 0.97 |
| False Positive Rate (FPR) | ≤ 2% |
| AUC-ROC | ≥ 0.99 |

---

## Ethics & Reproducibility

- All datasets are publicly available benchmarks or lab-captured with no real user data.
- Attack simulations performed exclusively on an isolated private testbed.
- Research findings intended to assist network defenders only.
- GDPR-compliant: no personal data collected or processed.

---

## Author

**Dagim Abate**
Department of Computer Science
Hawassa University Institute of Technology
📧 dagimabate4@gmail.com

---

## License

This project is released under the [MIT License](LICENSE) for academic use.
