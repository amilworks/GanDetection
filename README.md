# **GAN Generated Image Detection using Convolutional Neural Networks**
### Author:  Amil Khan | Version 1.0
[![DOI](https://zenodo.org/badge/181292740.svg)](https://zenodo.org/badge/latestdoi/181292740)



***

### Abstract

Synthetic image generation using _Generative Adversarial Network (GAN)_  architectures have become increasingly harder to fail the eye test. With a relatively low-cost GPU and enough time, we have seen images of fake celebrities, bedrooms, and landscapes---to name a few---deceive a reasonable person. Previous use cases of GANs, such as increasing the number of samples in a small dataset, have seen widespread adoption across disciplines. However, over the past year, we have also seen GANs being used for malicious cases as well. Hence, we will feed  GAN generated images we produced to a model whose task is to determine whether an image is "Real" or "Fake''. We demonstrate GAN generated image detection using five ImageNet classification models for the classification task: classification of real images and fake images presented as inputs to the ImageNet model.

### Data Generation

For the data generation portion, we decided to use the Progressive GANs implementation since it produced the best results at the time of this writing. More specifically, however, the Progressive GANs approach of starting with low-resolution images, and then progressively increasing the resolution by adding layers to the networks, allowed greater stability during training, shorter training times, and higher resolution images.

I opted to put everything you need for the data generation portion inside the `data` folder.


### Model Performance

The best model that was able to balance computational time, complexity, and accuracy. With 96% accuracy on the test set at epoch 11, we were able to obtain extremely low error rates and a generalizable model. 

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.testrun.org


--------
