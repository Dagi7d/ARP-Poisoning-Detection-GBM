# Adversarial IDS — Ensemble Adversarial Training (EAT)

> **Course:** Research Methods in Computer Science (CoSc3101)  
> **Institution:** Hawassa University Institute of Technology  
> **Department:** Computer Science, Year III Semester II — 2018/2026 A/Y  
> **Advisor:** Mr. Birhane Bekele  
> **Student:** Dagim Abate (ID: 1716/16)

---

## Abstract

Deep learning-based Intrusion Detection Systems (DL-IDS) have become a cornerstone of modern cybersecurity infrastructure; however, they remain critically vulnerable to adversarial examples — carefully crafted perturbations that cause misclassification while remaining imperceptible to human analysts. This project investigates the robustness of DL-IDS models against white-box and black-box adversarial attacks and proposes an **Ensemble Adversarial Training (EAT)** framework that simultaneously hardens multiple neural architectures (CNN, LSTM, Autoencoder). Using the CICIDS2017 and NSL-KDD benchmark datasets, the study quantifies detection degradation under FGSM, PGD, and Carlini–Wagner attacks, then evaluates whether the proposed EAT strategy restores and exceeds baseline detection rates. Evaluation metrics include accuracy, F1-score, False Negative Rate (FNR), and Adversarial Robustness Score (ARS). This research addresses the absence of a unified, dataset-agnostic adversarial hardening approach for network intrusion detection and contributes a reproducible open-source framework for the cybersecurity community.

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

# Compile the LaTeX document
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

---

## Evaluation Metrics

| Metric | Target |
|---|---|
| Accuracy | ≥ 95% (clean), ≥ 85% (adversarial) |
| F1-score | ≥ 0.90 post-hardening |
| False Negative Rate (FNR) | ≤ 0.08 |
| Adversarial Robustness Score (ARS) | ≥ 0.85 |

---

## Ethics & Reproducibility

- All datasets used (CICIDS2017, NSL-KDD) are publicly available benchmarks with no real user data.
- Research complies with GDPR principles — no personal data is collected or processed.
- Potential dataset bias is mitigated by evaluating on two independent benchmark datasets.

---

## Author

**Dagim Abate**  
Department of Computer Science  
Hawassa University Institute of Technology  
📧 dagimabate4@gmail.com

---

## License

This project is released under the [MIT License](LICENSE) for academic use.
