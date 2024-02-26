# pytorch_tutorial
A simple pytorch tutorial for developing DNN models for a regression, a classification and a computer vision task.

# Running the tutorial

## Option 1: Running on Google Colab
The jupyter notebook of this tutorial exists on google colab and can be used without additional installation requirements. However, users need an existing google account and it is required to create a copy of the notebook in the users personal google drive, since global editing is not permitted in the main notebook. The link to the notebook can be found here: [link](https://colab.research.google.com/drive/1jtWhXEnsBV7CYwE_x7gtV5AjOkX5kWFW?usp=sharing)

## Option 2: Running locally
**IMPORTANT NOTE:** We recommend to use `git clone --recursive` when cloning this repository! If you want to run locally, you **have** make sure that **also** the git submodule `pytorch-tutorial-lfs` is correctly cloned. The `--recursive` option takes care of this for you automatically. If this is not done correctly, important data files will be missing!

The code is also available from this repository in the `pytorch_tutorial.ipynb` file. We recommend to use an [anaconda](https://anaconda.org/) environment to run the tutorial. An environment that contains all the packages needed can be installed from a command shell like this:

```
conda create --name tutorial_env python pandas matplotlib numpy scikit-learn seaborn pytables ipykernel
conda activate tutorial_env
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
```

Note that in the last command, the `cudatoolkit` version needs to be adjusted to the supported CUDA version on the local machine.

We have also provided an `tutorial_env.yml` file with a working environment that can be used to install the required software using `anaconda` like this:

```
conda env create --name tutorial_env --file=tutorial_env.yml
```

Note that here we are using `cudatoolkit` version `11.3` again, which might be different for other machines.

# Datasets used

- For regression task: [WHO life expectancy dataset](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who) and [California Housing Prices dataset](https://www.kaggle.com/datasets/camnugent/california-housing-prices)

- For classification task: [Higgs dataset](https://archive.ics.uci.edu/ml/datasets/HIGGS) and the [Breast Cancer Wisconsin (Diagnostic) dataset](https://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+(diagnostic))

- For computer vision task: [MNIST dataset](http://yann.lecun.com/exdb/mnist/) and [CIFAR10 dataset](https://www.cs.toronto.edu/~kriz/cifar.html)