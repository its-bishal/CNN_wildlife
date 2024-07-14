# Wildlife Surveillance and Preservation System

## Overview

This project is a research-based initiative focused on experimenting with various neural network architectures for classification, segmentation, and detection. The primary goal is to create a system that aids in the preservation of wildlife while controlling encounters between wildlife and humans. This system is designed to surveil buffer zones and detect if any wildlife leaves their settlement areas, potentially entering human-conflict zones, which could endanger their lives.

## Dataset

The dataset used for this project consists of images of four prominent animals from Chitwan National Park, Nepal:
- Wildlife
- Elephant
- Rhino
- Zebra

## Objectives

1. **Classification**: Classify the images into one of the four classes.
2. **Segmentation**: Segment the images to identify different parts or features.
3. **Detection**: Detect the presence of the animals within the images.

## Models and Methods

### 1. Classification

#### Sequential CNN Model
- **Architecture**:
  - 4 Conv2D layers
  - 2 MaxPool2D layers
  - 1 Flatten layer
  - 2 Dense layers
- **Activation Functions**: ReLU for hidden layers, Softmax for the output layer
- **Loss Function**: Sparse Categorical Crossentropy

#### Transfer Learning Model
- **Base Model**: VGG16
- **Additional Layers**: Similar to the Sequential CNN Model

### 2. Segmentation

#### K-means Clustering
- **Number of Clusters**: 5
- **Output**: Segmented images saved to a specified location

### 3. Detection

#### Sliding Window Architecture
- **Method**:
  - Creation of a sliding window that hovers over the pixels of the images
  - Creation of image pyramids
  - Utilization of these methods for detection functionality

#### YOLOv3 Model
- **Architecture**:
  - 53-layered architecture
  - Batch Normalization Layer
  - Leaky ReLU Activation Function

## How to Use

1. Clone the repository: 
   ```sh
   git clone https://github.com/its-bishal/CNN_wildlife.git
   ```
2. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the training scripts for the desired model (classification, segmentation, detection).

## Conclusion

This project aims to contribute to wildlife preservation efforts by providing a robust system for monitoring and detecting wildlife in buffer zones, thereby reducing human-wildlife conflicts. The implemented models and techniques offer a comprehensive approach to address the challenges in wildlife surveillance and protection.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

We would like to acknowledge the efforts of Chitwan National Park, Nepal, for providing the dataset and the inspiration for this project.
