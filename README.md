In this work, we introduce the Coreset Selection methodology based on Neural Principal Component Analysis. Since some datasets contain a considerable volume of data, the issue arises regarding computational resources. Our approach addresses this challenge by selecting the most representable subset from the larger one.

We aim to determine whether the Coreset Selection Method, which is based on Neural Principal Component Analysis, is efficient in intelligent image selection. We present a mathematical explanation of the methodology and the technical implementation, presented in the code in the link below. Additionally, we want to find our method's efficiency by comparing it with other Coreset Selection Methodologies, looking for its variations, and finding out their capabilities.


This repo contains two python notebook files. The Thesis.ipynb contains the descripted method code. The other one contains code for colmparative methods.

In order to run Thesis.ipynb, run all the cells, starting from the first one. You should also download ImageNet dataset and locate train and val in 

Adjust imagenet_path
Open utils/datasets/paths.py and adjust the base_data_path in line 6, the default value is /scratch/datasets/. Note that we assume that you have extracted ILSVRC2012 to base_data_path/imagenet. If this does not match your folder layout, you can also directly manipulate get_imagenet_path in line 64. For example if your dataset is located in /home/user/datasets/ilsvrc2012/ you could change the function to:

def get_imagenet_path():  
    path = `/home/user/datasets/ilsvrc2012/` 
    return path

Download Robust ResNet50
Download the weights from here into utils and unzip the model.
