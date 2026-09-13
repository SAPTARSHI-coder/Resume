# Curriculum Vitae — Saptarshi Sadhu

[![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=flat&logo=LaTeX&logoColor=white)](research_cv.tex)
[![PDF Status](https://img.shields.io/badge/Status-Compiled-success)](research_cv.pdf)
[![CGPA](https://img.shields.io/badge/CGPA-9.30%20%2F%2010.00-blue)](https://saptarshisadhu.co.in)
[![Committers.top Rank](https://img.shields.io/badge/India%20Rank-%233%20Private%20Committer-orange)](https://committers.top/india_private)

A modern, high-impact, research-oriented **Curriculum Vitae** built from scratch using standard LaTeX packages. Engineered for applications to top-tier research institutions (*IISc, IITs, ETH Zurich, EPFL, CMU, MIT*) and PhD/Graduate admissions committees.

---

## 👤 Candidate Profile

**Saptarshi Sadhu**  
*Computer Science & Engineering Undergraduate (Specialization in AI & ML)*  
**Adamas University**, Kolkata, India  
- 📧 **Email**: [saptarshisadhuofficial@gmail.com](mailto:saptarshisadhuofficial@gmail.com)
- 🌐 **Portfolio**: [saptarshisadhu.co.in](https://saptarshisadhu.co.in)
- 🐙 **GitHub**: [SAPTARSHI-coder](https://github.com/SAPTARSHI-coder)
- 💼 **LinkedIn**: [in/saptarshi-sadhu](https://linkedin.com/in/saptarshi-sadhu)
- 🆔 **ORCID**: [0009-0009-7505-1973](https://orcid.org/0009-0009-7505-1973)
- 🎓 **Google Scholar**: [Saptarshi Sadhu](https://scholar.google.com/citations?hl=en&user=CnV674wAAAAJ)

---

## 📁 Repository Structure

```
research_cv/
├── research_cv.tex         # Master LaTeX source document
├── research_cv.pdf         # Compiled 2-page research CV (PDF output)
├── picture.jpg             # Profile photo asset embedded in header
├── DESIGN.md               # Complete design specification & macro architecture
├── README.md               # Project documentation and summary
├── main.log                # Build log
└── research_cv.synctex.gz  # SyncTeX file for editor navigation
```

---

## 🔬 Key Highlights in CV

### 🎓 Academic Record
- **B.Tech CSE (AI & ML)** — Adamas University, Kolkata | **CGPA: 9.30 / 10.00**
- **Higher Secondary (Class XII)** — B.T. Road Govt. Spon. H.S. School | **Score: 89.6%** (PCMB Stream)
- **Secondary (Class X)** — B.T. Road Govt. Spon. H.S. School | **Score: 93.7%**

### 📚 Manuscripts in Preparation (2026)
1. **Ozone Photochemical Regimes and Particulate Transport in Kolkata and Howrah**  
   *Argha Kamal Guha, Saptarshi Sadhu, Chirag Deb.* (2026)
2. **Spatial Autocorrelation, RNN & Statistical Distribution Framework for Air Quality Forecasting in Kolkata–Howrah Airshed**  
   *Argha Kamal Guha, Saptarshi Sadhu, Susmit Bagchi, Chirag Deb.* (2026)
3. **Assessment of Particulate and Gaseous Pollution: Case Study of Barrackpore Municipality**  
   *Argha Kamal Guha, Enubothula Bala Mani, Piyush Raj, Navnit Kumar, Saptarshi Sadhu, Snehamanju Basu.* (2026)
4. **Enhancing Micro Electrochemical Spark Machining via Electrolyte Sonication**  
   *Co-authors, Saptarshi Sadhu (4th Author).* (2026)

### 🌟 Open Source Leadership
- **Lead Maintainer** of [EaseMotion CSS Framework](https://github.com/SAPTARSHI-coder/EaseMotion-css) under GirlScript Summer of Code (GSSoC '26).
- **Ranked #3 Private Committer in India** & **#2 Active Committer** on [Committers.top](https://committers.top/india_private).
- Scaled repository to **25,424 merged PRs, 62,001 commits, and 704 contributors** (averaging 496 PRs/day).
- Deployed automated **Honeypot Sandbox System** to block spam and optimized CI/CD pipelines from 3m down to <25s.

### 🏆 Honors & Awards
- **ACM Summer School at IISc Bangalore (July 2026)**: Selected participant for advanced computing summer school.
- **Google Student Ambassador (2026)**: Campus representative leading technical workshops.
- **AWS College Showcase (Feb 2026)**: Top 7 selection for cloud innovation.
- **4th Place Coding Premier League (Apr 2026)**: Algorithmic competitive programming finish.
- **HackerRank**: **4-Star in C** | **3-Star in C++ / Problem Solving**.

### 💼 Leadership & Service
- **Publicity Chair** — ACM Student Chapter, Adamas University (Apr 2026 – Present)
- **Student Coordinator** — IETE Student Chapter, Adamas University (Mar 2026 – Present)
- **Class Representative (CR)** — Department of CSE, Adamas University (Oct 2025 – Present)
- **Team Leader** — AI Impact Summit Buildathon (HCL GUVI) & Smart India Hackathon (SIH 2024 & 2025)

---

## ⚙️ Compilation & Build Instructions

### Prerequisites
Ensure you have a standard TeX distribution installed:
- **Linux**: `sudo apt install texlive-full`
- **macOS**: `brew install --cask mactex`
- **Windows**: [MiKTeX](https://miktex.org/) or [TeX Live](https://www.tug.org/texlive/)

### Building the PDF
Run `pdflatex` or `latexmk` from inside the `research_cv` directory:

```bash
# Using latexmk (recommended)
latexmk -pdf research_cv.tex

# Direct compilation
pdflatex research_cv.tex
```

---

## 🎨 Design System

- **Primary Accent**: `#3873AD` (`cvblue` — Classic ModernCV Blue)
- **Primary Text**: `#333333` (`cvdark` — Soft Dark)
- **Subtitles & Hints**: `#7F7F7F` (`cvgray` — Slate Gray)
- **Layout Architecture**: Custom two-column minipage layout with orphan prevention (`\needspace{5\baselineskip}` & `\nopagebreak`). Zero external template dependencies (`moderncv.cls` or `awesome-cv.cls` free).

---

## 🛡️ License, Copyright & Legal Protection

[![License: Proprietary / All Rights Reserved](https://img.shields.io/badge/License-All_Rights_Reserved-red.svg)](LICENSE)

**Copyright © 2026 Saptarshi Sadhu. All Rights Reserved.**

### ⛔ Usage & Protection Terms:
- **Strict Anti-Plagiarism & Anti-Impersonation**: You are **strictly prohibited** from copying, reproducing, or publishing any of Saptarshi Sadhu's personal achievements, manuscript titles, research metrics, academic scores, or project statistics under another person's name.
- **No Commercial Exploitation**: No part of this CV, document content, or personal assets may be harvested, scraped, resold, or sublicensed for commercial resume services or talent databases.
- **Permitted Use (LaTeX Template Structure)**: You may reference and adapt the structural LaTeX layout logic (`research_cv.tex` macro setup) for your own resume, **provided that all personal text, project data, publication titles, and candidate identifiers belonging to Saptarshi Sadhu are completely removed**.

For official verification or inquiries, please contact: [saptarshisadhuofficial@gmail.com](mailto:saptarshisadhuofficial@gmail.com)
