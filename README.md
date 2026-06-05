# MarzaBIM

**IFC-native BIM reconstructions of the Etruscan urban settlement of Marzabotto (ancient Kainua, Italy, 6th–4th century BCE). Open archaeological dataset produced at CNR-ISPC using Bonsai/BlenderBIM and IfcOpenShell.**

> Part of an open digital archaeology framework for ancient Kainua. For the associated GIS data of the settlement, see [MarzaGIS](https://github.com/gmancuso24/MarzaGIS).

---

## Overview

MarzaBIM provides semantically structured three-dimensional reconstructions of the built environment of Kainua/Marzabotto, one of the best-preserved Etruscan urban sites in Italy. The models are authored natively in IFC (Industry Foundation Classes) and are designed as an open, reusable archaeological dataset rather than a visualisation product.

The repository is organised following the topographic structure of the site: regiones, insulae, and the acropolis. Each spatial unit is documented in its own folder with a dedicated `README.md` describing sources, modelling choices, and limitations.

---

## Repository structure

```
MarzaBIM/
├── 1_regio/               # Regio I (in progress)
├── 4_regio/               # Regio IV
│   ├── 1_insula/          # Insula 1
│   └── 2_insula/          # Insula 2
├── acropoli/              # Acropolis area
├── analysis/              # Jupyter notebooks for IFC data analysis
├── utility/
│   ├── .venv/             # Python 3.14 virtual environment (git-ignored)
│   ├── requirements.txt   # Python dependencies
│   └── textures/          # Shared texture assets
└── README.md
```

Each subfolder containing data includes its own `README.md` with context-specific documentation (sources, phasing, modelling conventions).

---

## Data and methods

- **Format:** IFC 2x3 / IFC 4 (open BIM standard)
- **Authoring tools:** [Bonsai/BlenderBIM](https://bonsaibim.org/), [IfcOpenShell](https://ifcopenshell.org/)
- **Coordinate system:** aligned with MarzaGIS (EPSG:32632 / WGS 84 / UTM zone 32N)
- **Chronological scope:** 6th–4th century BCE (Etruscan urban phase)
- **Semantic structure:** IFC spatial hierarchy (`IfcSite` → `IfcBuilding` → `IfcBuildingStorey` → `IfcSpace`); property sets document archaeological phasing and source references

The `analysis/` folder contains Jupyter notebooks (Python / IfcOpenShell) for quantitative queries on the IFC models: surface areas, volumes, element counts, and stratigraphic relationships.

A shared Python 3.14 virtual environment is maintained in `utility/.venv/`. To activate it and install dependencies:

```bash
source utility/.venv/bin/activate
pip install -r utility/requirements.txt
```

---

## Related resources

| Repository | Content |
|---|---|
| [MarzaGIS](https://github.com/gmancuso24/MarzaGIS) | GIS data for the Marzabotto/Kainua settlement (QGIS, GeoPackage) |

---

## Cite

If you use this dataset, please cite it as:

> Mancuso, G. (CNR-ISPC). *MarzaBIM: IFC-native BIM reconstructions of ancient Kainua (Marzabotto)*. GitHub. [URL]

A citable release with DOI will be issued via Zenodo following the first stable version.

---

## Licence

Data and models: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)  
Code (notebooks, scripts): [MIT Licence](LICENSE)

Individual models may carry a more specific licence expressed in the `LICENSE` file within their respective folder.

---

## Contact

Giacomo Mancuso — CNR, Istituto di Scienze del Patrimonio Culturale (ISPC)  
giacomo.mancuso@cnr.it
