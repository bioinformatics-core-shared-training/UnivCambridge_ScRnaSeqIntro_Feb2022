# Introduction to single-cell RNA-seq data analysis

### 4, 11, 18 Feb 2022, 09:30 - 17:30
#### Taught remotely (zoom link provided by email)
#### Bioinformatics Training Facility, University of Cambridge

![](Images/uniOfCamCrukLogos.png)

## Instructors

* Abigail Edwards - Bioinformatics Core, Cancer Research UK Cambridge Institute
* Ashley Sawle - Bioinformatics Core, Cancer Research UK Cambridge Institute
* Hugo Tavares - Bioinformatics Training Facility, University of Cambridge
* Katarzyna Kania - Genomics Core, Cancer Research UK Cambridge Institute
* Stephane Ballereau - Cellular Genetics programme, Wellcome Sanger Institute

**Helpers:**

* Chloe Pacyna - Wellcome Sanger Institute
* Jon Price - The Gurdon Institute, University of Cambridge
* Qi Wang - Department of Plant Sciences, University of Cambridge

## Outline

This workshop is aimed at biologists interested in learning how to perform
standard single-cell RNA-seq analyses. 

This will focus on the droplet-based assay by 10X genomics and include running
the accompanying `cellranger` pipeline to align reads to a genome reference and
count the number of read per gene, reading the count data into R, quality control,
normalisation, data set integration, clustering and identification of cluster
marker genes, as well as differential expression and abundance analyses.
You will also learn how to generate common plots for analysis and visualisation
of gene expression data, such as TSNE, UMAP and violin plots.

> ## Prerequisites
>
> __**Some basic experience of using a UNIX/LINUX command line is assumed**__
> 
> __**Some R knowledge is assumed and essential. Without it, you
> will struggle on this course.**__ 
> If you are not familiar with the R statistical programming language we
> strongly encourage you to work through an introductory R course before
> attempting these materials.
> We recommend our [Introduction to R course](https://bioinformatics-core-shared-training.github.io/r-intro/)

## Data sets

Two data sets:

* '[CaronBourque2020](https://www.nature.com/articles/s41598-020-64929-x)': pediatric leukemia, with four sample types, including:
  * pediatric Bone Marrow Mononuclear Cells (PBMMCs)
  * three tumour types: ETV6-RUNX1, HHD, PRE-T  
* ['HCA': adult BMMCs](https://data.humancellatlas.org/explore/projects/cc95ff89-2e68-4a08-a234-480eca21ce79) (ABMMCs) obtained from the Human Cell Atlas (HCA)
  * (here downsampled from 25000 to 5000 cells per sample)

## Schedule

Please not that we may adjust these times as the pace of the course requires.

### Day 1

* 09:30 - 09:40 **Welcome** <!-- Paul -->
* 09:40 - 10:25 **Introduction** - Katarzyna Kania
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/01_Introduction.pdf)
* 10:25 - 10:30 5 min **break** 
* 10:30 - 10:40 **Preamble**: data set and workflow - Stephane Ballereau
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/02_PreambleSlides.html)
* 10:40 - 12:30 Library structure, **cellranger** for alignment and cell calling - Stephane Ballereau
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/03_CellRangerSlides.html) <!-- \([pdf](scRNAseq/Slides/CellRangerSlides.pdf)\) -->
    + [Alignment with Cell Ranger](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/03_CellRanger.html)
* 12:30 - 13:30 **lunch break**
* 13:30 - 17:30 **QC and exploratory analysis** - Ashley Sawle
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/04_QualityControlSlides.html) \([pdf](UnivCambridge_ScRnaSeqIntro_Base/Slides/04_QualityControlSlides.pdf)\)
    + [QC and preprocessing](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/04_Preprocessing_And_QC.html)
    + [Exercise](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/04_Preprocessing_And_QC.Exercise.html)  

### Day 2

