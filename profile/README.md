<div align="center">
  <a href="https://project-carbox.github.io/">
    <img src="https://raw.githubusercontent.com/project-carbox/project-carbox.github.io/main/assets/carbox_logo.svg" alt="Carbox Logo" width="160"/>
  </a>
  <br/><br/>

  <h1>Welcome to Project Carbox ⚛️🧬</h1>
  <p align="center">
    <strong>High-Throughput Macromolecular Crystallographic Validation, Anomalous Carboxyl Protonation &amp; Low-Barrier Hydrogen Bond (LBHB) Discovery Platform</strong>
  </p>

  <p align="center">
    <a href="https://project-carbox.github.io/"><img src="https://img.shields.io/badge/Live_Portal-project--carbox.github.io-00e5ff?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Live Showcase"/></a>
    <a href="https://carboxmol.github.io"><img src="https://img.shields.io/badge/3D_Studio-carboxmol.github.io-10b981?style=for-the-badge&logo=webgl&logoColor=white" alt="CarboxMol Studio"/></a>
    <a href="mailto:suleyman.hacizade1@gmail.com?subject=Private%20Data%20%26%20Repository%20Access%20Request%20-%20Project%20Carbox"><img src="https://img.shields.io/badge/Private_Data_Access-Request_via_Email-dc2626?style=for-the-badge&logo=gmail&logoColor=white" alt="Request Access"/></a>
    <a href="mailto:suleyman.hacizade1@gmail.com"><img src="https://img.shields.io/badge/Contact-suleyman.hacizade1%40gmail.com-7c3aed?style=for-the-badge&logo=gmail&logoColor=white" alt="Contact"/></a>
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Crystallography-MRC--LMB_&_IMB-0284c7?style=flat-square" alt="MRC-LMB & IMB"/>
    <img src="https://img.shields.io/badge/PDB_Screened-7,230_Structures_(≤1.20_Å)-6366f1?style=flat-square" alt="7,230 Structures"/>
    <img src="https://img.shields.io/badge/Validated_Benchmarks-67_Golden_LBHBs-10b981?style=flat-square" alt="67 Benchmarks"/>
    <img src="https://img.shields.io/badge/Quality_Control-Tukey_IQR_+_Fisher_Z_RSCC-f59e0b?style=flat-square" alt="Tukey IQR + Fisher Z"/>
    <img src="https://img.shields.io/badge/Version-v0.4.5-ec4899?style=flat-square" alt="v0.4.5"/>
  </p>
</div>

---

> [!IMPORTANT]
> ### 🔒 Private Data & Repository Access Notice (Məxfi Məlumatlar və Giriş İcazəsi)
> **English:** All raw crystallographic datasets, full 7,230-PDB screening matrices, complete $2mF_o - DF_c$ and $mF_o - DF_c$ electron density correlation profiles, backend computational pipelines (`carbox`), persistent LLM research wiki notes, and pre-publication LaTeX manuscripts housed in **`project-carbox/carbox`** are **strictly private**.
>
> **Azərbaycanca:** Bu təşkilatdakı bütün xam kristalloqrafik məlumat bazaları, 7,230 PDB strukturu üzrə tam skrininq matrisaları, elektron sıxlığı korrelyasiya xəritələri, əsas hesablama boru xətləri (`carbox`), elmi dissertasiya/məqalə əlyazmaları və daxili bilik bazası **məxfidir (private)**.
>
> **How to Request Access / Giriş üçün Müraciət:** If you are a researcher, academic reviewer, or collaborator and wish to request access to the private core repository or raw research datasets, please apply via email (Əgər tədqiqat məlumatlarına və ya qapalı repozitoriyaya giriş əldə etmək istəyirsinizsə, elektron poçt vasitəsilə müraciət edə bilərsiniz):  
> 📧 **[suleyman.hacizade1@gmail.com](mailto:suleyman.hacizade1@gmail.com?subject=Access%20Request%20-%20Project%20Carbox%20Private%20Data%20%26%20Repository)**

---

## 🏛️ Organization Architecture & Data Governance

To uphold scientific rigor and protect sensitive pre-publication crystallographic datasets, **Project Carbox** is partitioned into two dedicated repositories:

