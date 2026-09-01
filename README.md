BESTTAXA: pipeline adaptado para la asignación taxonómica de consenso de secuencias 16S de longitud completa.

This workflow was adapted and modified by Andrés David Delgado Aldana for the taxonomic classification of full-length 16S rRNA PacBio HiFi sequences. 
It integrates classifications obtained from Greengenes2, GTDB and SILVA, applying a minimum confidence threshold of 0.80 and the priority order GG2 → GTDB → SILVA.

## Metodología de asignación taxonómica

El enfoque de asignación taxonómica "best taxonomy" implementado en este 
repositorio está inspirado en la estrategia utilizada por el pipeline 
HiFi-16S-workflow de PacBio (PacificBiosciences), que prioriza la 
clasificación entre tres bases de referencia en el siguiente orden: 
GreenGenes2 → GTDB → SILVA, evaluando primero la resolución a nivel de 
especie y, si no es posible, a nivel de género.

Referencia: PacificBiosciences. HiFi-16S-workflow. 
https://github.com/PacificBiosciences/HiFi-16S-workflow

## Bases de datos y clasificadores utilizados

- GreenGenes2: gg2_2024.09_full_length_classifier.qza (release 2024.09)
- GTDB: gtdb_human_stool_weighted_classifier_r220.qza (release r220, 
  weighted para muestras de heces humanas)
- SILVA: silva-138-99-nb-classifier.qza (SILVA 138, 99% OTUs)
- Clasificación realizada con QIIME 2 (qiime feature-classifier classify-sklearn)

- ## Entorno de R

- R version: [pegar aquí la salida de sessionInfo()]
- dplyr: [versión]
- readr: [versión]
- stringr: [versión]

- ## Licencia

Este repositorio se distribuye bajo licencia MIT. Ver archivo LICENSE.

Nota: las bases de datos de referencia (GreenGenes2, GTDB, SILVA) y los 
clasificadores de QIIME 2 tienen sus propias licencias de uso, independientes 
de este código.
