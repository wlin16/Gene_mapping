# Gene_mapping

Concordance analysis of atrophy in MS an regional gene expression

These are parts of scirpts contributing to my Master thesis research project. 

## I. Gene mapping and correlation

To prepare the data, first run the two jupyer notebooks. This requires the gene expression data from the Allen Institute, available here: http://human.brain-map.org/static/download

The other bit required are updated (or improved) MNI coordinates. E.g., the ones provided by Chris Gorgolewski and available here: https://github.com/chrisgorgo/alleninf/tree/master/alleninf/data

1) AIBS_sample_preprocessing.ipynb This script selects the eligbile samples for the analysis.

2) AIBS_probe_selection.ipynb This script selects the eligible gene expression probes for the analysis.

3) Coordinates to values.ipynb This script obtains the EBM stage for a given MNI coordinate.

4) Regional_correlation.ipynb This script adds regional labels and EBM Stages to each sample ID. This script also contains the correlation part for temporal atrophic progression in MS

5) Genetic_correlation_plotting.ipynb This script plot out the figures for the correlation between the MS progression with top ten most correlated genes in positive and negative lists.


## II. GO overrepresentation analysis

After finishing the correlation part, the most correlated genes with the progression can be obtained (according to the r values). Then, these genes can be put into GO for overrepresentation analysis. In this project, we used an online Go tool which can be accessed through: http://cbl-gorilla.cs.technion.ac.il/

GO results can be downloaded as .xls files from the online GO tool. As jupyter lab does not recognise .xls files, we have to transformed them into .xlsx files before analysis. After that, we can analyse the results according to the order of the corresponding r value of each gene and the enrichment levels. 

Rank.ipynb This script matches r values to all genes in order. 

## III. Cell type correlation analysis

As we also would like to know the correlation between the potential brain cell type and MS temporal progression, we combined the genetic expression data with the cell fraction data (Menden et al. 2020).

Cell_type_plotting.ipynb This script combined two datasets to calculate the expression extent of various cell types by genes in two lists. 

########################################################

# Appendix

## 1. Script for image parcellation
The script for removing skull, CSF etc. and image parcellation: 'instruction_for_parcellation.txt'.
Please install FSLeye software before typing the codes into terminal. 

## 2. Supplementary dataset
Two Supplementary datasets can be found in the 'Supplementary dataset' file. Supplementary dataset 1 includes all significantly correlated genes; Supplementary dataset 2 includes all significantly enriched GO terms. 