```text
project-carbox
│
├── 🔒 carbox (Private Core Backend & Research Engine — Access by Request)
│   ├── High-throughput Euclidean contact mining engine (Asp/Glu d(O···O) ≤ 3.20 Å)
│   ├── Non-parametric Tukey IQR B-factor outlier filter (Q3 + α·IQR, α ∈ {1.5, 3.0})
│   ├── Real-Space Correlation Coefficient (RSCC) & Fisher z-transformation via Gemmi
│   ├── Clean-room empirical pKa perturbation solver (ΔpKa ≥ +2.0) & 70-cation metal audit
│   ├── Full 7,230-structure screening tables, validation CSVs, and REFMAC5/Servalcat restraints
│   ├── Persistent LLM Research Wiki (19+ interlinked notes) & LaTeX manuscripts
│   └── 📩 Request Access: suleyman.hacizade1@gmail.com
│
└── 🌐 project-carbox.github.io (Public Interactive Showcase Portal)
    ├── 🌟 Live URL: https://project-carbox.github.io/
    ├── Interactive 4-Stage Methodology stepper (Prof. Garib N Murshudov's protocol)
    ├── In-browser 3Dmol.js WebGL molecular viewer (1KZK, 1OEW, 2DSX, 1FKN)
    ├── Searchable & filterable 10–20 Golden Benchmarks calibration table
    └── Public citation records (BibTeX) and documentation overview
```

---

## 🔬 Scientific Mission & The 4-Stage Protocol

In standard macromolecular crystallography, side-chain carboxylates (Asp, Glu) in flexible loops can be artificially refined into close proximity ($d \le 2.50\text{ \AA}$) without supporting electron density.

> *"If there is no electron density for atoms, they are mismodeled. If atoms are mismodeled, the distance between them is completely meaningless."*  
> — **Prof. Garib N Murshudov** (*MRC Laboratory of Molecular Biology, Cambridge*)

**Carbox** solves this false-positive hazard via a 4-stage validation gate:
1. **Stage 1 — Geometric Contact Mining & Solvent Burial:** Extracts inter-residue Asp/Glu pairs with $d(O_i, O_j) \le 3.20\text{ \AA}$ (ultra-short LBHB regime $\le 2.55\text{ \AA}$) and evaluates dielectric shielding via nearest water exclusion ($d_{\text{water}} > 3.00\text{ \AA}$, $\varepsilon \approx 2\text{--}4$).
2. **Stage 2 — Non-Parametric B-Factor & Electron Density Pruning:** Eliminates thermally disordered loops using **Tukey IQR fences** ($B > Q_3 + \alpha \cdot \text{IQR}$) and verifies direct experimental density agreement using **Fisher $z$-transformed RSCC** ($z = \frac{1}{2}\ln\frac{1+\text{CC}'}{1-\text{CC}'}$, $Z_{\text{score}} \ge -3.0$), alongside a 70-metal coordination screen.
3. **Stage 3 — Biochemical Protonation Verification (PROPKA):** Confirms thermodynamic proton trapping at physiological pH via upward $\text{p}K_a$ shifts ($\Delta \text{p}K_a \ge +2.0$, local $\text{p}K_a \ge 6.5\text{--}10.2$).
4. **Stage 4 — The 10–20 Golden Benchmarks Calibration:** Manual verification against celebrated atomic-resolution structures (**`1KZK`** HIV-1 Protease, **`1OEW`** Endothiapepsin, **`2DSX`** Rubredoxin, **`1FKN`** BACE-1, **`4ZM7`** Aminopeptidase) prior to global PDB scaling.

---

## 🔗 Companion Ecosystem

- 🖥️ **[CarboxMol Organization (`github.com/carboxmol`)](https://github.com/carboxmol):** The 3D macromolecular crystallography workbench, desktop GUI, CLI, and Progressive Web App (PWA) Studio.
- 🌐 **[CarboxMol Live Web Studio (`carboxmol.github.io`)](https://carboxmol.github.io):** Interactive 3D crystallographic modeling and real-time electron density contouring in any browser.

---

## 👨‍🔬 Scientific Leadership & Contact

- **Lead Researcher:** Suleiman M Hajizadeh  
  *Institute of Molecular Biology, Ministry of Science and Education of the Republic of Azerbaijan*  
  *Western Caspian University, Baku, Azerbaijan*
- **Scientific Advisor & Co-Author:** Garib N Murshudov  
  *MRC Laboratory of Molecular Biology (LMB), Cambridge Biomedical Campus, Cambridge, United Kingdom*
- **Data & Repository Access Requests:** 📧 **[suleyman.hacizade1@gmail.com](mailto:suleyman.hacizade1@gmail.com?subject=Access%20Request%20-%20Project%20Carbox%20Private%20Data)**
- **Locations:** Baku, Azerbaijan · Cambridge, United Kingdom

---

<div align="center">
  <sub>© 2026 Suleiman M Hajizadeh &amp; Garib N Murshudov · Project Carbox</sub>
</div>
