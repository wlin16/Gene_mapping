# Gene_mapping

Concordance analysis of atrophy in MS an regional gene expression

A pre-print describing the analysis and a prior version of the pipeline and the results can be accessed through bioRxiv: https://www.biorxiv.org/content/10.1101/2019.12.11.872143v1

To prepare the data, first run the two jupyer notebooks. This requires the gene expression data from the Allen Institute, available here: http://human.brain-map.org/static/download

The other bit required are updated (or improved) MNI coordinates. E.g., the ones provided by Chris Gorgolewski and available here: https://github.com/chrisgorgo/alleninf/tree/master/alleninf/data

1) AIBS_sample_preprocessing.ipynb This script selects the eligbile samples for the analysis.

2) AIBS_probe_selection.ipynb This script selects the eligible gene expression probes for the analysis.

3) Coordinates to values.ipynb This script obtains the sustain stage for a given MNI coordinate.

4) Add_labels_and_stages.ipynb This script adds regional labels and corresponding gene ids to each subtype. This script also contains the correlation part for atrophic progression of MS

