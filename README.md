# Interpreting the IQMs of MRIQC

In this project we want to improve the interpretability of the Image Quality Metrics (IQMs) generated by MRIQC.

**What is MRIQC?**

MRIQC is an open-source tool to assess the quality of structural and functional MRI images. It generates visual reports for every scan, as well as a number of IQMs which are collected in a group-level report.

**What are IQMs?**

Image Quality Metrics (IQMs) are automatically generated metrics that reflect different aspects of the quality of an MR image. In the [MRIQC paper](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0184661#pone-0184661-t002) on table 2 you can find an overview of the IQMs and what they are measuring.

**What data do we use?**

We will use the [Movement-Related Artifacts (MR-ART)](https://www.nature.com/articles/s41597-022-01694-8) dataset. It contains the T1-weighted images of 148 healthy subjects. Each subject has been acquired under three motion conditions:

1. no head movement
2. little head movement
3. much head movement

The motion was artifically induced by giving the subjects cues when to node their head.

**How are we approaching the problem?**

We are using two different approaches to this problem.

1. We use dimensionality reduction techniques such as PCA, ICA, Factor Analysis, or TSNE to find summary dimensions that combine the metrics with potentially redundant information.

2. We use machine learning, in particular supervised learning, to predict the quality ratings and/or the motion condition of the images from the IQMs.

**What is the output?**

We combined what we learned with both approaches in a [dedicated notebook](./code/interpretability-of-iqms.ipynb). This notebook is aimed at being an educational ressource for researchers willing to learn how to analyse and interpret IQMs. This notebook has additionally been integrated into the [Nipreps QC book](https://www.nipreps.org/qc-book/auto-qc/iqms_intepretability.html). The results have been submitted as an abstract to OHBM Montréal 2023. This abstract is entitled ""Signal-to-noise ratio estimates predict head motion presence in T1-weighted MRI" and is available at [https://osf.io/7vqzr/](https://osf.io/7vqzr/).
