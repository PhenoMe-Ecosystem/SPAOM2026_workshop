# PhenoMe: An Interactive Toolkit for Microscopy Data Exploration and Phenotype Discovery with Foundation Model Embeddings

This workshop introduces PhenoMe (https://github.com/AAitorG/PhenoMe), an open-source, interactive Python toolkit designed to bridge the gap between foundation model embeddings and biological interpretation. 

**Requirements and basis**The workshop assumes basic familiarity with Python, including package installation, importing libraries, and executing simple commands for data analysis in Python scripts or notebooks. Nevertheless, workshop instructors will guide participants through every step of the process. No prior experience with machine learning, foundation models, or extensive programming is required. Participants may follow the exercises either on their local computers or through Google Colab environments provided by the instructors.

# PhenoMe setup

**Local installation** (Recomended for an interactive usage) Create a new conda environment and install PhenoMe following the installation instructions in (https://github.com/AAitorG/PhenoMe#-installation). If you are using your laptop, use the CPU option.

**Google Colab** You will need a Google account. Note that we will use the GPUs from Google Colab, which are limited to a few hours per day. 

# Data
### Local installation
You will need to download the following data to run the notebooks locally.
- Exercise 2.1: We will use the BBBC021 dataset from the Broad Bioimage Benchmark Collection [[Ljosa et al., Nature Methods, 2012](http://dx.doi.org/10.1038/nmeth.2083)].
  - Donwload [Filtered BBBC021 dataset](https://drive.google.com/file/d/15yS4g0UFFI60KS3E1smOiN_vWl_Gyyad/view?usp=sharing)
  - Download [PhenoMe embeddings](https://drive.google.com/file/d/1NBwgqc_Anp0A1je-r5yog58ZCeSZn_QR/view?usp=sharing)
  - Download [PhenoMe properties](https://drive.google.com/file/d/17ZRfOURTWRC3q_1hQg33OecQswhCDlaG/view?usp=sharing) 

- Exercise 2.2: We will use the BBBC014 dataset from the Broad Bioimage Benchmark Collection [[Ljosa et al., Nature Methods, 2012](http://dx.doi.org/10.1038/nmeth.2083)].
   - Donwload [BBBC014 dataset](https://drive.google.com/file/d/1386ZTEw-dQ2CXJnNS6basC3dnz4tkqtj/view?usp=sharing)
   - Download [PhenoMe embeddings](https://drive.google.com/file/d/1FadtWDhN3olvHrr5GXQG_8BIAiQiILJt/view?usp=sharing)
   - Download [PhenoMe properties](https://drive.google.com/file/d/1ONDExLd9QQ2ppfLPbrBBRp1m3aSxvNQ8/view?usp=sharing) 

# Exercises
## Exercise 1

**PhenoMe workflow and quickstart** This example is meant to showcase how latent representations can be interpreted through experimental metadata and biological features. The tasks in this exercise includes loading data, visualizing latent spaces, exploring phenotypic organization, and linking embeddings to biological variables, such as morphology. 

**Notebook** PhenoMe/Notebooks/tutorials/01_quickstart:
- Local installation: Open the **[Interactive Quickstart Notebook](https://github.com/AAitorG/PhenoMe/blob/main/Notebooks/tutorials/01_interactive_quickstart.ipynb)** using Jupyter.

For this, after installing PhenoMe as indicated in the [**PhenoMe setup**](https://gist.github.com/esgomezm/c17f78f1fa9ac0259be56ed4f4f4c94f#phenome-setup) section, type the following in your terminal:

```terminal 
conda activate phenome-cpu
jupyter lab
````


- Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AAitorG/PhenoMe/blob/main/Notebooks/tutorials/01_interactive_quickstart.ipynb)


## Exercise 2
**Response to treatment and phenotypic interpretation** We will analyze pre-computed embeddings from large-scale Cell Painting datasets. This exercise will showcase the flexibility of latent representations for identifying biologically meaningful clusters, considering varying aspects such as altered structures or treatment, as well as experimental outliers.

**Notebook 1**
- Local installation: Open the **[BBBC021 Compound Screen](https://github.com/AAitorG/PhenoMe/blob/main/Notebooks/examples/bbbc021_compound_screen.ipynb)** using Jupyter.
- Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AAitorG/PhenoMe/blob/main/Notebooks/examples/bbbc021_compound_screen.ipynb)

**Notebook 2**
- Local installation: Open the **[BBBC014 - Cytoplasm–nucleus translocation](https://github.com/AAitorG/PhenoMe/blob/main/Notebooks/examples/bbbc014_two_cell_lines.ipynb)** using Jupyter.
- Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AAitorG/PhenoMe/blob/main/Notebooks/examples/bbbc014_two_cell_lines.ipynb)

## Exercise 3
**Process and explore your dataset** You will have the opportunity to load and explore your datasets using the workflow introduced in the previous exercises.

**DATASET REQUIREMENTS**: PhenoMe is compatible with 2D image collections of different types (multichannel images, images with their corresponding segmentation mask, time-lapse images). Preferably, images should be in TIF format and organized in folders corresponding to the different conditions (e.g., experimental replica, treatment).

**Notebook (same as in Exercise 1)** PhenoMe/Notebooks/tutorials/01_quickstart:
- Local installation: Open the **[Interactive Quickstart Notebook](https://github.com/AAitorG/PhenoMe/blob/main/Notebooks/tutorials/01_interactive_quickstart.ipynb)** using Jupyter.
- Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AAitorG/PhenoMe/blob/main/Notebooks/tutorials/01_interactive_quickstart.ipynb)


# Troubleshooting macOS
**Creation of Conda environment** for osx-arm64 platform (macOS). Download the [conda spec file](https://drive.google.com/file/d/1w3r_1wN7YYjSdSfE_c3K5RsrH3JtTCzx/view?usp=sharing) and run the following command in your terminal.
````terminal
# This file may be used to create an environment using:
conda create --name phenome-cpu --file spec-file.txt
````
**Creation of a conda environment using requirements**. Download the [requirements file](https://drive.google.com/file/d/1TVa3DlGG0a-OCGKHiukHxkOmTqGIljyf/view?usp=sharing) and run the following command in your terminal.
````terminal
# This file may be used to create an environment using:
conda create --name phenome-cpu python=3.12 pip
conda activate phenome-cpu
pip install -r requirements.txt
````



### Acknowledgements
This community workshop is part of the activities of AIM-Net (RED2024-153844-T, funded by MICIU/AEI/10.13039/501100011033).