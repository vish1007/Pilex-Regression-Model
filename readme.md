## Problem Description

In this project, we aim to solve the problem of pixel localization by developing a CNN-based model. Given a black image of size **50x50**, with a single white pixel (value 255), the model predicts the coordinates **(x, y)** of this white pixel. The task involves training the model to understand the spatial distribution and map the image to its corresponding pixel coordinates.

---

## 1. **Clone the Repository**

Clone the repository to your local machine to get started:

```bash
git clone https://github.com/vish1007/Pilex-Regression-Model.git
cd Pilex-Regression-Model
```

---

## 2. **Create and Activate the Conda Environment**

This project uses a Conda environment to ensure that all dependencies are installed correctly. Follow the steps below to set up the environment.

### Step 1: **Create the Environment**

Create the environment using the provided `environment.yml` file. Here is the content of the `environment.yml` file:

```yaml
name: pixel-regression-env
channels:
  - defaults
  - conda-forge
  - pytorch
dependencies:
  - python=3.8
  - numpy
  - matplotlib
  - scikit-learn
  - pytorch
  - torchvision
  - torchaudio
  - cudatoolkit=11.3
  - torchsummary

```bash
conda env create -f environment.yml
```

### Step 2: **Activate the Environment**

Activate the environment after it's created:

```bash
conda activate pixel-regression-env
```

---

## 3. **Install the Jupyter Kernel**

To use the environment as a kernel in Jupyter Notebook, you need to install `ipykernel`:

```bash
conda install ipykernel
```

Once installed, register the environment as a Jupyter kernel:

```bash
python -m ipykernel install --user --name pixel-regression-env --display-name "Python (pixel-regression-env)"
```

---

## 4. **Launch Jupyter Notebook**

Now that the environment and kernel are set up, launch Jupyter Notebook:

```bash
jupyter notebook
```

This will open the Jupyter Notebook interface in your default web browser.

---

## 5. **Select the Kernel in Jupyter Notebook**

1. Open the notebook **`pixel_regression_project.ipynb`** you want to work with, or create a new one.
2. In the top menu, click on the **Kernel** dropdown.
3. Select **Change kernel** from the dropdown menu.
4. Choose **Python (pixel-regression-env)** from the list of available kernels.


---

## 6. **Run the Notebook**

With the correct kernel selected, you can now run the cells in the notebook. To run a cell, press **Shift + Enter** or click the **Run** button in the toolbar.

---

## 7. **Model Overview**

### Architecture

The model is based on a **Convolutional Neural Network (CNN)** that is designed to predict the **(x, y)** coordinates of the white pixel. The network is trained using mean squared error (MSE) loss, as the problem involves predicting continuous values for the pixel's coordinates.

### Training

The model is trained on synthetic images where each image contains a single white pixel at a random location on a black background (50x50 image). The network learns to map the image to the pixel's **(x, y)** coordinates.

---

## 8. **Model Evaluation**

After training, the model's performance is evaluated on a test set of images. The predicted coordinates are compared with the ground truth using standard regression metrics (e.g., Mean Absolute Error, MSE).

---

## 9. **Deactivate the Environment (Optional)**

When you're done, deactivate the Conda environment using:

```bash
conda deactivate
```
