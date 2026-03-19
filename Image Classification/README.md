# 🛍️ Image Classification

A machine learning project that classifies images into categories using a Support Vector Machine (SVM) — built with scikit-learn and scikit-image.

---

## 📌 Overview

This project builds an image classifier capable of distinguishing between four product categories from an image dataset:

| Label | Category |
|-------|----------|
| 0 | 🌸 Flowers |
| 1 | 🦋 Butterfly |
| 2 | 👕 T-Shirt |
| 3 | 📺 TV |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| NumPy | Numerical operations |
| Matplotlib | Image loading & visualization |
| Seaborn | Confusion matrix heatmap |
| scikit-learn | SVM model, train/test split, metrics |
| scikit-image | Image resizing |
| glob | File path collection |

---

## 📁 Project Structure

```
📦 image-classification
 ┣ 📓 Image_Classification_Project.ipynb     # Main notebook
 ┗ 📂  products/
    ┣ 🌸 flowers/        # Flower images (.jpg)
    ┣ 🦋 Butterfly/      # Butterfly images (Image_*.jpg)
    ┣ 👕 tshirt/         # T-shirt images (.jpg)
    ┗ 📺 tv/             # TV images (.jpg)
```

---

## ⚙️ Pipeline

```
Load Images → Assign Labels → Shuffle → Resize to 300×300
     → Flatten → Train/Test Split → SVM → Evaluate
```

1. **Load** — Collect image paths using `glob` for all four categories
2. **Label** — Assign integer labels (0–3) to each image
3. **Shuffle** — Randomize image-label pairs using `sklearn.utils.shuffle`
4. **Resize** — Standardize all images to `(300, 300, 3)` using `skimage`
5. **Flatten** — Reshape each image into a 1D feature vector (`270,000` features)
6. **Split** — 80/20 train-test split
7. **Train** — Fit a Support Vector Classifier (`SVC`)
8. **Evaluate** — Accuracy score, confusion matrix, and classification report





---

## 📊 Evaluation

The model is evaluated using:

- **Accuracy Score** — Overall classification accuracy
- **Confusion Matrix** — Visualized as a Seaborn heatmap
- **Classification Report** — Per-class precision, recall, and F1-score

---

## 💡 Applications

- 🏪 Automated product tagging for online stores
- 🔍 Visual search and recommendation systems
- 📦 Inventory categorization pipelines
- 🧪 Baseline for deep learning image classifiers

---

