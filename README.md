
# surface-trafficking

##### Python code for May and Gaudet (2024), Surface delivery quantification reveals distinct trafficking efficiencies among clustered protocadherin isoforms. These data are also available on [Zenodo](10.5281/zenodo.13345292).

***

### File descriptions

##### in the Segmentation folder:

- There is a segmentation `.yml` file with the environment for the segmentation notebook. A GPU is required to run this notebook.
- The segmentation notebook takes `.czi` microscope files as input, as well as a user-provided list of samples. For our experiments, the `.czi` files contain 24 positions (8 samples with 3 fields of view each) and 3 channels, one of which is brightfield. The notebook produces a segmentation mask (`labels.npy`) based on the brightfield channel and a `.txt` file containing the sample names, both of which are used as input for the calculations notebooks.

##### in the Calculations folder:

- There is a `micro_analysis.yml` file with the environemnt for all the analysis.
- The images_to_csv.ipynb notebook that takes the `.czi` microscope file, along with the `sample.txt` file and `labels.npy` mask file from the segmentation output, and calculates the average fluorescence values for each cell. The output is a `.csv` file (in the `out` folder) for each experiment. These data are also available on [Zenodo](10.5281/zenodo.13345292).
- The original `.csv` files containing the average fluorescence values for the experiments conducted for the manuscript are in the `out` folder.
- The `metrics.ipynb` notebook contains the code that pools the cellwise-averaged data from all the experiment `.csv` files and calculates `f+`, `Ab_bar`, and `E_surface`. These calculations make use of thresholds from specific control samples, including a mock-transfected sample and an transfected sample that is untagged or unstained. See manuscript `materials and methods` for further details.
- the `calc_metrics` folder contains `.csv` files with the calculated surface delivery metrics for the experiments from the manuscript. These data are also available on [Zenodo](10.5281/zenodo.13345292).
