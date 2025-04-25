Apologies for the confusion! Here's a **`README.md`** file tailored to your setup for creating a Conda environment, installing the kernel, and running it on Jupyter notebook. You can copy and save it directly into your project folder as `README.md`.

---

```markdown
# Pixel Regression Environment Setup

This repository provides all necessary files to run the **Pixel Regression** model for segmentation tasks. Follow the steps below to set up your environment and run the Jupyter Notebook.

## 1. **Clone the Repository (Optional)**

If you haven't already, clone the repository to your local machine using the following command:

```bash
git clone https://github.com/your-repository-name.git
cd your-repository-name
```

## 2. **Create and Activate the Conda Environment**

This repository uses a Conda environment to ensure that all dependencies are installed correctly.

### Step 1: **Create the Environment**

To create the environment with all required dependencies, use the provided `environment.yml` file:

```bash
conda env create -f environment.yml
```

This will set up the environment with all the required libraries specified in the YAML file.

### Step 2: **Activate the Environment**

Once the environment is created, activate it with the following command:

```bash
conda activate pixel-regression-env
```

Make sure to replace `pixel-regression-env` with the correct environment name if it's different.

## 3. **Install the Jupyter Kernel for the Environment**

To use this environment as a kernel in Jupyter Notebook, you need to install `ipykernel`:

```bash
conda install ipykernel
```

### Step 1: **Add the Environment to Jupyter Notebook as a Kernel**

Once `ipykernel` is installed, run the following command to add the environment as a kernel to Jupyter:

```bash
python -m ipykernel install --user --name pixel-regression-env --display-name "Python (pixel-regression-env)"
```

- `--name` is the name of the environment.
- `--display-name` is the name that will be shown in the Jupyter interface.

## 4. **Launch Jupyter Notebook**

Now that the environment is ready and the kernel is installed, launch Jupyter Notebook:

```bash
jupyter notebook
```

This will open the Jupyter Notebook interface in your default web browser.

## 5. **Select the Kernel in Jupyter Notebook**

Once Jupyter Notebook is open, follow these steps to select the correct kernel:

1. Open your desired notebook or create a new one.
2. In the top-right corner, click on the **Kernel** menu.
3. From the dropdown, select **Change kernel**.
4. Choose **Python (pixel-regression-env)** from the list of available kernels.

## 6. **Run the Notebook**

With the correct kernel selected, you can now execute the cells in your notebook. To run a cell, simply press **Shift + Enter** or click the **Run** button in the toolbar.

## 7. **Deactivate the Environment (Optional)**

When you are done, deactivate the environment with the following command:

```bash
conda deactivate
```
