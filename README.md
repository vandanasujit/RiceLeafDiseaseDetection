# Image Classification with Data Augmentation
This project focuses on building an image classification model using deep learning techniques and data augmentation to enhance model performance and generalization. The dataset consists of 119 images related to rice leaf diseases. . The images are grouped into 3 classes based on the type of disease. 
Classes
●	Leaf smut-39 images
●	Brown spot-40 images
●	Bacterial leaf blight-40 images

 and the project explores the impact of various data augmentation techniques on model accuracy and overfitting.

 Domain: 
[Link Text](https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1001-RiceLeaf.zip)



### Project Overview
Given the limited size of the dataset, data augmentation is employed to artificially increase the training data size, helping the model generalize better to unseen images and avoid overfitting. The goal is to classify rice leaf diseases while maintaining high accuracy on both the training and testing datasets.

### Techniques Applied
### Data Augmentation
Several augmentation techniques were used to generate variations in the dataset:

#### *Rotation:
Initially tested with 10 degrees but increased to 20 degrees for better generalization.

#### *Shearing:
Random shearing along the X or Y axis. Increasing the shear value from 0.1 to 0.2 improved test accuracy.

#### *Zoom:
Random zooming in and out to simulate different distances.

#### *Horizontal Flip:
Random horizontal flips to reduce model bias toward orientation.

#### *Fill Mode:
The "nearest" fill mode was used to handle missing pixels after transformations.

### Image Preprocessing
#### *Normalization:
Pixel values were normalized to the range [0,1] for faster model convergence.

### Model Optimization
#### *Batch Size:
Experimented with batch sizes of 32 and 50. A batch size of 32 was optimal for this dataset.

#### *Epochs:
Trained the model for 30 epochs to allow convergence while avoiding overfitting.

#### *Early Stopping:
Early stopping was used to halt training when validation loss stopped improving, preventing the model from overfitting on the training data.

### Results
Two models were trained for comparison:

Model 1 (No Augmentation):

Training Accuracy: 100%
Test Accuracy: 79.1%
Model 2 (With Augmentation):

Training Accuracy: 98%
Test Accuracy: 87.5%
