# microboone-data-release
Example code for various MicroBooNE HEPdata data releases

## Overview
Each script has the same backbone of code, slightly modified for the specific data releases. Before running, you will need to download all yaml files with resource files from the HEPdata page, unzip it, and store them in the same directory as the jupyter notebook.

- Creates list of all datasets using the `submission.yaml` input file from HEPdata
- Separates into 3 general categories (1D data, efficiency, covaraince matrix), currently based on manually noted keywords in the dataset titles
- Reads in the independent and dependent datasets, as definted in the HEPdata yaml
- Automatically stacks the background + signal prediction (MC) channels for the 1D plots
- Efficiencies plotted to match the given datasets
- Covariance matrix plotted to show visual correlations
- Example of how to calculate a chi^2 and goodness of fit 

## Specifics: Inclusive

- Automatically handles the cases for constrained and unconstrained predictions, along with the impact of including the LEE model
- Stacks the MC Background, 1 photon in Fiducial Volume signal, and the Low Energy Excess (LEE) expectation (when applicable)
- Handles input for 2D efficiency (the second independent variable goes from -1 --> 1)
- Shows calculation of the Pearson Chi^2 used in this analysis to estimate the statistical impact in the covariance matrix 

## Specifics: NC Delta

- Only shows prediction vs. data for 1D plots (no stacking needed)
- Input order for 2D efficiency slightly different (the second independent variable goes from 1 --> -1)
- Combines necessary 1D datasets (manually) to calculate chi^2 with the given covariance matrices
- Note that the statistical covariance is included already in the given covaraince matrix, so no addition needed

## Specifics: e+e-

- Stacks the MC and Sig(nal) to compare with data
- Data uncertainty not given in HEPdata table, but it is just statistical sqrt(n)
- Efficiency is in 1D slices with the given topology
- Combines necessary 1D datasets (manually) to calculate chi^2 with the given covariance matrix
- Shows calculation of the Pearson Chi^2 used in this analysis to estimate the statistical impact in the covariance matrix 
