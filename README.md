# Exact degree and real-point counts in a localized sector of quantum Levi-Civita connections on (Z2)^4

Marius Torsheim — a computer-assisted classification of a marked path-triangle sector.

This repository contains article revision **0.13**, computational supplement **2.3**, literature comparison **1.2**, and the exact code, data and certificates required for reproduction.

## Read the work

- [Article PDF](Quantum_Gravity_QLC_Article.pdf)
- [Written computational supplement PDF](Quantum_Gravity_QLC_Supplement.pdf)
- [Complete scientific source, code and data archive](Quantum_Gravity_QLC_Computational_Supplement.zip)

The archive preserves the complete `qlc_release/` directory and all **319 scientific package files**. Its internal `SHA256SUMS.txt` checks the other 318 files. It includes all editable manuscript/supplement sources, `audit/`, `certificates/`, `sections/`, pinned dependencies, a worked connection, the literature comparison and fresh execution records. Author submission forms and internal review dossiers are excluded.

## Mathematical scope

The declared marked, spatially homogeneous, trace-zero localized path-triangle sector has generic complex degree **512**. At q = (4/3, 12/11, 3/4), with all four scales one, the declared fibre consists of **512 distinct reduced complex points**, exactly **204 of which are real** and reconstruct the specified star-preserving quantum Levi-Civita connections.

The marking, support and localization are retained. This is a classification of the stated sector, without a symmetry quotient or a claim about the full moduli space. Curvature and cosmology belong to a separate project. The literature report identifies the inspected versions and the remaining limits, including the uninspected final square journal version.

## Reproduce

Clone or download this repository, then extract the scientific archive. The following commands use Python 3.10 or later and a POSIX shell:

```sh
python3 -m zipfile -e Quantum_Gravity_QLC_Computational_Supplement.zip .
python3 -m venv .venv
. .venv/bin/activate
python -m pip install -r qlc_release/requirements.txt
cd qlc_release
python -B reproduce.py --output ../qlc-results
```

The pinned dependencies are `python-flint==0.9.0`, `sympy==1.14.0` and `mpmath==1.3.0`. The output directory must be new. After dependency installation, reproduction needs no network access. The complete command checks source consistency, runs the 20 counting jobs in both normal and optimized Python modes, compares 28 mathematical result pairs, and replays the worked real connection.

The recorded complete run used Python 3.12.14. The execution records distinguish that run from subsequent documentation-only source changes. Exact arithmetic certificates and written arguments, rather than status labels or hash values alone, support the mathematical claims.

After extraction, verify the scientific files with:

```sh
cd qlc_release
sha256sum --check SHA256SUMS.txt
```

See the extracted `qlc_release/README.md` and `REPRODUCTION_RESULTS.md` for the proof/data map and replay scope. Rebuilding the PDFs requires a LaTeX installation with the packages specified by their sources.

## Citation and status

Citation metadata are in [CITATION.cff](CITATION.cff). No DOI or ORCID has been assigned here. Remaining journal formalities are separate from this repository; it does not indicate acceptance or external journal peer review. The manuscript discloses the actual scope of AI assistance and author oversight.
