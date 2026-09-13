# Research CV Design Specification

## Overview & Philosophy
This document specifies the design architecture for a modern, high-impact, research-oriented Curriculum Vitae built entirely from scratch using standard LaTeX packages. The design aims for a premium academic visual identity suitable for applications to top tier research institutions (IITs, IISc, ETH Zurich, EPFL, CMU, MIT) and PhD admissions committees.

---

## 1. Visual Identity & Color Palette

### Primary Color System
- **Accent Blue (`cvblue`)**: `#1D4ED8` (`RGB{29, 78, 216}`) — Used for section headers, bullet accents, key metrics highlights, and horizontal divider bars.
- **Primary Text (`cvprimary`)**: `#0F172A` (`RGB{15, 23, 42}`) — Slate 900 for primary typography, section text, and candidate name.
- **Secondary Text / Subtitles (`cvsecondary`)**: `#475569` (`RGB{71, 85, 105}`) — Slate 600 for dates, locations, institutional affiliations, and subtitles.
- **Muted Gray (`cvmuted`)**: `#64748B` (`RGB{100, 116, 139}`) — Used for metadata labels, rules, and icon tints.
- **Subtle Background (`cvlightbg`)**: `#F8FAFC` (`RGB{248, 250, 252}`) — Used for light highlight boxes or skill tags if applicable.

---

## 2. Typography & Hierarchy

### Font Family & Encoding
- **Engine**: `pdflatex` compatible.
- **Font Packages**: `lmodern` (Latin Modern) or standard Computer Modern / Helvetica (`helvet`) options with `fontenc[T1]` and `inputenc[utf8]`.
- **Icon Support**: `fontawesome5` for general icons, `academicons` for ORCID & Google Scholar.

### Scale & Hierarchy
1. **Candidate Name**: `26pt` bold (`\Huge\bfseries`), Primary color (`cvprimary`), tight tracking.
2. **Title / Professional Designation**: `12pt` medium (`\large\scshape`), Accent color (`cvblue`).
3. **Section Headers (`\section`)**: `12pt` bold small-caps (`\large\bfseries\scshape`), Accent blue (`cvblue`), with a sleek bottom rule (`\titlerule`) or left accent bar.
4. **Subsection Headers (`\subsection`)**: `11pt` bold (`\bfseries`), Primary text color (`cvprimary`).
5. **Body Text**: `10pt` normal (`\normalsize`), line spread `1.15` for optimum readability and whitespace balance.
6. **Dates & Locations**: `9.5pt` italic / slate gray (`\small\itshape\color{cvsecondary}`), right-aligned using `\hfill`.

---

## 3. Geometry, Spacing & Layout Architecture

### Page Margins
- Top: `0.55in` (40pt)
- Bottom: `0.55in` (40pt)
- Left: `0.60in` (43pt)
- Right: `0.60in` (43pt)

### Alignment & Grid Alignment
- Perfect left margin alignment across all section titles, entry titles, and bullet lists (`leftmargin=*` in `enumitem`).
- Right-aligned date ranges and geographic locations using explicit micro-spacing (`\hfill`).
- Tabular alignments using `tabularx` with `@{} X @{}` to eliminate unwanted left/right table padding.

### Micro-Spacing Strategy
- **Section Spacing**: `10pt` before, `5pt` after.
- **Entry Item Spacing**: `3pt` between distinct items within a section.
- **Bullet Item Spacing**: `leftmargin=1.2em`, `itemsep=1.5pt`, `parsep=0pt`, `topsep=2pt`.

---

## 4. Reusable Macro Architecture

All layout structures are encapsulated in clean, custom LaTeX commands:

```latex
% Header Block
\newcommand{\cvheader}[8]{ ... }

% Section Formatting
\titleformat{\section}{\large\bfseries\scshape\color{cvblue}}{}{0em}{}[\color{cvblue}\titlerule]

% Standard Experience / Education Entry
\newcommand{\cventry}[5]{%
  \noindent\textbf{#1} \hfill \textbf{#2} \\
  \textit{#3} \hfill \textit{#4} \\
  #5 \vspace{4pt}
}

% Project Entry with Tech Stack & Link
\newcommand{\cvproject}[5]{%
  \noindent\textbf{#1} \hfill \href{#3}{\small\color{cvblue}\faLink~#3} \\
  \textit{Technologies: #2} \hfill \textit{#4} \\
  #5 \vspace{4pt}
}

% Publication Entry
\newcommand{\cvpub}[5]{%
  \noindent\textbf{#1} (#2). \textit{#3}. #4. \ifthenelse{\equal{#5}{}}{}{\textbf{[#5]}} \vspace{3pt}
}

% Key-Value Skill Line
\newcommand{\cvskill}[2]{%
  \noindent\textbf{#1:} #2 \vspace{2pt}
}
```

---

## 5. Structural Breakdown of CV Sections

1. **Header**: Name, Title, Contact Info (Email, Phone, Location), Links (Portfolio, GitHub, LinkedIn, X, ORCID, Google Scholar), optional profile photo layout.
2. **Professional Summary**: Concise overview of research background, engineering skills, and open-source contributions.
3. **Research Interests**: Categorized list of technical domains (AI/ML, Edge AI, Distributed Systems, Environmental AI, XAI).
4. **Education**: Degrees, institution, CGPA, semester breakdowns, relevant coursework.
5. **Research Experience**: Detailed academic research roles, datasets used, methodology, ML models, publications/outcomes.
6. **Publications & Manuscripts**: Refereed journal papers, preprints, and manuscripts in preparation with full citations.
7. **Open Source Leadership**: Maintainer duties, scale of contributions (commits, PRs, contributors), architecture (anti-spam, CI/CD, bot automation).
8. **Technical Projects**: Key full-stack, ML, and software projects with live/code links and key technical bullet points.
9. **Technical Skills**: Programming languages, ML frameworks, web tech, databases, GIS tools, DevOps.
10. **Awards & Achievements**: Competitions, ambassador roles, hackathon finishes, competitive programming stars.
11. **Leadership & Service**: ACM Publicity Chair, IETE Coordinator, Class Representative, Buildathon Team Lead, SIH Team Lead.
12. **Academic Exposure & Visits**: TCG CREST Quantum Lab visit, CTRLS Data Centre visit, DRDO workshop exposure.
13. **Certifications**: Official certifications from HCL GUVI, MoE, DevTown.
14. **Languages**: Multilingual proficiency (English, Bengali, Hindi, German).

---

## 6. Compilation & Quality Guarantee
- 100% `pdflatex` compilation without warnings.
- Zero overfull/underfull `\hbox` warnings.
- No dependency on template packages (`moderncv.cls`, `awesome-cv.cls`, `altacv.cls`).
