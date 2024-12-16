# ECBME4060-Project
Single cell sets GSE179633 and GSE174188 were retrieved from the Gene Expression Omnibus (GEO), and were read into a python environment utilizing scanpy’s 10x-Genomics and h5ad reading tools, respectively. Five SLE samples, five healthy samples from GSE179633, and a sample of 120000 cells from both SLE and healthy samples in GSE174188 were utilized in downstream analysis. For the purposes of the analysis, two distinct filtering procedures were used: T cells were selected by filtering for cells expressing CD3D, and B cells were selected by filtering for cells expressing MS4A1. Genes with mean expression in the lower 50th percentile were excluded for each set of cells to reduce computational complexity. Principal component analysis was performed on normalized and logarithmized counts. Leiden clusters and UMAP plots were generated with results of PCA, with the experimental groups (SLE, healthy) being included as metadata. Differentially expressed genes between SLE and healthy cells were determined with scanpy’s rank_genes_groups function, and the top four genes ordered by each gene’s t-statistic were plotted. For B cell groups, the differentially expressed genes for each leiden cluster were determined using the same method, and each cluster was annotated with its corresponding top three genes (B.geneAgeneBgeneC).

# lupus_skin.ipynb
Contains all downstream analysis of single-cell data from GSE179633.

# lupus_blood.ipynb
Contains all downstream analysis of single-cell data from GSE174188.
