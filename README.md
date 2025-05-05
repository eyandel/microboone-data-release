# microboone-data-release
Example code for various MicroBooNE HEPdata data releases

## Overview
Each script has the same backbone of code, slightly modified for the specific data releases. Before running, you will need to download all yaml files from the HEPdata release, unzip it, and store them in the same directory as the jupyter notebook.

- Creates list of all datasets using the `submission.yaml` input file from HEPdata
- Separates into 3 general categories (1D data, efficiency, covaraince matrix), currently based on manually noted keywords in the dataset titles
- Reads in the independent and dependent datasets, as definted in the HEPdata yaml
- Automatically stacks the background + signal prediction (MC) channels for the 1D plots
- Efficiencies plotted to match the given datasets
- Covariance matrix plotted to show visual correlations
- Example of how to calculate a chi^2 and goodness of fit 

## Specifics: Inclusive

## Specifics: NC Delta

## Specifics: e+e-
