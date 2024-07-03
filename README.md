# README: Day to Night Image Translation using CycleGAN

## Introduction

This repository contains the implementation of a CycleGAN model for translating images between day and night domains without requiring paired datasets. The primary objective is to generate realistic nighttime scenes from daytime images and vice versa.

## Dataset

We used a dataset consisting of day and night images, split into training and testing sets:

- **Training Day Images**: 417
- **Testing Day Images**: 105
- **Training Night Images**: 181
- **Testing Night Images**: 46

## Model Architecture

### Generator

- Utilizes ResNet with 19 residual blocks.
- Converts day images to night images and vice versa.

### Discriminator

- Uses PatchGAN architecture.
- Classifies image patches as real or fake.

## Training

- **Epochs**: 200
- **Learning Rate**: 0.0002 with decay starting at epoch 100
- **Batch Size**: 4
- **Loss Functions**: Adversarial, cycle consistency, and identity losses
- **Optimizers**: Adam with gradient clipping
- **Replay Buffer**: Stores up to 50 previously generated images

## Results and Visualization

The results include generated images that convincingly capture the characteristics of both day and night scenes. Training loss curves indicate stable and effective learning.
![image](https://github.com/bahetiaditi/cyclegan/assets/73452048/39e50159-3867-40d2-ae31-2047ae256053)


## Notebook

The uploaded notebook contains the full code for the project.

## Final Notebook

To view the final notebook after 200 epochs, visit this [link](https://www.kaggle.com/aditibaheti/cyclegan-daynight).

## Blog

For a detailed explanation and analysis of this project, read our blog post [here](https://dev.to/aditi_baheti_f4a40487a091/from-day-to-night-building-a-cyclegan-for-image-translation-3pjd).

## Conclusion

This project demonstrates the effectiveness of CycleGANs in translating images between day and night domains, showcasing the versatility and power of GAN-based image translation.
