# HIT-UAV Thermal Object Detection 🔥🚁

This project uses **Ultralytics YOLOv11** to detect objects in **thermal UAV (infrared) imagery**, based on the HIT-UAV dataset.

## 🧩 Features
- Thermal-aware preprocessing (CLAHE enhancement)
- Conversion from grayscale → RGB for YOLO compatibility
- YOLOv11 training using AdamW optimizer and cosine LR scheduler
- Model export to `.pt` and `.onnx` for deployment

## 🧠 Dataset
The dataset used is **HIT-UAV** (High-Altitude Infrared Thermal UAV Dataset).  
If using locally, update the dataset path inside the notebook:
```python
ROOT_DIR = '/path/to/hit-uav-dataset'
```

## ⚙️ Setup
```bash
pip install -r requirements.txt
```

## 🚀 Run
You can open and run the notebook directly in **Google Colab**:
```bash
jupyter notebook hit-uav.ipynb
```

## 📦 Exporting the Model
After training:
- The best weights are saved under `runs/detect/exp*/weights/best.pt`
- Export to ONNX:
```python
model.export(format='onnx')
```

## 📜 Results
| Model | Input Type | mAP@50 | Output Format |
|--------|-------------|--------|----------------|
| YOLOv11 | Thermal RGB | 89.2% | .pt, .onnx |

---

**Author:** Dinesh Kumar  
**License:** MIT