* 09:30 - 09:40 Recap <!-- Stephane -->
* 09:40 - 12:30 **Normalisation** - Stephane Ballereau
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/05_NormalisationSlides.html) <!-- \([pdf](scRNAseq/Slides/05_normalisationSlides.pdf)\) -->
    + [Practical](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/05_Normalisation.html)    
<!-- + [Exercises](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/05_Normalisation_exercises.html) -->
<!-- + [Exercise Solutions](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/05_Normalisation_exercises_solutions.html) -->
* 12:30 - 13:30 **lunch break**
* 13:30 - 15:25 **Feature selection and dimensionality reduction** - Hugo Tavares
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/06_FeatureSelectionAndDimensionalityReduction_slides.html)
    + R script for practical in `Exercises/06_DimensionalityReduction_worksheet.R` (you can also download it [here](https://github.com/bioinformatics-core-shared-training/UnivCambridge_ScRnaSeqIntro_Base/blob/87c654f73aa47d258f39a9c42d1563c4e51ddcd3/CourseMaterials/Exercises/06_DimensionalityReduction_worksheet.R))
<!-- + [Materials](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/06_FeatureSelectionAndDimensionalityReduction.html) -->
* 15:25 - 15:35 10 min **break**
* 15:35 - 17:30 **Batch correction and data set integration** - Abigail Edwards
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/07_DataIntegrationAndBatchCorrectionSlides.html)  
 + [Data set integration](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/07_DatasetIntegration.html) 
<!-- + [Solutions](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/07_DataIntegrationChallengeSolution.html) -->
<!-- + [Batch Correction extended example](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/07_BatchCorrection.html) -->
    
### Day 3

* 09:30 - 09:40 Recap <!-- Stephane -->
* 09:40 - 11:05 **Clustering** - Stephane Ballereau
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/08_ClusteringSlides.html)
<!-- + [Practical](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/08_ClusteringPostDsi.html) -->
<!-- + [Exercise1](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/08_ClusteringPostDsi_exercise.Rmd) -->
<!-- + [Exercise Solutions](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/08_ClusteringPostDsi_exercise_solutions.html) -->
* 11:05 - 11:15 10 min **break** 
* 11:15 - 12:30 **Identification of cluster marker genes** - Hugo Tavares
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/09_ClusterMarkerGenes.html)
    + R script for practical in `Exercises/09_ClusterMarkerGenes.R` (you can also download it [here](https://github.com/bioinformatics-core-shared-training/UnivCambridge_ScRnaSeqIntro_Base/blob/87c654f73aa47d258f39a9c42d1563c4e51ddcd3/CourseMaterials/Exercises/09_ClusterMarkerGenes.R))
<!-- + [Cluster marker genes](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/09_ClusterMarkerGenes.html) -->
<!-- + Worksheet in `Exercises/09_ClusterMarkerGenes.R` -->
* 12:30 - 13:30 **lunch break**
* 13:30 - 15:25 **Differential expression between conditions** - Stephane Ballereau
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/10_MultiSplCompSlides.html)
<!-- + [Practical](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/10_MultiSplComp.html) -->
<!-- + [Exercise1](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/10_MultiSplComp_exercise1.Rmd) -->
<!-- + [Exercise1 Solutions](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/10_MultiSplComp_exercise1_solutions.html) -->
* 15:25 - 15:35 10 min **break** 
* 15:35 - 17:30 **Differential abundance between conditions** - Stephane Ballereau
    + [Slides](UnivCambridge_ScRnaSeqIntro_Base/Slides/10_MultiSplCompSlides.html)
<!-- + [Practical](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/10_MultiSplComp.html) -->
<!-- + [Exercise2](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/10_MultiSplComp_exercise2.Rmd) -->
<!-- + [Exercise2 Solutions](UnivCambridge_ScRnaSeqIntro_Base/Markdowns/10_MultiSplComp_exercise2_solutions.html) -->
