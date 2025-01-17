# INSPIRE

*INSPIRE: interpretable, flexible and spatially-aware integration of multiple spatial transcriptomics datasets from diverse sources*

An effective and efficient method for joint analyses of multiple spatial transcriptomics datasets.

![INSPIRE\_pipeline](demo/overview.jpg)

We develop INSPIRE, a deep learning-based method for integrating and interpreting multiple spatial transcriptomics (ST) datasets from diverse sources. It integrates information across slices in a shared latent space, where meaningful biological variations from the input slices are preserved, while complex unwanted variations are eliminated. Utilizing this shared latent space, INSPIRE achieves an integrated NMF on gene expressions across slices, decomposing biological signals in different slices into consistent and interpretable spatial factors with associated gene programs. These inferred spatial factors often correspond to distinct cell populations and biological processes within the analyzed tissues.

INSPIRE takes gene expression count matrices and spatial coordinates from multiple ST slices as input, and generates three key outputs: latent representations of cells or spatial spots, non-negative spatial factors for cells or spatial spots, and non-negative gene loadings shared among datasets.

By integrating multiple ST datasets with INSPIRE, users can:
* Identify spatial trajectories and major spatial regions consistently across datasets using latent representations of cells or spatial spots.
* Reveal detailed tissue architectures, spatial distributions of cell types, and organizations of biological processes in tissues across slices using non-negative spatial factors of cells or spatial spots.
* Detect spatially variable genes, identify gene programs associated with specific spatial architectures in tissues, and conduct pathway enrichment analysis using non-negative gene loadings.

## Installation
* INSPIRE can be downloaded from GitHub:
```bash
git clone https://github.com/jiazhao97/INSPIRE.git
cd INSPIRE
conda env update --f environment.yml
conda activate INSPIRE
```

## Usage and reproducibility

In our manuscript, we demonstrate that INSPIRE is applicable to a range of biologically significant integrative analysis scenarios:
* Integration of multiple ST slices from biological replicate samples, leveraging information across slices to enhance the accuracy of downstream analysis.
* Integration of multiple ST slices offering complementary views of complex tissue, where spatial structures only partially overlap, to construct a comprehensive spatial atlas.
* Integration of multiple ST slices from distinct ST technologies, harnessing the unique strengths of each to deepen biological insights.
* Integration of multiple whole-embryo ST slices collected across various developmental stages to unravel complex dynamic changes during embryonic development.
* Integration of multiple adjacent ST slices along an axis to reconstruct 3D structures of organs or entire organisms, offering deeper insights beyond traditional 2D analyses.

We provide tutorials and codes for reproducing the experiments of our paper at [this tutorial website](https://inspire-tutorial.readthedocs.io/en/latest/index.html#).

## Development
### Building locally with hatch
First make sure that the right tools are installed:
```bash
pip install hatch
pip install keyrings.alt
```
Then build with hatch:
```
hatch build
```

## Reference

Jia Zhao, Xiangyu Zhang, Gefei Wang, Yingxin Lin, Tianyu Liu, Rui B. Chang, Hongyu Zhao. INSPIRE: interpretable, flexible and spatially-aware integration of multiple spatial transcriptomics datasets from diverse sources. Preprint. 2024. [https://doi.org/10.1101/2024.09.23.614539](https://doi.org/10.1101/2024.09.23.614539).
