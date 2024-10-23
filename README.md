# Cat Faces Image Generation with GANs

This project implements a deep learning model using Generative Adversarial Networks (GANs) for generating realistic images of cat faces. The model is built with TensorFlow and Keras, utilizing a convolutional architecture for both the generator and discriminator networks.

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
