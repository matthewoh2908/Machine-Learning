# Cats vs Dogs Image Classifier

This project builds a **neural network model** to classify images as either **cats or dogs** using a simple deep learning approach.

Based on my coursework: :contentReference[oaicite:0]{index=0}  

---

## Project Overview

The goal of this project is to see how well a **fully connected neural network (Dense layers only)** can perform image classification.

- Input: Images of cats and dogs  
- Output: Prediction → Cat (0) or Dog (1)  
- Dataset: ~25,000 images (balanced dataset)

Instead of using advanced models like CNNs, this project focuses on **basic neural networks** to understand how they work.

---

## What I Did

### 1. Data Preprocessing
- Converted images to **grayscale**
- Resized images to **32 × 32**
- Removed corrupted images
- Flattened images into **1D vectors (1024 features)**
- Shuffled data to avoid bias  

---

### 2. Models Built

I tested different models to compare performance:

- **Random Guessing (Baseline)** → ~49.94% accuracy  
- **Single Layer Perceptron (SLP)** → ~57% (underfitting)  
- **Multi-Layer Perceptron (MLP)** → ~64% (overfitting)  
- **Regularised MLP (Final Model)** → ~65% (best balance)  

---

### 3. Improving the Model

To improve performance, I:
- Added **more layers (deeper model)**
- Used **L2 Regularisation** (to reduce large weights)
- Used **Dropout** (to prevent over-reliance on neurons)
- Tuned hyperparameters using **RandomSearch**

---

## Final Results

Final model performance:
- **Accuracy:** ~65%  
- **Precision:** ~63%  
- **Recall:** ~71%  
- **AUC:** ~0.71  

The model performs much better than random guessing and generalises well.

---

## Key Findings

- Simple models (SLP) are **too weak** → underfitting  
- Bigger models can **overfit easily**  
- Best results come from:
  - ✔️ Multiple layers  
  - ✔️ Proper regularisation  
- Increasing neurons alone **does NOT guarantee better performance**  

---

## Limitations

- No CNN used (due to coursework restriction)
- Flattening images loses spatial information
- Model accuracy is limited compared to modern approaches

---

## Future Improvements

- Use **CNNs** for better image feature extraction  
- Apply **data augmentation** (flip, rotate, zoom)  
- Add **early stopping** to prevent overfitting  
- Try deeper architectures  

---

## Key Learning

This project helped me understand:
- How neural networks learn from image data  
- The importance of **model architecture + regularisation**  
- Why **overfitting vs underfitting** matters  
