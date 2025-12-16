# Multi-Type-Road-Surface-Dataset-MTRSD

This repository provides a **Multi-Type-Road-Surface-Dataset** for road surface recognition tasks, including six road surfaces with ambient illuminance data and encompassing unstructured and heterogeneous road surfaces. The dataset is designed to support supervised classification of different road surface types under varying illumination conditions.

After the paper is accepted, the dataset will be uploaded fully.

---

## 1. Dataset Overview

The dataset consists of RGB road surface images collected under real-world lighting conditions. Each image is associated with:

* A **road surface category label** (derived from the filename prefix)
* An optional **illumination value** encoded in the filename

The dataset supports illumination-aware preprocessing and grayscale–RGB fusion for robust road surface recognition.

### Supported Road Surface Categories

| Class Tag | Class ID | Description                 |
| --------- | -------- | --------------------------- |
| BY        | 0        | Asphalt Pavement (AP)       |
| SN        | 1        | Cement Pavement (CP)        |
| TL        | 2        | Earth Surface (ES)          |
| CD        | 3        | Grass Surface (GS)          |
| CS        | 4        | Grass Gravel Surface (GGS)  |
| CT        | 5        | Grass Earth Surface  (GES)  |

---

## 2. Directory Structure

The dataset directory is organized as follows:

```
root_path/
├── train/
│   ├── image_001_xxx_illumination.jpg
│   ├── image_002_xxx_illumination.jpg
│   └── ...
├── test/
│   ├── image_101_xxx_illumination.jpg
│   └── ...
```

* `train/`: training images
* `test/`: testing images

Image filenames must follow the format:

```
<ClassTag>_<SequenceNumber>_<VibrationValue>_<IlluminanceValue>.jpg
```

The **first character** defines the class label, and the **last numeric field** represents the illumination value.

---

## 3. License

This dataset and code are released for **academic and research use only** with license **CC BY 4.0**.

If you use this dataset or code in your research, please cite the corresponding paper or project.
