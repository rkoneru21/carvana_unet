# 🚗 Carvana UNet Semantic Segmentation

This project uses a **UNet architecture** to perform semantic segmentation on the [Carvana Image Masking Challenge](https://www.kaggle.com/competitions/carvana-image-masking-challenge) dataset. The goal is to accurately segment cars in images using deep learning with PyTorch.

> Built and trained entirely in **Google Colab**, with support for training on GPU and storing the best model in Google Drive.

---

## 📌 Features

- UNet implementation in PyTorch
- Image augmentations using **Albumentations**
- Mixed precision training using **AMP**
- Live training logs via **tqdm**
- Validation with Dice Score and Pixel Accuracy
- Corrupted image handling for robust training
- Model saving/loading to/from Google Drive
- Save predictions as images

---

## 🧠 Model Architecture

We use the **UNet** architecture, which is popular for semantic segmentation tasks. It has an encoder-decoder structure with skip connections that help preserve spatial information.

---

## 🧪 Dataset

- Dataset used: Carvana Car Segmentation dataset from Kaggle
- Images of cars with corresponding masks

---

## 🚀 How to Run (in Google Colab)

1. Open the Carvana_UNet.ipynb file in a Python Notebook
2. Make sure the dataset is in the correct path (e.g., `/content/drive/MyDrive/Kaggle/carvana/...`), or update the path variables in the notebook
3. Run the entire notebook.
4. The best model will be saved to your Drive, and predictions will be stored as images.

---

## 📊 Results

Evaluation is done using:
- Dice Score
- Pixel Accuracy

**Training Results after 5 Epochs**:
- ✅Best Accuracy: **98.31%**
- ✅Best Dice Score: **0.962**

---

## 🖼️ Sample Predictions

Below are examples of ground truth masks compared to the predicted masks:

| Ground Truth Mask | Predicted Mask |
|-------------------|----------------|
| ![Ground Truth](truth_11.png) | ![Prediction](pred_11.png) |
| ![Ground Truth](truth_8.png) | ![Prediction](pred_8.png) |

> 🧠 The predicted masks align closely with the ground truth after only 5 epochs, demonstrating strong performance of the U-Net model.


