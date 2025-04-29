# 🛣️ Pothole Detection using XAI (Explainable AI)

A full-fledged machine learning pipeline for pothole detection using deep learning and Explainable AI (XAI) — with support for automatic PDF reporting, model comparison, and explainability heatmaps.

---

## 📚 Table of Contents

- [📖 General Information](#-general-information)
- [🎯 Objective](#-objective)
- [📊 Dataset Information](#-dataset-information)
- [🔥 Project Pipeline](#-project-pipeline)
- [🧠 Explainable AI (XAI) Explained](#-explainable-ai-xai-explained)
- [🚀 Use Cases](#-use-cases)
- [📈 Conclusions](#-conclusions)
- [🙏 Acknowledgment](#-acknowledgment)
- [📬 Contact](#-contact)
- [🚀 How to Use This Repository](#-how-to-use-this-repository)

---

## 📖 General Information

This project enables automatic pothole detection in road images and justifies its decisions using Explainable AI (XAI). It supports field survey analysis using drone images, smart model training, visual explanation generation, and structured PDF report generation.

---

## 🎯 Objective

- Detect road potholes from drone/survey images.
- Justify predictions visually using XAI methods.
- Automate reporting with confidence scores and heatmaps.
- Compare model performances using charts.

---

## 📊 Dataset Information

- **Dataset**: [Kaggle - Pothole Detection Dataset](https://www.kaggle.com/datasets/atulyakumar98/pothole-detection-dataset?utm_source=chatgpt.com)
- **Classes**:
  - `Pothole`
  - `Normal`
-dataset/ ├── pothole/ ├── normal/


Images are resized to 224×224 or 512×512 depending on the model architecture.

---

## 🔥 Project Pipeline

1. Load and preprocess images
2. Train three models:
   - Simple CNN
   - Better CNN
   - ResNet18 (Transfer Learning)
3. Evaluate performance using accuracy, AUC
4. Apply XAI methods (GradCAM, IG, SmoothGrad)
5. Generate comparison visualizations
6. Export results to PDF

---

## 🧠 Explainable AI (XAI) Explained

We use Captum to apply:
- **GradCAM**: Class activation heatmaps
- **Integrated Gradients**: Input attribution
- **SmoothGrad**: Noise-reduced gradient visualizations

All explanations are generated per image and stored.

---

## 🚀 Use Cases

- Road maintenance planning
- Smart city infrastructure auditing
- Safety risk assessment in transportation
- Education and model interpretation demos

---

## 📈 Conclusions

| Model     | Accuracy | AUC Score |
|-----------|----------|-----------|
| Simple CNN | 91.24%  | 0.972     |
| Better CNN | 85.40%  | 0.956     |
| ResNet18   | 97.08%  | 0.995     |

- ResNet18 was the best performer.
- XAI helped validate visual focus areas of the model.

---
## 🙏 Acknowledgment

This project was made possible through the contributions of the open-source and ML research community. Special thanks to:

- **Atulya Kumar** for the [Pothole Detection Dataset](https://www.kaggle.com/datasets/atulyakumar98/pothole-detection-dataset) on Kaggle.
- **PyTorch** for providing a powerful deep learning framework.
- **Captum** for enabling model explainability via GradCAM, IG, and SmoothGrad.
- **FPDF** for streamlined PDF report generation.

I appreciate the global community’s ongoing efforts toward transparency, education, and open innovation.

---

## 📬 Contact

Created by **[@poronita](https://github.com/poronita)** — feel free to connect!

- 🔗 LinkedIn: [linkedin.com/in/prathvibhatti08](https://www.linkedin.com/in/prathvibhatti08/)

> Always open to collaborations, ideas, and opportunities!

---

## 🚀 How to Use This Repository

```bash
git clone https://github.com/your-username/pothole-detection-xai.git
cd pothole-detection-xai

pip install -r requirements.txt

# Train models
python train_models.py

# Generate predictions + XAI
python predict_and_explain.py

# Create downloadable report
python generate_report.py



