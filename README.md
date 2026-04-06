# 🚨 FloodGuard Saudi Arabia

AI-powered flood detection and alerting system for safer driving.

FloodGuard is a computer vision project that analyzes flood-related road images to detect flooded scenes, identify affected objects, and segment water regions. Built to address sudden flooding risks in Saudi Arabia, where road conditions can become dangerous within minutes.


## Why this matters

Flooding can make roads dangerous within minutes, especially during sudden rainfall. In Saudi Arabia, a fast and reliable flood detection system can help support early warnings, improve road safety, and assist decision-making before drivers enter risky areas.

## Key highlights

- Classifies images as flood or no-flood.
- Detects flooded objects and flood-affected regions.
- Segments water areas at pixel level.
- Compares classical ML and deep learning approaches.
- Evaluates multiple models across several public datasets.

## Tech stack

Python • PyTorch • OpenCV • Scikit-learn • NumPy • Matplotlib • Ultralytics YOLO • Google Colab

## Dataset preview


## Results

### Table 1. Classical classification results.
| Model | Feature Extraction | Train Accuracy | Train Precision | Train Recall | CV Accuracy |
|---|---|---:|---:|---:|---:|
| SVM | HOG | 0.6265 | 0.6355 | 0.6265 | 0.6449 |
| SVM | LBP | 0.7217 | 0.7230 | 0.2981 | 0.7042 |
| ANN | HOG | 0.7175 | 0.7121 | 0.7175 | 0.6931 |

### Table 2. CNN classification results.
| Model | Dataset | Train Accuracy | Train Precision | Train Recall | Train F1 | CV Accuracy |
|---|---|---|---:|---:|---:|---:|
| EfficientNet | Flood | 0.91 | 0.91 | 0.91 | 0.91 | 0.9848 |
| MobileNet | Flood | 0.98 | 0.82 | 0.84 | 0.82 | 0.9870 |
| Inception | Flood/NoFlood | 0.95 | 0.95 | 0.95 | 0.95 | 0.9300 |

### Table 3. Detection model results.
| Model | Dataset | Train Precision | Train Recall | Train mAP50 | CV Precision | CV Recall | CV mAP50 |
|---|---|---:|---:|---:|---:|---:|---:|
| YOLOv5 | Flooded Objects | 0.73 | 0.77 | 0.76 | 0.69 | 0.67 | 0.69 |
| YOLOv8 | Flood Area | 0.73 | 0.56 | 0.62 | 0.88 | 0.84 | 0.92 |
| YOLOv11 | Flooded Objects | 0.68 | 0.81 | 0.78 | 0.79 | 0.74 | 0.81 |

## Main findings

- HOG and LBP performed better than SIFT and ORB in classical classification experiments.
- CNN-based models consistently outperformed classical machine learning approaches.
- EfficientNet, MobileNet, and Inception gave strong classification results.
- YOLOv8 performed well for both detection and segmentation tasks.
- The best model depended on the dataset and task, showing that flood monitoring is not a one-model problem.

## How to run

1. Open the notebook.
2. Upload the required datasets.
3. Run the cells in order.
4. Review the training outputs and evaluation metrics.

## Requirements

- Python 3.9+
- PyTorch
- OpenCV
- NumPy
- Matplotlib
- Scikit-learn
- Ultralytics
- Pandas

