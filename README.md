BESTTAXA: An adapted pipeline for consensus taxonomic assignment of full-length 16S rRNA gene sequences.

This workflow was adapted and modified by Andrés David Delgado Aldana for the taxonomic classification of full-length 16S rRNA PacBio HiFi sequences. 
It integrates classifications obtained from Greengenes2, GTDB and SILVA, applying a minimum confidence threshold of 0.80 and the priority order GG2 → GTDB → SILVA.

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
