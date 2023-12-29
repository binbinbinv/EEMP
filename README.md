# EEMP
This is the bioinformatic workflow to identify putative PET-degrading enzymes

## grep Command Usage:
Taking the example of the "grep -E -B 1 "SMGGG.{25,35}D"" command, where "." represents any amino acid and "{25,35}" denotes an interval of 25-35 amino acids between SMGGG and D. In the context of this manuscript, to reproduce the results, the code needs to be modified as follows: "! grep -B 1 SMGGG path/to/Alphafold_sequences.fasta | grep -E -B 1 "! grep -B 1 SMGGG path/to/Alphafold_sequences.fasta | grep -E -B 1 "SMGGG.{38,44}D" | grep -E -B 1 "SMGGG.{66,76}H" | grep -v ^- > SMGGG_D_H.fasta"

## Exclusion of Low-Confidence Data:
We have excluded data from the AlphaFold protein structure database with Model Confidence CA scores below 60, specifically referring to the "Ca_reliability" in the code.

## Adjustable Parameters in Code:
The parameters S_D_distance, S_H_distance, and D_H_distance in the code can be set to any desired range.