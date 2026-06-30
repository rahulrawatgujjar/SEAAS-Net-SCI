# SEAAS-Net

Official repository for the paper:

**SEAAS-Net: Squeeze-Excitation Attention with Adaptive Suppression for Source Camera Identification**

## Overview

SEAAS-Net is a deep learning framework for source camera identification. The proposed architecture employs SEAAS (Squeeze-Excitation Attention with Adaptive Suppression) blocks to suppress scene content and enhance camera-specific traces for robust camera model recognition.

The framework consists of three main stages:

1. Patch-Level Processing
2. Preprocessing Head
3. Classification Head

---

## Reproducibility Resources

This repository provides an evaluation notebook that reproduces the reported results on the Dresden dataset using the released pretrained model and test patches.

### Kaggle Resources

### Pretrained SEAAS-Net Model

https://www.kaggle.com/models/rahulrawatgujjar/best-seaas-model

### Dresden Test Patches

https://www.kaggle.com/datasets/rahulrawatgujjar/dresden-test-patches

### Dataset Splits

This repository also includes `train_images.json` and `test_images.json` files for the following splits:

* `dresden_split`
* `forchheim_split`
* `vision_split`

### Public Dataset Links

* Forchheim Dataset: https://faui1-files.cs.fau.de/public/mmsec/datasets/fodb/
* Dresden Dataset: https://www.kaggle.com/datasets/micscodes/dresden-image-database
* Vision Dataset: https://lesc.dinfo.unifi.it/VISION/

---

## Contents

* Pretrained SEAAS-Net model (Kaggle)
* Dresden test patches (Kaggle)
* train_images.json and test_images.json for dresden_split, forchheim_split, and vision_split
* Public links for the Dresden, Forchheim, and Vision datasets
* Evaluation notebook
* Requirements file

The evaluation notebook reproduces the reported:

* Patch-Level Accuracy
* Image-Level Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

---

## Citation

If you find this work useful in your research, please cite:

> Citation information will be updated after publication.

---

## Authors

* Rahul Rawat, National Institute of Technology Kurukshetra, India
* Vishwas Rathi, National Institute of Technology Kurukshetra, India

---

## Contact

**Rahul Rawat**

[324103106@nitkkr.ac.in](mailto:324103106@nitkkr.ac.in)

**Dr. Vishwas Rathi**

[vishwas@nitkkr.ac.in](mailto:vishwas@nitkkr.ac.in)
