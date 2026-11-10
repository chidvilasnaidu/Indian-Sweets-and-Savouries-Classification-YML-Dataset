# Indian Sweets & Savouries Dataset: 132 Classes | YOLO Object Detection | Computer Vision

## 1. Dataset Files & Download Guide

This Kaggle upload contains **four files**, organized to provide flexibility for researchers, developers, and machine learning practitioners.

| File | Description |
|---|---|
| `RAW-Indian-Sweets-Classification-dataset` | RAW dataset containing the original images and their corresponding labels, without the train/validation/test split. |
| `Cleaned-Indian-Sweets-Classification-dataset` | Cleaned and organized dataset containing separate training, validation, and testing directories, along with the YOLO `data.yaml` configuration file. |
| `Configuration_of_Custum_DataSet.ipynb` | Jupyter Notebook containing the dataset configuration and preparation workflow. |
| `best.pt` | Trained YOLO model weights, representing the best-performing checkpoint saved during training. |

### Which file should you download?

**Recommended: Cleaned Dataset**

If you want to directly train a YOLO model, download the **Cleaned Dataset**. It already contains:

- Training images and labels.
- Validation images and labels.
- Testing images and labels.
- YOLO dataset configuration (`data.yaml`).

The directory structure is organized and ready for integration into an Ultralytics YOLO training pipeline, subject to updating the dataset root path.

**RAW Dataset**

The RAW version is provided for users who prefer working with the original image and annotation collection before applying their own train/validation/test splitting, preprocessing, or dataset preparation strategies.

**Trained Model (`best.pt`)**

The `best.pt` file provides the trained model checkpoint for users interested in exploring inference and object detection without starting model training from scratch.

**Configuration Notebook**

The accompanying Jupyter Notebook provides additional insight into the dataset preparation and configuration process.

---

## 2. Dataset Overview

The Indian Sweets & Savouries Dataset is a specialized computer vision dataset developed to support deep learning research, multi-class object detection, and visual recognition of India's diverse culinary heritage.

[Continue with the existing Dataset Overview, Dataset Statistics, Categories, Annotation Format, YOLO Training, Research Applications and Future Scope sections.]

## 3. License, Usage & Image Attribution Notice

**Important: Educational and Research Purposes Only**

This dataset has been developed and shared primarily for educational, academic, experimentation, and non-commercial research purposes.

Some images included in this dataset were collected from publicly accessible sources on the internet, including Google Images. These images may belong to their respective original creators, photographers, websites, or copyright holders.

I do not claim ownership or exclusive copyright over third-party images included in this collection.

The dataset is shared as an educational computer vision resource to encourage experimentation with:

- Artificial Intelligence (AI)
- Machine Learning (ML)
- Deep Learning
- Computer Vision
- YOLO Object Detection
- Indian Food Recognition and Classification
- Academic and Research Projects

### Usage Restrictions and Responsibilities

1. This dataset is intended for educational and non-commercial research purposes.
2. No commercial usage rights are granted for third-party images through this dataset.
3. Users are responsible for independently verifying the copyright, licensing, attribution, and usage permissions of individual images before reusing or redistributing them.
4. Redistribution or commercial exploitation of third-party images must not be assumed to be permitted.
5. The dataset creator does not guarantee ownership or licensing clearance for third-party visual content.

### Copyright Concerns & Image Removal Requests

If you are an original image owner, photographer, copyright holder, or authorized representative and believe that any image included in this dataset infringes your intellectual property rights, please contact me.

**Email:** chidvilasnaidu99@gmail.com

Please provide the relevant image identification or source URL and details of your ownership or concern. I will review the request and take appropriate action, including removing the disputed image from the dataset where warranted.

I respect the rights of original creators and welcome genuine copyright concerns.

### A Note from the Creator

This project was independently developed with an educational objective: to explore the application of Artificial Intelligence and Computer Vision in recognizing and preserving India's diverse culinary heritage.

