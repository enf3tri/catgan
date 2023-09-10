# CatGAN: Cat Image Generator
![logo](https://github.com/enf3tri/catgan/blob/main/lib/cat-gan-icon-n.png)

## Overview

CatGAN is a Generative Adversarial Network (GAN) designed to generate realistic images of cats. This project uses deep learning techniques to create high-quality cat images from random noise. Whether you're a cat lover or a machine learning enthusiast, you can use CatGAN to generate adorable cat pictures!

## Features

- Generates images from random noise.
- Customizable architecture and training parameters for fine-tuning.
- Pre-trained models for quick image generation.

## Architecture
![logo](https://github.com/enf3tri/catgan/blob/main/lib/arch.png)

### Generator
```python
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 dense_3 (Dense)             (None, 8192)              827392    
                                                                 
 leaky_re_lu_6 (LeakyReLU)   (None, 8192)              0         
                                                                 
 reshape (Reshape)           (None, 4, 4, 512)         0         
                                                                 
 conv2d_transpose (Conv2DTr  (None, 8, 8, 512)         4194816   
 anspose)                                                        
                                                                 
 batch_normalization_4 (Bat  (None, 8, 8, 512)         2048      
 chNormalization)                                                
                                                                 
 leaky_re_lu_7 (LeakyReLU)   (None, 8, 8, 512)         0         
                                                                 
 conv2d_transpose_1 (Conv2D  (None, 16, 16, 256)       2097408   
 Transpose)                                                      
                                                                 
 batch_normalization_5 (Bat  (None, 16, 16, 256)       1024      
 chNormalization)                                                
                                                                 
 leaky_re_lu_8 (LeakyReLU)   (None, 16, 16, 256)       0         
...
Total params: 9050052 (34.52 MB)
Trainable params: 7780163 (29.68 MB)
Non-trainable params: 1269889 (4.84 MB)
```

### Discriminator
```python

_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d (Conv2D)             (None, 64, 64, 128)       3584      
                                                                 
 leaky_re_lu (LeakyReLU)     (None, 64, 64, 128)       0         
                                                                 
 batch_normalization (Batch  (None, 64, 64, 128)       512       
 Normalization)                                                  
                                                                 
 conv2d_1 (Conv2D)           (None, 64, 64, 128)       147584    
                                                                 
 leaky_re_lu_1 (LeakyReLU)   (None, 64, 64, 128)       0         
                                                                 
 batch_normalization_1 (Bat  (None, 64, 64, 128)       512       
 chNormalization)                                                
                                                                 
 max_pooling2d (MaxPooling2  (None, 21, 21, 128)       0         
 D)                                                              
                                                                 
 dropout (Dropout)           (None, 21, 21, 128)       0         
                                                                 
 conv2d_2 (Conv2D)           (None, 21, 21, 128)       147584    
                                                                 
...
Total params: 1267969 (4.84 MB)
Trainable params: 1266945 (4.83 MB)
Non-trainable params: 1024 (4.00 KB)
```


## Getting Started

### Prerequisites

- Python 3.6+
- TensorFlow 2.x
- Keras
- NumPy
- Matplotlib (for visualization)

### Result
![logo](https://github.com/enf3tri/catgan/blob/main/lib/GANCAT_14500.png)
