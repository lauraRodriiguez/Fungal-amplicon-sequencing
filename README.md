# Fungal Amplicon Sequencing

Investigating the soil microbiome of peanuts at the Wiregrass Research and Extension Center (WREC) in Headland, Alabama, under five distinct water regimes. Using ITS amplicon sequencing, leveraging the Alabama Supercomputer, and conducting subsequent analysis in R. Starting with demultiplexed reads.

## [Striping primers](https://github.com/lauraRodriiguez/Fungal-amplicon-sequencing/blob/main/Scripts/01_strippingPrimers.rtf)

Removal of primer form sequences

## [Get stats](https://github.com/lauraRodriiguez/Fungal-amplicon-sequencing/blob/main/Scripts/02_stats.rtf)

Filtering parameters

## [Filtering and trimming](https://github.com/lauraRodriiguez/Fungal-amplicon-sequencing/blob/main/Scripts/03_filtering%20%26%20trimming.rtf)

Trimming and filtering based on the "stats" results. FASTQ used to observe the quality of the data

## [Dereplication, De-noising, Clustering](https://github.com/lauraRodriiguez/Fungal-amplicon-sequencing/blob/main/Scripts/04_clustering.rtf)

De-noising: zOTUs
Clustering: OTUs based on traditional 97% identity

## [Mapping](https://github.com/lauraRodriiguez/Fungal-amplicon-sequencing/blob/main/Scripts/05_mapping.rtf)

OTU table

## [Taxonomy](https://github.com/lauraRodriiguez/Fungal-amplicon-sequencing/blob/main/Scripts/06_taxonomy.rtf)

This will create the taxonomy to all filtered and trimmed sequences. For fungal taxonomy UNITED databased was employed, utilizing two taxonomy programs, SINTAX and NBC.

## [R analysis](https://github.com/lauraRodriiguez/Fungal-amplicon-sequencing/blob/main/FungalPeanutsSoilAnalysis2.Rmd)
Additional downstream analysis and visualization were conducted, with the predominant utilization of R packages such as "phyloseq," "tyRa," "Biostrings," "ggplot2," "dplyr," and "vegan."
- Load packages, dependencies and palettes
- Input metadata, OTUs, taxonomy, and fasta
- Filter the "unidentified" from your taxonomy
- Decontaminate data
- Sanity check, making sure all the taxonomy is fungi
- Filter and discard all samples with less than 5000 reads
- Rarefaction analysis
- Normalize the data
- Beta diversity
- Prevalent fungi in the soils
- Differential abundance analysis
- Core microbiome