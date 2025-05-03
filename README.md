# Image Clustering with VGG16 and K-Means

An efficient tool that uses the VGG16 CNN and the K-means algorithm to automatically organize and group similar images. This project leverages feature extraction through deep learning and unsupervised learning to create meaningful clusters of images without the need for labeled data.

## Overview

This project provides an optimized approach to automatically organizing image collections by:

1. Using a pre-trained VGG16 convolutional neural network to extract meaningful features from images  
2. Applying the K-means algorithm to group similar images based on these extracted features  
3. Organizing the grouped images into separate folders for easy review

Ideal for photographers, digital asset managers, content creators, or any project that requires intelligent image organization.

## Features

- **Deep Feature Extraction**: Leverages the VGG16 CNN pre-trained on ImageNet to extract high-level features from images  
- **Unsupervised Learning**: Groups similar images without needing labeled data  
- **Customizable Clusters**: Adjust the number of groups based on your specific needs  
- **Organized Output**: Automatically saves the grouped images in separate directories  
- **Supports Multiple Image Formats**: Works with JPG, JPEG, and PNG files  

## Requirements

- Python 3.7+  
- TensorFlow/Keras  
- scikit-learn  
- NumPy  
- PIL (Python Imaging Library)  
- Google Colab (for notebook implementation)  

## Installation

### Option 1: Run on Google Colab  
The easiest way to use this project is through Google Colab:

1. Upload the notebook `Image_Clustering_VGG16_K_Means.ipynb` to Google Colab or go to https://colab.research.google.com/drive/1j41Ws0FHBEGST5QK2JwxfWxB80crT8lj?usp=sharing
2. Mount your Google Drive (the notebook includes code for this)  
3. Upload your images to a folder in your Google Drive  
4. Update the input folder path in the notebook to point to your images  

### Option 2: Local Installation  
To run locally:

```bash
# Clone the repository
git clone https://github.com/tuusuario/image-clustering-vgg16-kmeans.git
cd image-clustering-vgg16-kmeans

# Install required packages
pip install tensorflow scikit-learn numpy pillow matplotlib
```
## Usage

1. **Prepare your images**  
   - Place all the images you want to cluster in a single directory

2. **Set paths and parameters**  
   - Update the `input_folder` path to your image directory  
   - Set `output_folder` to your desired destination  
   - Adjust `n_clusters` to the number of groups you want to create

3. **Run the code**  
   - In Google Colab, run all the notebook cells in order  
   - Locally, run the equivalent Python script

4. **Review the results**  
   - The clustered images will be organized into numbered directories within your output folder  
   - You can download the ZIP file containing all the cluster folders

## How It Works

1. **Feature Extraction**: The pretrained VGG16 model (without the classification layer) processes each image to extract a 512-dimensional feature vector representing high-level image features.

2. **Dimensionality Reduction**: These feature vectors capture the essence of each image in a much more meaningful way than raw pixel values.

3. **K-means Clustering**: The extracted features are grouped using the K-means algorithm, which finds natural clusters in the data.

4. **Output Organization**: The images are copied into cluster-specific folders based on their assigned cluster.

## Customization

- **Change the Feature Extractor**: You can replace VGG16 with other models such as ResNet50, InceptionV3, or EfficientNet  
- **Clustering Algorithm**: K-means can be replaced by other clustering algorithms like DBSCAN or hierarchical clustering  
- **Preprocessing**: Add custom preprocessing steps tailored to your specific image collection

## Performance Notes

- Processing time depends on the number and size of the images  
- For large image collections, consider processing in batches  
- The notebook is optimized to run on Google Colab GPU for faster processing

## Limitations

- K-means requires you to specify the number of clusters in advance  
- Very large image collections may require additional optimization  
- Clustering quality depends on the diversity and features of your image collection

## License

This project is licensed under the MIT License – see the LICENSE file for more details.

## Acknowledgments

- [VGG16](https://keras.io/api/applications/vgg/) pretrained model from Keras Applications  
- Inspired by various image clustering techniques in computer vision

## Author

Mateo Vergara

---

If you find this project useful, consider starring the repository on GitHub.
