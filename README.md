
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

![App Screenshot](https://www.researchgate.net/profile/Azam-Hamidinekoo/publication/343839103/figure/fig4/AS:934374526685186@1599783655783/Some-examples-of-T2W-ADC-and-DWI-MR-images-from-our-dataset-which-demonstrates-that-DWI.ppm)


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
