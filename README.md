
# Prostate Image Segmentation using AI on Image Data

Prostate cancer disease is one of the common types that cause men's prostate damage all over the world. The patient undergoes  Magnetic resonance imaging (MRI) before any medications are prescribed to the patient and in the process the images so scanned are wider spread out, and it becomes very important to segment only the prostate regions which plays a crucial role in many diagnostic medical applications. Automatic segmentation of prostate and prostate zones from MR images makes many diagnostic and therapeutic applications easier and efficient.


## Toolkit

numpy==1.16.6

scipy==1.2.1

tensorflow-gpu==1.12.0

tensorboard==1.12.2

SimpleITK==1.2.0
## Dataset

The Train and Test datasets were created using different the combinations of images, including T2-Weighted (T2W) images, Diffusion-Weighted Images (DWI) and Apparent Diffusion Coefficient (ADC) images. To merge and aligne the DWI, ADC and T2W images.

Dataset can be accessed using the below link
https://drive.google.com/file/d/1ow7Ikh7LRSo5C0VEF6qyhRSvZECN6j_1/view
## Overview

The MRI, once scanned are passed onto the ADC and DWI to check for diffusion, the higher the diffusion more probability that its a prostate region suitable to detect the cancer

![PS2](https://user-images.githubusercontent.com/65388338/183240248-ef016054-1363-4db7-a6f4-5d491cc77009.png)


## Methods

1. Combining the t2W, DWI, ADC images 
2. Normalization of the images was performed
3. The images were rotated by 90◦
4. Generator loss - A sigmoid cross entropy loss of the generated images were tabulated using the Mean absolute error
5. Discriminator loss - The discriminator loss function takes 2 inputs; real images, generated images. Then the total_loss considered is the sum of real_loss and the generated_loss 
6. The images were trained using TensorFlow using jupyter notebook.
    * Optimizer - Adam
    * Epochs    - 100 (could be increased for better learning)
    * Batch size - 1


## Sample Output

#### The Actual Input Image
![ps5](https://user-images.githubusercontent.com/65388338/183256349-38be7768-4ca8-49e7-a7b9-a79df53b4312.png)

#### Trained
![ps3](https://user-images.githubusercontent.com/65388338/183256365-c457f42c-134a-48be-8575-70ad2df63889.png)

#### Predicted
![ps4](https://user-images.githubusercontent.com/65388338/183256380-ff090d08-ff42-4e4b-a02c-c57ce52758aa.png)


## Future Improvisations

1.  The accuracy of the predicted images could be improved
2.  Training the images with more data could be the next ideal move
3.  Increasing the Epochs while training will definetly deliver much accurate results.
