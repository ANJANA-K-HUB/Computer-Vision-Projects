# 🚗 Number Plate Detection & Blurring

A computer vision project that automatically detects vehicle license plates in images and applies privacy blurring using OpenCV's Haar Cascade classifier.

---

## 📌 Overview

This project uses classical computer vision techniques to:
- **Detect** license plates in car images
- **Visualize** detections with bounding boxes
- **Blur** detected plates for privacy anonymization

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| OpenCV (`cv2`) | Image processing & plate detection |
| NumPy | Array operations |
| Matplotlib | Image display |

---

## 📁 Project Structure

```
📦 number-plate-detection
 ┣ 📓 Number_Plate_Detection_Project.ipynb   # Main notebook
 ┣ 🖼️ car.jpg                                # Sample input image
 ┗ 🔍 haarcascade_russian_plate_number.xml   # Pre-trained Haar Cascade model
```

---

## ⚙️ How It Works

1. **Load & Convert** — Read the car image and convert from BGR to RGB
2. **Load Classifier** — Initialize OpenCV's `CascadeClassifier` with the Haar Cascade XML model
3. **Detect** — Run `detectMultiScale()` to locate plate regions
4. **Output** — Either draw bounding boxes or blur the plate region

```
Input Image → Haar Cascade Detection → Bounding Box / Blur Output

---



## 🧠 Core Functions

### `detect_plate(img)`
Detects license plates and draws red bounding boxes around them.

```python
result = detect_plate(img)
display(result)
```

### `detect_and_blur_plate(img)`
Detects license plates and applies a median blur to anonymize them.

```python
result = detect_and_blur_plate(img)
display(result)
```

---

## 📷 Sample Output

| Mode | Description |
|------|-------------|
| Detection | Red rectangle drawn around the detected plate |
| Blurring | Plate region replaced with a median-blurred version |

---

## 💡 Applications

- 🚦 Traffic surveillance systems
- 🗺️ Privacy protection in street-view imagery
- 🅿️ Automated parking management
- 📹 CCTV footage anonymization

---

