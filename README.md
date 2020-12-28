# Normalization for various batches using NMJ-Analyser
This script was done using R/RStudio 1.2.1 and ggplot2 package.

What is this? 
We have created a simple protocol for normalization MFI between batches. This protocol has to be used with NMJ-Analyser pipeline.

How can I use it? 
We have submitted a file called normalization.csv. It contains 4 columns (Timepoint, MFI_presynaptic, Presynaptic_volume, Normalized_volume)
Timepoint = it has 3 different experiments (batches) MFI_presynaptic = Mean Fluorescence Intensity of each presynaptic NMJ in each batch analyzed Presynaptic_volume = actual Presynaptic values obtained by NMJ-Analyser Normalized_volume = corrected volume to compare between batches

Steps for normalization: 
1.- Test whether MFI of each batch follows a normal distribution (apply Shapiro-Wilk test). See test file 
2.- Test whether MFI differ statistically between batches (see Normalized.R) 
3- if batches differ, divide Presynaptic_volume by their Normalized_volume = Normalized_volume
