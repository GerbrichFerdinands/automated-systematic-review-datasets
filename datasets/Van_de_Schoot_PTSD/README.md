# PSTD

**Bayesian PTSD-Trajectory Analysis with Informed Priors Based on a Systematic Literature Search and Expert Elicitation**
Rens van de Schoot ORCID Icon, Marit Sijbrandij, Sarah Depaoli ORCID Icon, Sonja D. Winter ORCID Icon, Miranda Olff & Nancy E. van Loey
https://doi.org/10.1080/00273171.2017.1412293

Dataset publication: https://osf.io/h5k2q/

# Data cleaning

To create the cleaned dataset in the proper format for the ASR software, you can use the `raw2csv.py` python script in this folder. This will create the cleaned dataset in `output/PTSD_VandeSchoot_18.csv`.

This can also be done manually on the command line:

Use the `risparser.py` script to convert the ris files to csv (schoot-lgmm-ptsd-included-2.csv, schoot-lgmm-ptsd-included-1.csv,  schoot-lgmm-ptsd-initial.csv):

```bash
python risparser.py $FILE_IN $FILE_OUT
```

Put the converted files in the `csv` folder and run the R script with

```bash
Rscript clean_schoot_lgmm_ptsd.R
```

The resulting training data should be in `csv/PTSD_VandeSchoot_18.csv`.