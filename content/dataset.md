---
title: Dataset
nav: Dataset
---

<!-- {% include figure.html img="data_sponsor.png" %} -->

# Background on the Dataset
The dataset that will be used for this hackathon is a stem cell differentiation to cardiomyocytes with samples collected every day during the differentiation starting at the day cells were plated (Day -2) and ending with cardiomyocytes (Day 14). Day 0 indicates the start of the differentiation. The cells were differentiated using the [StemCell Technologies Ventricular Cardiomyocyte Differentiation kit](https://www.stemcell.com/products/stemdiff-cardiomyocyte-kit.html). Samples were fixed on the day of collection and then processed together with combinatorial indexing using Scale Biosciences technology.


{% include figure.html img="Experimental_Design.png" alt="Experimental Design" width="100%" %}


This data contains three stem cells lines (FSA0024I1, IST2607K3, WAB0137L8) that were cultured using a village platform meaning that all lines were cultured in the same dish and demultiplexed following sequencing by matching the genetic information in the sequencing reads to genotype data for each cell line. Each line is well represented across the days of differentiation:

{% include figure.html img="2024_hackathon_cell_line_time.png" alt="Experimental Design" width="100%" %}


## Details about the data metadata
This dataset only has a few different metadata fields. This icludes:
- **nCount_RNA**: Number of UMIs identified per cell
- **nFeature_RNA**: Number of unique features (genes) expressed per cell
- **Barcode**: Cell  barcode
- **CellLine**: The cell line that cell is from (FSA0024I1, IST2607K3 or WAB0137L8)
- **Day**: The collection day each cell was collected and fixed
- **Sex**: The sex of the donor that the iPSC line was generated from

| orig.ident |     nCount_RNA |      nFeature_RNA |   Barcode | CellLine |       Day | Sex |
| --- | --- | --- | --- | --- | --- | --- |
| SeuratProject |  6642.99981199999 |        3462 |   AAACCATAGGCAGGTCCGTAGGTCAGCTT |   WAB0137L8 |      Day-1 | Female |
| SeuratProject |  17163.0002339001 |        6789 |   AAACCATAGGCAGGTCCGTTAAGTCCTGA |   WAB0137L8 |      Day-1 | Female |
| SeuratProject |  11131.0002034 |   5248 |   AAACCATAGGCAGGTCCGTTCCGGCTTAT |   FSA0024I1 |      Day-1 | Female |
| SeuratProject |  18820.0002576 |   6886 |   AAACCATAGTCAACGTAAGAGCCGTAGTT |   FSA0024I1 |      Day-1 | Female |
| SeuratProject |  15492.0002927 |   6469 |   AAACTCCAAACGCGAGATTGTAGCAGCTA |   WAB0137L8 |      Day-1 | Female |
| SeuratProject |  15993.0000964 |   6711 |   AAACTCCAAGCAGGTCCGTCCGCTAAGAG |   WAB0137L8 |      Day-1 | Female |
| SeuratProject |  20849.0000901 |   7491 |   AAATCGTTCGCAGGTCCGTACGGCGTTAA |   WAB0137L8 |      Day-1 | Female |
| SeuratProject |  41359.9987672 |   9909 |   AAATTCCTCACGCGAGATTGTAGGCTGCA |   WAB0137L8 |      Day-1 | Female |
| SeuratProject |  23723.999869 |    8025 |   AAATTCCTCGCAGGTCCGTTATTGCTGGA |   WAB0137L8 |      Day-1 | Female |


# Accessing the Dataset
The provided data has been demultiplexed with doublets removed resulting in 19,663 cells. The cell line labels for each cell is provided in the cell metadata sections of the provided objects and the ``2024_hackathon_cell_metadata.tsv`` file. All data can be found in [this directory](https://www.dropbox.com/scl/fo/8659cnxbw6z5e3vmqshoc/ABvKcjHLiAzMwQ0c6LY9t3E?rlkey=5alw8fzrqqqypyy4cw5qsxqs0&dl=0). Links to individual data structure files so you can use download bash commands if desired:

- **Seurat rds**: [https://www.dropbox.com/scl/fi/4h1sangqmm8se9urcuuqx/2024_hackathon_seuratv5.rds?rlkey=b7wpmhxpbszn7n9f487b4pylr&st=ddz024uo](https://www.dropbox.com/scl/fi/4h1sangqmm8se9urcuuqx/2024_hackathon_seuratv5.rds?rlkey=b7wpmhxpbszn7n9f487b4pylr&st=ddz024uo)
- **SCE rds**: [https://www.dropbox.com/scl/fi/6bqlblz52u6iqn66kgkab/2024_hackathon_sce.rds?rlkey=veuafta6bml31gagcxwcf8w7s&st=vhx9dskd](https://www.dropbox.com/scl/fi/6bqlblz52u6iqn66kgkab/2024_hackathon_sce.rds?rlkey=veuafta6bml31gagcxwcf8w7s&st=vhx9dskd)
- **AnnData h5ad**: [https://www.dropbox.com/scl/fi/luu05po55sd53emlbi8d0/2024_hackathon_anndata.h5ad?rlkey=3x10o6m5mt5bqqyk017m3jbct&st=b26cmacz](https://www.dropbox.com/scl/fi/luu05po55sd53emlbi8d0/2024_hackathon_anndata.h5ad?rlkey=3x10o6m5mt5bqqyk017m3jbct&st=b26cmacz)
- **Folder with matrix mtx, features and barcodes**: [https://www.dropbox.com/scl/fo/0sa41vt2zm0nv8x84x4tz/AN9j8A1jrA65UiwYu3sQ60s?rlkey=p4h0ifxcl79dfcltdo62g48k1&st=l2mqbdcd](https://www.dropbox.com/scl/fo/0sa41vt2zm0nv8x84x4tz/AN9j8A1jrA65UiwYu3sQ60s?rlkey=p4h0ifxcl79dfcltdo62g48k1&st=l2mqbdcd)
- **Cell metadata**: [https://www.dropbox.com/scl/fi/3gb74lrr8f4fyqkgzmcii/2024_hackathon_cell_metadata.tsv?rlkey=r4f7m3oiv90pqimxl2pm91ijn&st=8qclg284](https://www.dropbox.com/scl/fi/3gb74lrr8f4fyqkgzmcii/2024_hackathon_cell_metadata.tsv?rlkey=r4f7m3oiv90pqimxl2pm91ijn&st=8qclg284)

We recommend downloading these before the hackathon and doing some quick preliminary assessments to make sure you have a good grasp on the data structure.


# Oz Single Cell 2024 Github Organisation
We have generated a [github organisation](https://github.com/Oz-Single-Cell-2024-Hackathon) specifically for this hackathon so all code for each project can be stored in a central location. You should have received an invitation to join the [Oz Single Cell 2024 Github Organisation](https://github.com/Oz-Single-Cell-2024-Hackathon) but if you didn't receive it please email d.neavin @ garvan.org.au. Create a repo within the organisation to store all code and scripts and get hacking!