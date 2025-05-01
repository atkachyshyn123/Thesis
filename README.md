# Coreset Selection using Neural Principal Component Analysis

## Problem Formulation

In this work, we introduce the Coreset Selection methodology based on Neural Principal Component Analysis. Since some datasets contain a considerable volume of data, the issue arises regarding computational resources. Our approach addresses this challenge by selecting the most representable subset from the larger one.

We aim to determine whether the Coreset Selection Method, which is based on Neural Principal Component Analysis, is efficient in intelligent image selection. We present a mathematical explanation of the methodology and the technical implementation, presented in the code in this repository. Additionally, we want to find our method's efficiency by comparing it with other Coreset Selection Methodologies, looking for its variations, and finding out their capabilities.

## Repository Contents

This repo contains two python notebook files:
1. **Thesis.ipynb** - Contains the described method code
2. **Comparative_Methods.ipynb** - Contains code for comparative methods

## Setup Instructions

### Prerequisites
- Python 3.6+
- PyTorch 1.7+
- CUDA-capable GPU (recommended)
- ImageNet dataset

### Running the Code

In order to run Thesis.ipynb, run all the cells, starting from the first one. You should also download the ImageNet dataset and ReseNet-50 weights and place the properly.

#### Adjusting ImageNet Path

Open `utils/datasets/paths.py` and adjust the `base_data_path` in line 6. The default value is `/scratch/datasets/`. Note that we assume that you have extracted ILSVRC2012 to `base_data_path/neural_pca` and `train` and `val` folders are located in `neura_pca` folder. 

If this does not match your folder layout, you can also directly manipulate `get_imagenet_path` in line 64. For example, if your dataset is located in `/home/user/datasets/ilsvrc2012/` you could change the function to:

```python
def get_imagenet_path():
   path = '/home/user/datasets/ilsvrc2012/'
   return path
```
#### Download Robust ResNet50 
Download the weights from [here](https://drive.google.com/file/d/169fhxn5X2_1-5vWTepkKJZRMdr8z4b9p/view) into utils and unzip the model.

