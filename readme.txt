# Replication Package for 'Political Expression of Academics on Social Media'

## Overview

This replication package contains all necessary scripts and data to replicate the main figures and tables presented in the paper.

## Folder Structure

### 1. `1_scripts`

This folder contains all scripts required to replicate the main figures and tables of the paper. The scripts are numbers with a prefix (e.g. "1_") in the order they should be run. Output will also be produced in this folder.

- `0_init.Rmd`: An R Markdown file that installs and loads all packages necessary for the subsequent scripts. 
- `1_fig_1.Rmd`: Primarily produces Figure 1 (Zipf's plots) and conducts statistical tests to support underlying statistical claims made through the figure.

- `2_fig_2_to_4.Rmd`: Primarily produces Figures 2 to 4 (average levels of expression) and conducts statistical tests to support underlying statistical claims made through the figures. This includes conducting t-tests to establish subgroup differences. 

The script also includes The file table_controlling_how.csv contains the full set of regression results for the analysis of subgroup differences in political stances, controlling for emotionality, egocentrism, and toxicity. This file includes effect sizes, standard errors, confidence intervals, and p-values for each stance, group variable, and confounder.

- `3_fig_5_to_6.Rmd`: Primarily produces Figures 5 to 6 (trends in expression) and conducts statistical tests to support underlying statistical claims made through the figures. This includes conducting t-tests to establish subgroup differences. 

- `4_tab_1_to_2.Rmd`: Produces Tables 1 to 2, and shows code for Table A5 (descriptive tables). 

Expected run time for each script is under 3 minutes and requires around 4GB RAM. Script `3_fig_5_to_6.Rmd` can take up to 3-4 minutes and requires up to 6GB RAM. Installation of each package for the first time user may take around 2 minutes each, except 'tidyverse', which may take around 4 minutes. 

We have not provided a demo since the actual dataset used for analysis is small enough and computations are efficient enough to be run in most systems.

Each script starts with a layperson explanation to overview the functionality of the code and a pseudocode for a detailed procedure, followed by the actual code.

### 2. `2_data`

This folder contains all data used to replicate the main results. The data is called by the respective scripts automatically using relative paths.

- `data_dictionary.txt`: Provides a description of all variables as they are coded in the various datasets, especially the main author by time level dataset called `repl_df.csv`.
- Processed data at individual author by time (year by month) level aggregated measures are provided, as raw data containing raw tweets cannot be shared.

## Installation Instructions

### Prerequisites

This project uses R and RStudio. Make sure you have the following installed:

- [R](https://cran.r-project.org/) (version 4.0.0 or later)
- [RStudio](https://www.rstudio.com/products/rstudio/download/)

Once installed, to ensure the correct versions of the required packages are installed, use the following R markdown script '0_init.Rmd'. This script will install the `remotes` package (if not already installed) and then install the specified versions of the required packages.

## Running the Scripts
Open 0_init.Rmd in RStudio and run all chunks to install and load the required packages.
Run the remaining scripts (1_fig_1.Rmd, 2_fig_2_to_4.Rmd, 3_fig_5_to_6.Rmd, and 4_tab_1_to_2.Rmd) in the order they are listed to reproduce the figures and tables from the paper.

# Contact
For any questions, feel free to contact Prashant Garg at prashant.garg@imperial.ac.uk.

# License

This project is licensed under the Apache License 2.0 - see the license.txt file for details.
