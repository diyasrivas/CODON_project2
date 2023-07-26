# CODON_project2

## Joint analysis of gene expression and DNA accessibility in B-cell lymphoma ##

## Background: ##
Diffuse B-cell lymphoma is a type of blood cancer affecting B cells and
involves epigenetic dysregulation of normal gene expression programs. New assays such as
the 10x Genomics multiome enable simultaneous measurement of gene expression and
DNA accessibility within cells. This can allow us to both identify tumor cells from a
heterogeneous blood sample, and to investigate the gene regulatory networks active in
healthy and cancerous cells. In this project, we will analyse a dataset of ~14,000 nuclei
collected from a patient with diffuse B-cell lymphoma by 10x Genomics and profiled using
the multiome kit, resulting in genome-wide DNA accessibility profiles paired with gene
expression measurements. We will group cells according to both their DNA accessibility and
gene expression patterns, identify ATAC-seq peaks that may regulate key cell-type marker
genes, and visualize DNA accessibility patterns among the cells.

Referenced paper: https://pages.10xgenomics.com/rs/446-PBO-704/images/10x_LIT000110_Data_Spotlight_Multiome_digital.pdf

Highlights:
• Distinguish tumor versus normal cells in a heterogeneous sample
• Reconstruct cell type–specific gene regulatory network
• Confirm PAX5 as a critical regulator specific to tumor B cells
• Identify putative target genes downstream of PAX5

Data source:
https://support.10xgenomics.com/single-cell-multiome-atac-gex/datasets/1.0.0/lymph_node_lymphoma_14k

File downloaded:
lymph_node_lymphoma_14k_filtered_feature_bc_matrix.h5

Capstone presentation: https://itssastar-my.sharepoint.com/:p:/r/personal/diyasri_gis_a-star_edu_sg/Documents/Presentation2.pptx?d=wb2b99457adbe4064811fecbc9c5693ca&csf=1&web=1&e=unxmp8

## Tasks: ##
1. Create a seurat object containing the RNA data and metadata
2. Add the ATAC data as another assay in the Seurat object
3. Normalize the gene expression data and perform QC
4. Run PCA and create a UMAP plot using the gene expression data
5. Add gene annotation information to the ATAC assay
6. Run LSI and UMAP using the ATAC assay
7. Create a joint UMAP and clustering using both the RNA and ATAC data
8. Find gene expression markers for each cluster of cells
9. Plot the top unique marker genes for each cluster
10. Annotate the tumor cells
11. Link ATAC peaks to the top marker genes
12. Plot DNA accessibility and gene expression for some of the marker genes
