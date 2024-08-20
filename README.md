
# surface-trafficking

### This repository contains Python code for May and Gaudet (2024), Surface delivery quantification reveals distinct trafficking efficiencies among clustered protocadherin isoforms.

### Important files:

#### + Segmentation (in the Segmentation folder):

- There is a segmentation '.yml' file with the environment for the segmentation notebook. A GPU is also required to run this notebook.
- The segmentation notebook takes '.czi' microscope files as input, as well as a user-provided list of samples. For our experiments, the '.czi' files contain 24 positions (8 samples with 3 fields of view each) and 3 channels, one of which is brightfield. The notebook produces a segmentation mask based on the brightfield channel ('labels.npy') and a '.txt' file containing the sample names, both of which are used as input for the calculations notebooks.

#### + Calculations (in the Calculations folder):

- There is a 'micro_analysis.yml' file with the environemnt for all the analysis.
- The images_to_csv.ipynb notebook that takes the '.czi' microscope file, along with the 'sample.txt' file and 'labels.npy' mask file from the segmentation output, and calculates the average fluorescence values for each cell. The output is a '.csv' file (in the out folder) for each experiment.
- The original '.csv' files containing the average fluorescence values for the experiments conducted for the manuscript are in the 'out' folder.
