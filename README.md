# CHASMplus

## About

Sequencing studies have statistically implicated genetic drivers of human cancers by distinguishing these from the expected random accumulation of somatic mutations. However, prior work has coarsely focused on driver genes or regions, largely avoiding prediction of individual mutations. Here, we develop and rigorously validate CHASMplus to predict individual driver somatic missense mutations and show it exceeds state-of-the-art performance. Applied to 32 cancer types, CHASMplus identifies 3,527 unique drivers with four times higher prevalence of rare drivers than previously calculated. Our results indicate a complex relationship between the driver landscape of somatic missense mutations and each cancer type, some reveal a prominent role for rare drivers while others rely on common drivers and are already saturating discovery. We show experimentally that CHASMplus discriminates radiosensitivity mutations within the ATM gene, a phenotype of potential clinical relevance. The prevalence of rare cancer drivers has implications for future interpretation of cancer genomes and genome-driven oncology.

## Releases

You can download [releases](https://github.com/KarchinLab/CHASMplus/releases) on github.

## Installation

### conda

We recommend using conda to install the CHASMplus dependencies.

```bash
$ conda env create -f environment.yml 
$ source activate CHASMplus
```

Make sure the CHASMplus environment is activated when you want to run CHASMplus.

### pip

CHASMplus needs R and the randomForest R package. Since pip can not do this, you will need to do this by yourself.

CHASMplus also requires the following python packages:

* numpy
* scipy
* pandas>=0.17.0
* scikit-learn
* rpy2
* probabilistic2020
* snakemake

To install these packages via `pip` you can use the following command:

```bash
$ pip install -r requirements.txt
```

## Issues

* snvGetGenomic does not work in python 3, which is what most of my code is intended to run on
* 20/20+ only works in hg19, but CHASMplus is in hg38
