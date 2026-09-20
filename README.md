#  Implementation of a Camera-Based Traffic Violation Detection System Using Computer Vision

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/YOLOv8-Ultralytics-purple?logo=yolo&logoColor=white" />
  <img src="https://img.shields.io/badge/Faster%20R--CNN-Torchvision-orange?logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/Platform-Google%20Colab-yellow?logo=googlecolab&logoColor=white" />
</p>

---

## Project Overview

This project presents a **camera-based traffic violation detection system** using deep learning computer vision techniques. Two object detection architectures are implemented and compared:

- **YOLOv8** — A real-time, single-stage detector known for its speed.
- **Faster R-CNN** — A two-stage detector known for its accuracy.

The goal is to evaluate the trade-off between **speed** and **accuracy** for detecting traffic violations from camera footage.

---

## Project Structure

```
Project-RM/
violation_detection.ipynb   # Main notebook: preprocessing, training, evaluation
```

---

## Model Evaluation Results

The table below summarizes the performance of both models on the test dataset:

| Metric              | YOLOv8        | Faster R-CNN  |
|---------------------|:-------------:|:-------------:|
| **Precision**        | 0.7986        | **0.9770**    |
| **Recall**           | 0.7713        | **0.9762**    |
| **F1-Score**         | 0.7848        | **0.9759**    |
| **Inference Time**   | **6.48 ms**   | 32.60 ms      |
| **FPS**              | **154.35**    | 30.68         |
| **AUC (micro-avg)**  | 0.8367        | **0.9851**    |

---

## Analysis

### YOLOv8 — Speed Champion
- Achieves an extremely high inference speed of **154.35 FPS** (6.48 ms/frame)
- Suitable for **real-time** traffic monitoring systems
- Slightly lower accuracy compared to Faster R-CNN

### Faster R-CNN — Accuracy Champion
- Achieves superior accuracy with **Precision: 0.977**, **Recall: 0.976**, and **AUC: 0.985**
- More reliable in detecting violations with fewer false positives
- Slower inference at **30.68 FPS** (32.60 ms/frame)

### Conclusion
> **Faster R-CNN** outperforms YOLOv8 in accuracy across all metrics (Precision, Recall, F1-Score, AUC), making it more suitable when detection correctness is the priority. However, **YOLOv8** is significantly faster (~5× FPS), making it the better choice for real-time applications where speed is critical.

---

## Tools & Libraries

| Category        | Tools                                      |
|-----------------|--------------------------------------------|
| Language        | Python 3.x                                 |
| Deep Learning   | PyTorch, Ultralytics (YOLOv8), Torchvision |
| Data Processing | NumPy, Pandas, OpenCV                      |
| Visualization   | Matplotlib, Seaborn                        |
| Platform        | Google Colaboratory                        |

---

## How to Run

1. Open `violation_detection.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Upload the notebook and dataset
3. Run all cells sequentially from top to bottom

---

## Author

**lxgann**  
Research Methodology Project - Semester 4  
[GitHub Profile](https://github.com/lxgann)

**briansnjya**  
Research Methodology Project - Semester 4
[GitHub Profile](https://github.com/briansnjya).
