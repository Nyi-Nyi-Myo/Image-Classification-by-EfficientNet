# Image Classification by EfficientNet

This repository contains a complete pipeline for **multi-label image classification** of surgical instruments using **EfficientNet-B3** with custom dataset in PyTorch.

## 🚀 Highlights

- Model: `EfficientNet-B3` (from PyTorch Models)
- Task: Multi-label classification (one image could have multiple instruments)
- Classes: `G`, `HA`, `IS`, `M`, `NH` (5 classes total)
- Dataset Format: COCO-style with `.json` annotations and image folders
- Threshold Optimization for per-class F1
- Visualization of predictions with ground truth comparison

## 📁 Dataset Structure

```
root_dir/
├── train/
├── valid/
├── train_clean_updated.json
└── val_clean_updated.json
```

Each `.json` file follows COCO format and contains `file_name` and `labels` fields.

## 📊 Performance

- **Validation F1 (Best Epoch)**: 0.8285
- **Per-Class F1**:
  - `G`: 0.7983
  - `HA`: 0.7480
  - `IS`: 0.7789
  - `M`: 0.9703
  - `NH`: 0.8864

## 🧠 Notes

- The best model is automatically saved during training among 30 epochs.
- Thresholds for each class are optimized using validation F1.
- EfficientNet-B3 outperforms ViT baseline **without requiring augmentation**.
- Example results in `.ipynb`

## 📄 License

This project is released for research purposes only. Please cite appropriately if used in publications.
