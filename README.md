# Image Clustering with VGG16 and K-Means

This project demonstrates how to extract high-level feature representations from images using a pre-trained VGG16 Convolutional Neural Network (CNN), and then apply K-Means clustering to group the images based on those features.

## Overview

The workflow includes:
- Loading and preprocessing images to 224x224 pixels
- Using VGG16 (without top layers) to extract deep feature vectors
- Applying K-Means to cluster the images based on their features
- Organizing the images into folders according to their assigned cluster

This approach allows for an unsupervised grouping of images that share similar visual characteristics.

## Usage

### Local
1. Clone the repository and upload your own images into a directory.
2. Modify the `input_folder` path in the notebook to match your image directory.
3. Set the desired number of clusters with the `n_clusters` variable.
4. Run the notebook to generate clustered outputs.

### Google Colaboratory
1. Go to https://colab.research.google.com/drive/1j41Ws0FHBEGST5QK2JwxfWxB80crT8lj?usp=sharing
2. Create a copy into your Google Drive
3. Additional instructions are in the notebook
   
## Requirements
- Python 3.x
- TensorFlow
- scikit-learn
- NumPy
- Matplotlib
- Google Colab (if using Drive paths)

## License

This project is licensed under the MIT License. You are free to use, modify, and distribute this code for personal or commercial purposes.

