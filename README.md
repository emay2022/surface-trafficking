# surface-trafficking

### This repository contains Python code for May and Gaudet (2024), Surface delivery quantification reveals distinct trafficking efficiencies among clustered protocadherin isoforms.

### Important files:
#### Segmentation
##### In the segmentation folder, there is a segmentation .yml file with the environment for the segmentation notebook. A GPU is also required to run this notebook.
##### In the segmentatin folder, the segmentation notebook takes .czi microscope files as input, as well as a user-provided list of samples. For our experiments, the .czi files contain 24 positions (8 samples with 3 fields of view each) and 3 channels, one of which is brightfield. The notebook produces a segmentation mask based on the brightfield channel (labels.npy) and a .txt file containing the sample names, both of which are used as input for the calculations notebooks.
#### Calculations
##### In the calculations folder:
