# CNN Classification of Geomagnetic Storms from Wavelet Spectrograms

This project implements a Convolutional Neural Network (CNN) in Python using Keras to classify geomagnetic storm days from quiet days. The input to the model consists of daily wavelet spectrogram images derived from SYM-H index data.

The goal is to train a CNN to recognize patterns in spectrograms that correspond to geomagnetically active ("storm") days versus inactive ("quiet") ones.

The code includes:
- Data preparation and filtering based on SYM-H threshold
- Image classification using CNN
- Visualization of training performance
