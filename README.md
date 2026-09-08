# IRuDD: A Large-Scale Real-World Dataset for Industrial Rubber Defect Detection

Official repository for the paper: **"IRuDD: A Large-Scale Real-World Dataset for Industrial Rubber Defect Detection"** <!-- presented at **ICECCME 2026**, Bali, Indonesia.-->

[[Paper (PDF)]](https://github.com/arashlagzian/IRuDD---ICECCME-IEEE-2026/blob/master/ICECCME2026___IRuDD%20camera%20ready%20version.pdf) [[Presentation Video]](https://drive.google.com/file/d/1esP9sYjwfTw47rMO12hG3avs7fZbbbG6/view?usp=sharing)
---

## 📌 Overview
**IRuDD** is a comprehensive, high-resolution dataset designed to bridge the gap between academic research and real-world industrial application. It features **20,828 genuine rubber surface images** collected directly from production lines. 

Unlike many existing datasets, IRuDD contains **zero synthetic defects**, providing a realistic benchmark for small object detection and quality control in manufacturing environments.

## 📊 Key Statistics

| Property | Value |
| :--- | :--- |
| **Total Images** | 20,828 |
| **Total Annotations** | 66,492 |
| **Image Resolution** | 960 × 1280 (High-Res RGB) |
| **Defect-to-Surface Ratio** | 0.2 (Challenging small objects) |
| **Formats** | YOLO (.txt) and COCO (.json) |
| **Annotator** | Human experts (three annotators) |
| **Annotation Tool** | Label Studio |

## 🚀 Performance Benchmarks
We established strong baselines using state-of-the-art (SOTA) object detection models:


| Model | Backbone | Precision | Recall | mAP@50 | mAP@50-90 |
| :--- | :--- | :---: | :---: | :---: | :---: |
| Faster-RCNN | ResNet-50 | 69.15 | 83.62 | 61.05 | 63.08 |
| Faster-RCNN | VGG-16 | 74.81 | 80.51 | 74.81 | **76.10** |
| Faster-RCNN | MobileNetV3 | 53.96 | 65.34 | 58.65 | 57.40 |
| YOLOv5 | CSPDarknet53 | **94.10** | **96.00** | **98.00** | <u>65.50</u> |
| YOLOv7 | E-ELAN | 64.30 | 65.20 | 69.80 | 35.60 |
| YOLOv8 | Custom-CSPDarknet53 | <u>92.10</u> | <u>91.20</u> | <u>96.50</u> | 64.10 |
| YOLOv10 | CSPNet | 89.30 | 85.60 | 93.50 | 60.30 |
| RT-DETR (b=4) | ResNet | 57.90 | 47.60 | 56.20 | 23.90 |
| RT-DETR (b=8) | ResNet | 64.70 | 55.90 | 65.90 | 28.60 |
| HIC-YOLOv5 | CSP | 56.14 | 58.20 | 57.72 | 27.05 |


## 📁 Dataset Structure
To use this dataset with standard training pipelines (like Ultralytics), organize your directories as follows:

```bash
IRuDD/
├── data.yaml            # Dataset configuration file
├── train/
│   ├── images/          # 16,662 images
│   └── labels/          # YOLO format .txt files
├── val/
│   ├── images/          # 2,083 images
│   └── labels/          # YOLO format .txt files
└── test/
    ├── images/          # 2,083 images
    └── labels/          # YOLO format .txt files
```

## 🛠️ Getting Started
1. **Clone the Repo:**
   ```bash
   git clone https://github.com/arashlagzian/IRuDD
   cd IRuDD
   ```
2. **Download Data:**
   The dataset will be publicly released on [Kaggle/Roboflow] upon formal paper acceptance. [Link coming soon].

## 📝 Citation
If you find this dataset useful for your research, please cite our work:
```bibtex
@inproceedings{lagzian2026irudd,
  title={{IRuDD}: A Large-Scale Real-World Dataset for Industrial Rubber Defect Detection},
  author={Lagzian, Arash and Mollaee, Saeed and Shahi, Leila and Beigy, Hamid},
  booktitle={Proc. of the International Conference on Electrical, Computer, Communications and Mechatronics Engineering (ICECCME)},
  year={2026}
}
```

## 📧 Contact
For any questions regarding the dataset or collaboration, please contact:
*   **Arash Lagzian:** arash.lagzian94@gmail.com

---
*Note: This dataset is for academic and research purposes.*
