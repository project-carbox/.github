# Project Carbox

**Macromolecular Crystallographic Validation, Anomalous Carboxyl Protonation, and Low-Barrier Hydrogen Bond (LBHB) Analysis**

- Web Portal: [https://project-carbox.github.io/](https://project-carbox.github.io/)
- Documentation: [https://project-carbox.readthedocs.io/en/latest/](https://project-carbox.readthedocs.io/en/latest/)
- 3D Workbench: [https://carboxmol.github.io](https://carboxmol.github.io)
- Contact: [suleyman.hacizade1@gmail.com](mailto:suleyman.hacizade1@gmail.com)

---

## Private Data and Repository Access Notice

**English:** All raw crystallographic datasets, 7,230-PDB screening matrices, $2mF_o - DF_c$ and $mF_o - DF_c$ electron density correlation profiles, backend computational pipelines (`carbox`), research notes, and pre-publication manuscripts in `project-carbox/carbox` are private.

**Azərbaycanca:** Bu təşkilatdakı bütün xam kristalloqrafik məlumat bazaları, 7,230 PDB strukturu üzrə tam skrininq matrisaları, elektron sıxlığı korrelyasiya xəritələri, əsas hesablama boru xətləri (`carbox`) və elmi əlyazmalar məxfidir (private).

**Access Requests:** Researchers, academic reviewers, and collaborators wishing to request access to the private core repository or raw datasets may contact:  
**[suleyman.hacizade1@gmail.com](mailto:suleyman.hacizade1@gmail.com?subject=Access%20Request%20-%20Project%20Carbox%20Private%20Data%20%26%20Repository)**

---

## Official Documentation (Read the Docs)

Scientific guides, REFMAC5 and Servalcat restraint specifications, crystallographic validation memoranda, and API documentation are published on Read the Docs:

- [https://project-carbox.readthedocs.io/en/latest/](https://project-carbox.readthedocs.io/en/latest/) (English `en`, Azerbaijani `az`, Hebrew `he`)

---

## Organization Repositories

| Repository | Visibility | Description | Link |
| :--- | :--- | :--- | :--- |
| [**carbox**](https://github.com/project-carbox/carbox) | Private (By Request) | Euclidean contact mining ($d(\mathrm{O}\cdots\mathrm{O}) \le 3.20\text{ \AA}$), Tukey IQR B-factor filter, Fisher $z$-transformed RSCC validation, empirical pKa solver, and 70-cation metal coordination audit. | [Request Access](mailto:suleyman.hacizade1@gmail.com?subject=Access%20Request%20-%20Project%20Carbox%20Private%20Repository) |
| [**carbox-docs**](https://github.com/project-carbox/carbox-docs) | Public | Sphinx documentation sources and multilingual crystallographic validation manuals for Read the Docs. | [GitHub](https://github.com/project-carbox/carbox-docs) · [Read the Docs](https://project-carbox.readthedocs.io/en/latest/) |
| [**project-carbox.github.io**](https://github.com/project-carbox/project-carbox.github.io) | Public | Public web portal presenting the 4-stage validation methodology, interactive 3D structure viewer, and benchmark tables. | [project-carbox.github.io](https://project-carbox.github.io/) |

---

## Methodology Overview

In macromolecular crystallography, side-chain carboxylates (Asp, Glu) in flexible surface loops can be refined into close proximity ($d \le 2.50\text{ \AA}$) without supporting experimental electron density.

> *"If there is no electron density for atoms, they are mismodeled. If atoms are mismodeled, the distance between them is completely meaningless."*  
> — Prof. Garib N. Murshudov, MRC Laboratory of Molecular Biology, Cambridge

Carbox addresses false-positive short contacts through a four-stage validation protocol:

1. **Stage 1 — Geometric Contact Mining and Solvent Burial:** Extracts inter-residue Asp/Glu oxygen pairs with $d(\mathrm{O}_i, \mathrm{O}_j) \le 3.20\text{ \AA}$ (short LBHB regime $\le 2.55\text{ \AA}$) and evaluates dielectric shielding via nearest water exclusion ($d_{\text{water}} > 3.00\text{ \AA}$, $\varepsilon \approx 2\text{--}4$).
2. **Stage 2 — Non-Parametric B-Factor and Electron Density Filtering:** Excludes thermally disordered residues using Tukey IQR fences ($B > Q_3 + \alpha \cdot \text{IQR}$) and verifies experimental density support using Fisher $z$-transformed RSCC ($z = \frac{1}{2}\ln\frac{1+\text{CC}'}{1-\text{CC}'}$, $Z_{\text{score}} \ge -3.0$), combined with a 70-metal coordination screen.
3. **Stage 3 — Biochemical Protonation Verification:** Evaluates proton retention at physiological pH via upward $\mathrm{p}K_a$ shifts ($\Delta \mathrm{p}K_a \ge +2.0$, local $\mathrm{p}K_a \ge 6.5\text{--}10.2$).
4. **Stage 4 — Benchmark Calibration:** Validation against reference atomic-resolution crystal structures (`1KZK` HIV-1 Protease, `1OEW` Endothiapepsin, `2DSX` Rubredoxin, `1FKN` BACE-1, `4ZM7` Aminopeptidase).

---

## Companion Software

- [CarboxMol Organization (`github.com/carboxmol`)](https://github.com/carboxmol): 3D macromolecular crystallography workbench, desktop GUI, and CLI.
- [CarboxMol Web Studio (`carboxmol.github.io`)](https://carboxmol.github.io): Browser-based 3D crystallographic inspection and electron density contouring.

---

## Authors and Contact

- **Suleiman M. Hajizadeh**  
  Institute of Molecular Biology, Ministry of Science and Education of the Republic of Azerbaijan; Western Caspian University, Baku, Azerbaijan
- **Prof. Garib N. Murshudov**  
  MRC Laboratory of Molecular Biology (LMB), Cambridge Biomedical Campus, Cambridge, United Kingdom
- **Documentation:** [https://project-carbox.readthedocs.io/en/latest/](https://project-carbox.readthedocs.io/en/latest/)
- **Web Portal:** [https://project-carbox.github.io/](https://project-carbox.github.io/)
- **Contact:** [suleyman.hacizade1@gmail.com](mailto:suleyman.hacizade1@gmail.com)
