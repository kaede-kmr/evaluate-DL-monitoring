# Evaluation of deep learning-based monitoring of frog reproductive phenology

This repository contains the code implementation used for training a deep learning classifier as described in the paper accepted for Ichthyology & Herpetology by Kimura and Sota (DOI will be included after publication). We trained a convolutional newral network (CNN) capable of identifying five frog species based on their call recorded in Kyoto City, Japan.

The code was uploaded to share an example of simple training procedure using Python and the [fastai](https://www.fast.ai/) library. Audio datasets required for training and inference are not included, which are available from the corresponding author (K.K.) upon request.

The training procedure is chiefly based on [fastai tutorials on multi-label image classification](https://docs.fast.ai/tutorial.vision.html#multi-label-classification---using-the-high-level-api).  If you are interested in creating your own species classification model, I recommend referring to the fastai tutorials as well as [Chage (2020)](https://doi.org/10.22541/au.158316446.65534248).



## Environments

Install requirements: fastai 2.7.10, scikit-learn 1.2.0

We used a Windows computer with NVIDIA GeForce RTX 3060.

## Description

1. **model-training.ipynb** | Train the ResNet18 model to classify spectrograms into six classes. These classes include five frog species and background noise. Since more than one frog species can be present in a single spectrogram, multi-label classification has been implemented.
2. **model-evaluation.ipynb** | Write out the classification results of the test dataset and various model performance metrics.
3. **inference-with-trained-model.ipynb** | Apply the trained model (stored in `output/20230102_trained-model.pkl`) to detect frog species in the spectrograms generated from field recordings.
