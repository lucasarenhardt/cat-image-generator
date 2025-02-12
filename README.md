# Cat Faces Image Generation with GANs

This project uses Generative Adversarial Networks (GANs) to generate images of cat faces. Built with TensorFlow and Keras, this model leverages deep convolutional architectures in both the generator and discriminator networks. The project includes evaluation of image quality using the Frechet Inception Distance (FID), a common metric for assessing GAN performance.

## Features

- Utilizes Convolutional Neural Networks (CNNs) for cat image generation.
- Loads and processes a dataset of cat faces for training.
- Employs a GAN architecture, where:
    - The generator learns to create realistic cat face images.
    - The discriminator evaluate the authencity of generated cat images.
- Trains the model using a GPU (if available).

## Dataset
The project uses a collection of cat face images, which are preprocessed and normalized to fit the model's requirements.

- **Source**: [Animal Faces HQ Dataset (AFHQ)](https://github.com/clovaai/stargan-v2/tree/master), using only the cat subset.
- Images are resized to 128x128 pixels and normalized to a range between 0 and 1 for efficient training.

## Model Architecture

The GAN model is built using TensorFlow and Keras libraries, with distinct architectures for the generator and discriminator:

- Generator Architecture: The generator network uses layers such as convolutional transpose layers, batch normalization, and LeakyReLU activations to create synthetic images from random noise vectors.
- Discriminator Architecture: The discriminator network consists of convolutional layers with dropout and LeakyReLU activations, designed to classify images as real or fake.

The adversarial training approach helps the generator and discriminator improve simultaneously, refining the quality of generated images over successive training epochs.

## Frechet Inception Distance (FID)

The Frechet Inception Distance (FID) is a widely recognized metric for evaluating the quality of images generated by Generative Adversarial Networks (GANs). FID measures the similarity between real and generated images by comparing their feature distributions in a deep feature space, typically leveraging a pre-trained Inception-v3 model. A lower FID value signifies better quality in the generated images, indicating that they are more similar to real images in terms of their visual characteristics.

In this project, the FID value obtained by the model is 39, reflecting a reasonably good quality of the generated cat faces. This score suggests that the model effectively captures the essential features of real cat images, although there is still room for improvement in generating even more realistic and diverse outputs.

## Examples

Here are some examples of images generated by the GAN model. These images showcase the model's ability to create diverse cat faces:

![image](https://github.com/user-attachments/assets/2e60eef8-af58-41ad-81d4-8029df2fd063)