It is not intended to exploit the intellectual property of original image creators or to claim ownership of their work.

Thank you for understanding and supporting this educational initiative.

---
## What Makes This Dataset Unique?

To the best of my knowledge, there is a lack of publicly available, dedicated, large-scale computer vision datasets specifically focused on the diverse varieties of Indian sweets.

Existing food datasets generally focus on broader food categories, while the regional diversity and individual identities of Indian sweets deserve more dedicated attention.

This project aims to contribute towards filling that gap by bringing together India's traditional and modern sweet varieties in a unified dataset.

A small step towards making India's rich culinary heritage recognisable through Artificial Intelligence.

## Categories Covered

The dataset covers seven broad dimensions of Indian sweet varieties and creations:

**Traditional Sweets**: Sweets deeply rooted in Indian culture, customs, and generations of culinary traditions.

**Authentic Sweets**: Regional delicacies prepared using traditional ingredients, methods, and distinctive local flavours.

**Customized Sweets**: Personalised sweet creations with variations in ingredients, shapes, designs, and presentation.

**Fancy Sweets**: Decorative and premium sweets, often associated with celebrations, gifting, and special occasions.

**Creative Sweets**: Innovative sweet creations featuring new combinations, designs, and presentations.

**Inspired Sweets**: Modern creations inspired by traditional Indian sweets and international dessert concepts.

**Fusion Sweets**: A combination of Indian traditional flavours with contemporary and international culinary influences.

## Regional & Cultural Diversity

India's sweet heritage goes far beyond a handful of popular desserts.

This dataset aims to represent sweets from different Indian states and regions, including traditional specialities and major GI-recognised sweet products.

From the famous Bengali sweets to the rich delicacies of Rajasthan, from Andhra Pradesh's traditional preparations to the iconic sweets of Tamil Nadu, every regional speciality represents a part of India's cultural identity.

The goal is to celebrate this diversity through a unified computer vision dataset.


---
## 📊 Dataset Information

| Attribute | Details |
|---|---|
| Dataset Name | Indian Sweets & Savouries |
| Domain | Indian Food & Culinary Heritage |
| Total Classes | 132 |
| Task | Object Detection |
| Annotation Format | YOLO |
| Configuration | data.yaml |
| Framework | Ultralytics YOLO |
| Dataset Format | Images and YOLO annotations |
| Application | Computer Vision & Food Recognition |

##  Potential Applications

This dataset can be useful for:

- Indian sweet and food recognition systems.
- Deep learning and computer vision research.
- YOLO-based object detection projects.
- Regional food identification applications.
- Smart food classification systems.
- Indian culinary heritage documentation.
- AI-powered food discovery applications.
- Educational and academic research.

## Getting Started

The dataset is organised for YOLO-based object detection.

### 1. Install Ultralytics

```bash
pip install ultralytics
```

### 2. Download the Dataset

Download and extract the dataset from Kaggle.

### 3. Configure the Dataset

Locate the `data.yaml` configuration file and verify the dataset paths.

Example:

```yaml
path: /path/to/dataset

train: train/images
val: val/images
test: test/images

nc: 132

names: [...]
```

Make sure the paths match the actual extracted directory structure.

### 4. Train a YOLO Model

```python
from ultralytics import YOLO

model = YOLO("yolov8m.pt")

results = model.train(
    data="data.yaml",
    epochs=20,
    imgsz=640
)
```

### 5. Run Predictions

```python
from ultralytics import YOLO

model = YOLO("runs/detect/train/weights/best.pt")

results = model.predict(
    source="test/images",
    conf=0.25,
    save=True
)
```

---

## 4. Acknowledgement

Indian sweets are more than food. They represent culture, traditions, regional identities, celebrations, and generations of culinary craftsmanship.

This project is a small attempt to bring India's rich culinary diversity into the world of Artificial Intelligence.

**Preserving Tradition. Enabling Recognition. Advancing AI.**

May your Diwali be as sweet as India's incredible culinary heritage!

Happy Diwali!
