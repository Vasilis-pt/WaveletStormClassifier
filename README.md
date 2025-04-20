# CNN Classification of Geomagnetic Storms from Wavelet Spectrograms
# Geomagnetic Storm Classifier (Wavelet + CNN)

This project uses **wavelet spectrograms** of geomagnetic field data to classify days as either **storm** or **quiet** using a **Convolutional Neural Network (CNN)**.

---

## 🌍 Motivation

Geomagnetic storms are critical space weather events that can disrupt power grids, GPS, and satellites. This project explores the feasibility of identifying storm days directly from **spectrogram images** built using time-frequency analysis (e.g., wavelet transforms).

---

## 📁 Directory Structure


---

## ⚙️ How It Works

1. **Spectrogram Generation**: Time-series data is transformed into 2D images (spectrograms) using wavelet analysis (done offline).
2. **Storm vs Quiet Classification**:
   - SYM-H < -100 nT → **Storm**
   - SYM-H > -20 nT → **Quiet**
   - 12 images of each are selected for balance.
3. **CNN Architecture**:
   - 3 convolutional + pooling layers
   - 1 fully connected layer
   - Binary classification with sigmoid output
4. **Model Training**:
   - Uses Keras + TensorFlow backend
   - Early stopping to prevent overfitting

---

## 🧪 Run the Training

```bash
python train_model.py

**Notes**
The raw SYM-H index data file (KyotoSymhYear2015.dat) is not distributed with this repo. You can download it for free from the Kyoto World Data Center.

Spectrograms are generated externally using wavelet transforms on 1-minute resolution SYM-H data.

The .h5 model file is not uploaded due to GitHub’s file size limits.

 **Acknowledgments**
SYM-H data: World Data Center for Geomagnetism, Kyoto

Wavelet code inspired by Torrence & Compo (1998)

Model developed with Keras + TensorFlow

