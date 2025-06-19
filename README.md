# scRNA-seq Analysis of Pancreatic Cancer Liver Metastasis

This is a Seurat-based single-cell RNA-seq analysis pipeline. The project reproduces and extends findings from Zhang et al. (2023, Nat Commun) to explore the cellular landscape and immunosuppressive microenvironment in pancreatic cancer liver metastasis.

## 📁 Structure

```
scRNAseq-pdac-project/
├── scripts/                   # R scripts for Seurat, CellChat, Slingshot
├── data/                      # Raw and processed data (GSE197177)
├── results/
│   ├── plots/                 # Figures for clustering, signaling, pseudotime
│   └── tables/                # Marker gene lists, annotations
├── markdown/                  # Project report and notes
├── envs/                      # Conda environments or R libraries
├── .gitignore
└── README.md
```

## 🔁 Workflow Steps
1. **Quality Control**  
   - Filtering by gene/cell count, mitochondrial content

2. **Doublet Detection**  
   - DoubletFinder to remove artificial multiplets

3. **Batch Correction & Integration**  
   - Harmony for dataset integration across tissue types

4. **Cell Type Annotation**  
   - SingleR + manual annotation using canonical markers

5. **Cell–Cell Communication**  
   - CellChat to infer signaling networks between cell types

6. **Pseudotime Analysis**  
   - Slingshot to reconstruct lineage and differentiation paths

## 🚀 Run
```r
# Run main Seurat pipeline
source("scripts/seurat_pipeline.R")
```

## 👤 Author

**Wenshou He**  
GitHub: [@VHE888](https://github.com/VHE888)  
Boston University - Bioinformatics MSc
