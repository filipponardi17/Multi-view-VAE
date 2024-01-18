# Multi-View Variational Autoencoder (MVAE) Project

This project was originally the first lab for the Machine Learning in Healtcare course at UC3M 
This GitHub repository showcases the implementation of a Multi-View Variational Autoencoder (MVAE) using PyTorch. The goal of the project is to generate latent representations of images from both the MNIST and SVHN datasets simultaneously.

## Model Architecture

The MVAE consists of two encoders and two decoders corresponding to each view (MNIST and SVHN). The encoders map input images to a shared latent space, and the decoders reconstruct the images from this shared latent space.

- **Encoder:** Utilizes convolutional layers to extract features from input images and projects them into the shared latent space.
- **Decoder:** Reconstructs images from the shared latent space using transposed convolutional layers.

## Training

The model is trained using a custom training loop over a specified number of epochs. The loss function includes a reconstruction term and a KL divergence term, ensuring that the generated latent space accurately represents the input images.

The training loop logs various metrics, such as total loss, reconstruction losses for each view, and KL divergence. Checkpoints are saved during training for easy restoration and further experimentation.

## Data Preparation

The project employs the MNIST and SVHN datasets, with a custom DataLoader to handle multi-modal training. Transformed indices are used to match samples from both datasets for effective training.

## Usage

The project provides utility functions to train the MVAE, generate samples from the learned latent space, and visualize reconstruction results. 

## Co-authour 
Riccardo Conforti Gallo
Jorge Parreno
