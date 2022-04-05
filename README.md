# CSS844_Module2_Group2

**Guide to colab notebooks:**

_Lidar processing for all plots and fields.ipynb:_ Looping through all plots to get data, and similar to (derived from) “Module 2 Lidar Processing.ipynb”

_Module 2 Lidar Processing.ipynb:_ Adopted code from the pdf for lidar processing but is only for one plot. Was used as a stepping stone and first step to process all plots

_Untitled2.ipynb:_ This was code for merging and plotting all point clouds, and some visualization. The merging function did not end up needed since each numpy file is already a plot (defined by one row and one column within one folder/”id” in metadata)

_RunPCA.ipynb:_ Working out code to run PCA on the data in preparation for further modelling (this needs be run on HPCC, as it will use too much RAM and crash when run in Colab)

_scree_plot_linear_regression.ipynb:_ Creates scree plots for x, y, and z PCAs (PCA run as in RunPCA.ipynb). Also has some code to do linear regression on the data (scroll down to the last cell for the model that uses the first 5 x PCs, first y PC, and first 5 z PCs).

**Notes on data files:**
- Meta data: (example: https://michiganstate-my.sharepoint.com/:x:/r/personal/thom1718_msu_edu/_layouts/15/doc2.aspx?sourcedoc=%7B06767E34-39C9-4C8A-9893-F1C14298F47E%7D&file=21atue_vw_2021-08-18.csv&action=default&mobileredirect=true&cid=0024ca80-048f-4416-896b-4167187477a0)
  - This file contains:
  - ID
  - Timestamp
  - Field
  - Column
  - Range (“row”)
  - Start (ms)
  - End (ms)
- ground traits file (example: https://docs.google.com/spreadsheets/d/1z_tReav6UDIi5lkTB3prd5sBhGDn-Og6/edit#gid=562832244)
  - This file contains phenotypic measurements 

**Other resources:**

Code from Gage et al. Plant Phenome Paper: https://acsess.onlinelibrary.wiley.com/doi/full/10.2135/tppj2019.07.0011

Video from class with Dr. Gage speaking: https://mediaspace.msu.edu/media/1_sqiv9zmr

Main Source with all steps and scripts: https://bitbucket.org/bucklerlab/p_lidar_lsp/src/master/ [Contains source code for processing lidar data. To replicate analyses done in the paper, run the scripts prefaced with numbers 1-6 in order. File paths may need to be changed inside scripts.]

1_LiDar_import_clean_makeDensities.R:

2_process_raw_point_clouds.R:

3_remoteAutoencoder.sh:

4_make_clean_dataset.R:

5_PLSR.R:

6_model_phenotypes.R:
