# EdgeFormerNet++: A Hybrid Attention-Guided Transformer Network for Accurate Retinal Layer Segmentation in OCT Images
### Manuscript ID: IEEE LATAM Submission ID: 10551
#### Authors and Affiliations:
- Anju Thomas (Department of Electronics and Communication Engineering,National Institute of Technology Tiruchirappalli, Tamil Nadu, India., Department of Sensor & Biomedical Technology, School of Electronics Engineering, Vellore Institute of Technology,Vellore, India.)
- Farhin Janath S. J. (Department of Electronics and Electronics Engineering, Government Engineering College, Barton Hill, Trivandrum, Kerala, India.)
- Vijayalakshmi P (Department of Electronics and Electronics Engineering, Government Engineering College, Barton Hill, Trivandrum, Kerala, India.)
-  Nisan Pranavah Raja (Department of Electronics and Communication Engineering,National Institute of Technology Tiruchirappalli, Tamil Nadu, India.)
-   P. Palanisamy (Department of Electronics and Communication Engineering,National Institute of Technology Tiruchirappalli, Tamil Nadu, India.)
-   Varun P. Gopi (Department of Electronics and Communication Engineering,National Institute of Technology Tiruchirappalli, Tamil Nadu, India.)

  
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

---
| Dataset | Purpose |
|----------|----------|
| MGU Dataset | Macular layer segmentation |
| NR206 Dataset | Peripappilary layer segmentation |
## Installation

### Clone Repository

```bash
git clone https://github.com/anjunitt/EdgeFormerNet-A-Hybrid-Attention-Guided-Transformer-Network-for-Accurate-Retinal-Layer-Segmentat.git
cd EdgeFormerNet-A-Hybrid-Attention-Guided-Transformer-Network-for-Accurate-Retinal-Layer-Segmentat
```

### Create Environment

```bash
python -m venv venv
```

### Activate Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Dataset Organization

### MGU Dataset

```text
MGU/
├── train/
│   ├── img/
│   └── mask/
│
├── eval/
│   ├── img/
│   └── mask/
```

### NR206 Dataset

```text
NR206/
├── train/
├── train_labels/
├── val/
└── val_labels/
```

---

## Running MGU Training

```bash
python MGU/train_mgu.py
```

---

## Running NR206 Training

```bash
python NR206/train_nr206.py
```

---

## Testing

### MGU

```bash
python MGU/test_mgu.py
```

### NR206

```bash
python NR206/test_nr206.py
```

---

## Expected Outputs

The best-performing model is automatically saved as:

```text
EdgeFormer_Dice85_best_val_loss_xxxxx.h5
```

Evaluation metrics include:

- Dice Score
- Intersection over Union (IoU)
- Pixel Accuracy

---

## Requirements

```text
tensorflow==2.10.0
numpy
Pillow
albumentations
opencv-python
matplotlib
scikit-learn
scipy
pandas
h5py
```

---

## Citation

Citation information will be updated once the manuscript is published.

## License

This project is released for academic and research purposes.
