# PBTK_Adult_Zebrafish
PBTK model for bisphenols in adult zebrafish. Code written by Ioana Chelcea, adapted from Grech et al. 2019
Publication:Title: "Physiologically Based Toxicokinetic Modelling of Bisphenols in Zebrafish (Danio rerio) Accounting for Variation in Metabolic Rates, Brain Distribution and Liver Accumulation"
Author(s): Chelcea, Ioana; Örn, Stefan; Hamers, Timo; Koekkoek, Jacco ; Legradi, Jessica; Vogs, Carolina; Andersson, Patrik
Reference if used and/or modified

Repository contains 2 files for running the model. IMPORTANT: Place both files in the same folder and set the local KNIME directory to that folder. All packages required for running need to be installed
Files for model running:
1. PREDATAR_Revision_git.knwf :KNIME workflow containing models modfied to fit each experimental scenario found in literature and displaying all predictions and graph. The main workflow contains the experimental data for BPA (Lindholst et al. 2013, Chen et al. 2017, Fang et al. 2016), BPAF (Shi et al. 2016), BPZ (Chelcea et al. 2022) and TBBPA (Nyholm et al. 2007). The Metanode entitled "All BPs" contains the predictions for all selected bisphenols at a dose of 10 µg/L in female adult zebrafish and calculation of the corresponding biococentration factors (BCFs) in organs.
2. Model_parameters_KNIME_Fitted_revision1.xlsx :Contains parameters needed to parameterize the model. Each sheet contains parameters for one of the 11 selected bisphenols and gender-speciffic paramateres (_M for males and _F for females). Place this file in the same folder as the KNIME workflow.

Instructions:
1. Download both files in the same folder. 
2. Open KNIME and set your local directory to that folder. (You can change your local directory under File>Switch workspaces> Browse for the folder you have the files in)
3. To open workflow it has to be imported. Go to File>Import KNIME workflow> Select file (Browse and select the PREDATAR_Revision_git.knwf file)

Required R packages:
plyr
dplyr
deSolve
reshape2
httk
MESS
tidyverse
sensitivity
ggplot2

Trouble shooting:
Packages not found even after installing them: Check which version of R is set to use in KNIME. Using a local computer version is more suitable as packages are installed there by default. To change R version go to File>Preferences>KNIME>R> Path to R Home.
