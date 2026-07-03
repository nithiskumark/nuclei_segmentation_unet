# 🧬 Biomedical Nuclei Instance Segmentation using U-Net

Deep Learning based biomedical image segmentation system for detecting and analyzing cell nuclei from microscopy images using **PyTorch**, **OpenCV**, and **U-Net**.

---

## 📌 Problem Statement

Manual identification and segmentation of cell nuclei from microscopy images is time-consuming, labor-intensive, and prone to human error. Researchers and pathologists often need to analyze hundreds of images to estimate cell count, morphology, and distribution.

The goal of this project is to automate nuclei segmentation and extract useful morphological features that can support biomedical image analysis.

---

## 💡 Solution

This project implements an end-to-end deep learning pipeline that:

- Loads microscopy images
- Generates instance segmentation masks using a U-Net model
- Detects individual nuclei using connected component analysis
- Extracts morphological features of each nucleus
- Visualizes segmentation results and detected nuclei

---

## 🚀 Features

- ✅ Biomedical image preprocessing
- ✅ U-Net based semantic segmentation
- ✅ Automatic nuclei detection
- ✅ Instance labeling using Connected Components
- ✅ Feature extraction
- ✅ Morphological analysis
- ✅ GPU Training (Google Colab T4)

---

# 📂 Dataset

Dataset Structure

```
data/
    train_data/
        <image_id>/
            images/
                <image_id>.png
            masks/
                mask1.png
                mask2.png
                ...
```

Each image contains multiple individual nucleus masks.

---

# 🏗️ Project Pipeline

```
Microscopy Image
        │
        ▼
Image Preprocessing
(OpenCV)
        │
        ▼
U-Net Model
(PyTorch)
        │
        ▼
Predicted Segmentation Mask
        │
        ▼
Connected Component Analysis
(scikit-image)
        │
        ▼
Individual Nuclei Detection
        │
        ▼
Feature Extraction
        │
        ▼
CSV Report + Visualization
```

---

# 🧠 Model Architecture

U-Net Encoder

↓

Feature Bottleneck

↓

Decoder with Skip Connections

↓

Binary Segmentation Mask

---

# 📊 Feature Extraction

For every detected nucleus:

- Area
- Perimeter
- Circularity
- Centroid
- -Eccentricity
- Extent
- Solidity

These features are stored inside a Pandas DataFrame for further analysis.

---

# 📈 Evaluation Metrics

- Dice Loss
- Binary Cross Entropy Loss
- Intersection over Union (IoU)
- Dice Score

---

# 🛠️ Tech Stack

| Tool | Purpose |
|-------|----------|
| Python | Programming |
| PyTorch | Deep Learning |
| OpenCV | Image Processing |
| scikit-image | Connected Components & Feature Extraction |
| NumPy | Numerical Operations |
| Pandas | Data Analysis |
| Matplotlib | Visualization |
| Google Colab | Model Training |

---

# 🧰 Tools Used

<p align="left">

<a href="https://www.python.org/">
<img src="https://skillicons.dev/icons?i=python" height="50"/>
</a>

<a href="https://pytorch.org/">
<img src="https://skillicons.dev/icons?i=pytorch" height="50"/>
</a>

<a href="https://opencv.org/">
<img src="https://upload.wikimedia.org/wikipedia/commons/3/32/OpenCV_Logo_with_text_svg_version.svg" height="50"/>
</a>

<a href="https://numpy.org/">
<img src="https://skillicons.dev/icons?i=python" height="50"/>
</a>

<a href="https://pandas.pydata.org/">
<img src="https://upload.wikimedia.org/wikipedia/commons/e/ed/Pandas_logo.svg" height="45"/>
</a>

<a href="https://scikit-image.org/">
<img src="https://scikit-image.org/docs/stable/_static/img/logo.png" height="50"/>
</a>

<a href="https://matplotlib.org/">
<img src="https://upload.wikimedia.org/wikipedia/commons/8/84/Matplotlib_icon.svg" height="50"/>
</a>

<a href="https://colab.research.google.com/">
<img src="https://colab.research.google.com/img/colab_favicon_256px.png" height="50"/>
</a>

</p>

-

If you found this project useful, consider giving it a ⭐ on GitHub.
