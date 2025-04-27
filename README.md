# Data Augmentation with TensorFlow Keras

This Colab notebook demonstrates how to apply data augmentation to images using TensorFlow Keras' `ImageDataGenerator`. 

By randomly transforming input images during training, you can improve model generalization and robustness.

---

## Table of Contents
1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Notebook Structure](#notebook-structure)
4. [Usage](#usage)
5. [Customization](#customization)
6. [References](#references)

---

## Overview
Data augmentation generates new training samples by applying random transformations (rotation, shift, shear, zoom, flip) to existing images. 

This technique helps prevent overfitting and allows models to learn more robust feature representations.

In this notebook, you will:
- Suppress TensorFlow warning messages for cleaner output
- Load a sample image into a batch tensor
- Configure an `ImageDataGenerator` with common augmentation parameters
- Generate and display a grid of augmented images

---

## Prerequisites
- Python 3.7+
- TensorFlow 2.x
- Matplotlib
- NumPy

To install missing packages in Colab, run:
```bash
!pip install tensorflow matplotlib numpy
```

---

## Notebook Structure

1. **Suppressing TensorFlow Warning Messages**: Sets the environment variable to hide TensorFlow C++ backend logs.
2. **Loading a Sample Image**: Reads a JPEG file and converts it into a 4D tensor `(batch_size, height, width, channels)`.
3. **Configuring the Data Augmentation Generator**: Defines random transformation parameters.
4. **Generating and Displaying Augmented Images**: Uses the generator to produce and plot six augmented variants of the sample image.

---

## Usage
1. Open this notebook in Google Colab.
2. Ensure the `sample_images/dog.jpg` file is available in the working directory (or update the path).
3. Run all cells sequentially.
4. Observe the augmented outputs and adjust parameters as needed.

---

## Customization
- Change `rotation_range`, `width_shift_range`, etc., in the `ImageDataGenerator` to experiment with different augmentation intensities.
- Replace the sample image with your own dataset.
- Integrate the generator into a model training loop via `model.fit(datagen.flow(...))`.

---

## References
- [Keras ImageDataGenerator Documentation](https://www.tensorflow.org/api_docs/python/tf/keras/preprocessing/image/ImageDataGenerator)
- [Colab Quickstart Guide](https://colab.research.google.com/notebooks/intro.ipynb)

