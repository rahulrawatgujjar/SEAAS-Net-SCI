# SEAAS-Net

Official repository for the paper:

**SEAAS-Net: Squeeze-Excitation Attention with Adaptive Suppression for Source Camera Identification**

## Overview

SEAAS-Net is a deep learning framework for source camera identification. The proposed architecture employs SEAAS (Squeeze-Excitation Attention with Adaptive Suppression) blocks to suppress scene content and enhance camera-specific traces for robust camera model recognition.

The framework consists of three main stages:

1. Patch-Level Processing
2. Preprocessing Head
3. Classification Head

## What This Repo Contains

This repository is set up to reproduce the Dresden evaluation reported in the paper. It includes:

* `SEAAS-Net_Reproducibility.ipynb` - the evaluation notebook
* `pretrained_seaasnet_model/` - the pretrained model used by the notebook
* `dresden_split/`, `forchheim_split/`, `vision_split/` - dataset split JSON files
* `dresden_test_patches/` - Dresden test patches directory
* `requirements.txt` - Python dependencies

The notebook runs the full evaluation pipeline:

1. Loads the pretrained SEAAS-Net model.
2. Loads the Dresden test patches.
3. Runs patch-level prediction.
4. Applies majority voting to produce image-level predictions.
5. Reports the evaluation metrics.
6. Displays the confusion matrix.

## Prerequisites

* Python 3.10 or newer
* `pip`
* A Kaggle account if you need to download the Dresden test patches yourself

The pretrained model is already included in this repository, so you do not need to download it separately.

## Step-By-Step Setup

### 1. Clone the repository

```bash
git clone <repository-url>
cd SEAAS-Net-SCI
```

### 2. Create and activate a virtual environment

On Linux:

```bash
python3 -m venv venv
source venv/bin/activate
```

If you are using another shell or operating system, activate the virtual environment with the command for that platform.

### 3. Upgrade `pip`

```bash
python -m pip install --upgrade pip
```

### 4. Install the dependencies

```bash
pip install -r requirements.txt
```

If you want to run the notebook from Jupyter, the dependencies in `requirements.txt` are enough for the current reproducibility workflow.

### 5. Check that the required files are present

Make sure these paths exist before running the notebook:

```bash
ls pretrained_seaasnet_model
ls dresden_test_patches
ls dresden_split
ls forchheim_split
ls vision_split
```

You should see `seaasnet_dresden.keras` inside `pretrained_seaasnet_model/`. The notebook expects `dresden_test_patches/` to contain the Dresden patch folders directly.

## Downloading the Dresden Test Patches

If you do not already have the Dresden test patches in this repository, download them from Kaggle and extract them so the directory structure matches `dresden_test_patches/`.

Dataset link:

* https://www.kaggle.com/datasets/rahulrawatgujjar/dresden-test-patches

Download and extract the dataset so the directory structure matches `dresden_test_patches/`.

## Running the Notebook

### Option 1: Run from Jupyter

```bash
jupyter notebook SEAAS-Net_Reproducibility.ipynb
```

If you prefer JupyterLab:

```bash
jupyter lab SEAAS-Net_Reproducibility.ipynb
```

### Option 2: Run from VS Code

1. Open `SEAAS-Net_Reproducibility.ipynb`.
2. Select the Python interpreter from the virtual environment you created.
3. Run the cells from top to bottom.

## Expected Output

The notebook reproduces the Dresden evaluation and prints or plots the following results:

* Patch-level accuracy
* Image-level accuracy
* Precision
* Recall
* F1-score
* Image-level confusion matrix

## Public Dataset Links

* Forchheim Dataset: https://faui1-files.cs.fau.de/public/mmsec/datasets/fodb/
* Dresden Dataset: https://www.kaggle.com/datasets/micscodes/dresden-image-database
* Vision Dataset: https://lesc.dinfo.unifi.it/VISION/

## Citation

If you find this work useful in your research, please cite:

> Citation information will be updated after publication.

## Authors

* Rahul Rawat, National Institute of Technology Kurukshetra, India
* Vishwas Rathi, National Institute of Technology Kurukshetra, India

## Contact

**Rahul Rawat**

[324103106@nitkkr.ac.in](mailto:324103106@nitkkr.ac.in)

**Dr. Vishwas Rathi**

[vishwas@nitkkr.ac.in](mailto:vishwas@nitkkr.ac.in)
