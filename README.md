BESTTAXA: An adapted pipeline for consensus taxonomic assignment of full-length 16S rRNA gene sequences.

This workflow was adapted and modified by Andrés David Delgado Aldana for the taxonomic classification of full-length 16S rRNA PacBio HiFi sequences. 
It integrates classifications obtained from Greengenes2, GTDB and SILVA, applying a minimum confidence threshold of 0.80 and the priority order GG2 → GTDB → SILVA.

## Methodological origin and citation

BESTTAXA is an R-based implementation adapted from the “besttax”
taxonomic prioritization strategy of the PacBio HiFi-16S-workflow.
The underlying strategy prioritizes Greengenes2, GTDB, and SILVA
and evaluates species-level assignments before genus-level assignments.

This repository provides an implementation for integrating taxonomic
classifications generated with QIIME 2 `classify-sklearn`, using updated
reference classifiers and an additional fallback procedure.

If you use the implementation provided in this repository, please cite
BESTTAXA and acknowledge the original PacBio HiFi-16S-workflow.

## Taxonomic Assignment Methodology

The “best taxonomy” approach implemented in this repository was inspired by the strategy used in PacBio’s HiFi-16S-workflow (Pacific Biosciences). 
This approach prioritizes classification using three reference databases in the following order: GreenGenes2 → GTDB → SILVA. 
Taxonomic resolution is first evaluated at the species level and, when this is not possible, at the genus level.
Reference: Pacific Biosciences. HiFi-16S-workflow.
https://github.com/PacificBiosciences/HiFi-16S-workflow

## Databases and Classifiers Used
GreenGenes2: gg2_2024.09_full_length_classifier.qza (release 2024.09)
GTDB: gtdb_human_stool_weighted_classifier_r220.qza (release r220, weighted for human stool samples)
SILVA: silva-138-99-nb-classifier.qza (SILVA 138, 99% OTUs)
Taxonomic classification performed with QIIME 2 (qiime feature-classifier classify-sklearn)
## R Environment
R version:
dplyr
readr
stringr

## License

This repository is distributed under the MIT License. See the LICENSE file.
Note: The reference databases (GreenGenes2, GTDB, and SILVA) and the QIIME 2 classifiers are subject to their own licenses, independently of this code.
