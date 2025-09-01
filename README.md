# scExtract: Automated Single-cell RNA-seq Analysis

This project replicates a portion of the workflow described in the paper:

**scExtract: Leveraging large language models for fully automated single-cell RNA-seq data annotation and prior-informed multi-dataset integration**  
Published in Genome Biology (2025)

GitHub Repository: [scExtract GitHub](https://github.com/IGVF/single-cell-pipeline)  
DOI: [https://doi.org/10.1186/s13059-025-03639-x](https://doi.org/10.1186/s13059-025-03639-x)

## Workflow Components
- **FastQC**: Quality control of FASTQ reads  
- **STARsolo**: Alignment and gene quantification  
- **Scanorama-prior**: Prior-informed batch correction  
- **cellhint-prior**: Cell type annotation using LLMs  
- **Seurat**: Downstream clustering and visualization  

## Input Data
Sample: SRR11680207 (Human PBMC single-cell RNA-seq)  
Data accessed via NCBI SRA

## Directory Structure
```
/data              # Contains the FASTQ files (SRR11680207)
/workflow          # Contains Snakemake/Nextflow scripts to run the pipeline
questions.yaml     # Questions to evaluate pipeline outputs
answers.yaml       # Ground-truth answers
metadata.yaml      # Metadata including paper DOI and tools used
data_access.txt    # Instructions to access the data
```

To replicate the pipeline, run the `workflow` on the dataset in `/data` and answer the questions.