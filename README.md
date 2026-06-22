# EdgeFormerNet++: A Hybrid Attention-Guided Transformer Network for Accurate Retinal Layer Segmentation in OCT Images
# Manuscript ID: IEEE LATAM Submission ID: 10551
# Authors: Anju Thomas, Farhin Janath S. J., Vijayalakshmi P, Nisan Pranavah Raja, P. Palanisamy,Varun P. Gopi
This repository contains the complete training and testing implementation of **EdgeFormerNet++**, a hybrid CNN–Transformer-based segmentation framework for retinal layer segmentation from OCT images.

The code includes:

- OCT image and mask loading
- Automatic mask color extraction
- Data augmentation
- EdgeFormerNet++ model training
- Hybrid Dice–Tversky loss
- Dice and IoU evaluation
- Per-layer segmentation performance
- Model complexity analysis
- Inference time and FPS calculation

## Project Objective

The aim of this work is to accurately segment retinal layers from OCT images using a lightweight hybrid attention-guided transformer network.

The model is designed for segmentation of 9 retinal layers such as:

- RNFL
- GCL
- IPL
- INL
- OPL
- ONL
- IS/OS
- RPE
- Choroid

# Install the required libraries:
pip install tensorflow numpy pillow albumentations opencv-python scikit-learn matplotlib

  ## Dataset Structure
For the **NR dataset**, arrange the dataset as follows:

```text
oct_dataset
│
├── train
│   ├── img
│   └── mask
│
├── eval
│   ├── img
│   └── mask
│
└── test
    ├── img
    └── mask
