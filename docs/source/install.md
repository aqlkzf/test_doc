# Installation

Follow these steps to install the MultiGATE package in a dedicated Conda environment. Please ensure you have Conda installed on your system before proceeding with these instructions.

```shell
conda create -n MultiGATEenv  python=3.7 -y 
conda activate MultiGATEenv
conda install tensorflow-gpu=1.15.0 cudatoolkit=10.0 cudnn=7.6.5 -y
conda install scikit-learn  pandas scanpy jupyterlab tqdm matplotlib conda-forge::networkx bioconda::pybedtools  conda-forge::louvain -y
pip install rpy2 --global-option=build_ext --global-option="-std=c99"
pip install MultiGATE
```


## Deatiled instructions

### Installation Guide for MultiGATE Package

Follow these steps to install the MultiGATE package in a dedicated Conda environment. Please ensure you have Conda installed on your system before proceeding with these instructions.

1. **Create a Conda Environment**
   Start by creating a new environment named `MultiGATEenv` with Python 3.7. This isolates the installation and avoids conflicts with existing packages.

   ```bash
   conda create -n MultiGATEenv python=3.7 -y
   ```

2. **Activate the Environment**
   Activate the newly created environment:

   ```bash
   conda activate MultiGATEenv
   ```

3. **Install TensorFlow and CUDA Toolkit**
   Install TensorFlow 1.15.0 along with the compatible CUDA toolkit and cuDNN library to enable GPU support. We strongly recommend you install the listed version of TensorFlow and CUDA toolkit and cudnn library.

   ```bash
   conda install tensorflow-gpu=1.15.0 cudatoolkit=10.0 cudnn=7.6.5 -y
   ```

4. **Install Additional Dependencies**
   Install the necessary Python packages including scikit-learn, pandas, scanpy for single-cell analysis, and other utilities.

   ```bash
   conda install scikit-learn pandas scanpy jupyterlab tqdm matplotlib -y
   conda install -c conda-forge networkx louvain -y
   conda install -c bioconda pybedtools -y
   ```

5. **Install RPy2**
   RPy2 is required for integrating R with Python. Note the use of global options to ensure compatibility with the C99 standard.

   ```bash
   pip install rpy2 --global-option=build_ext --global-option="-std=c99"
   ```

6. **Install MultiGATE**
   Finally, install the MultiGATE package using pip. 

   ```bash
   pip install MultiGATE
   ```

7. **Verify Installation**
   After installation, it's a good practice to verify that all components are installed correctly. You can do this by running a simple import test in Python.

   ```python
   # Activate your Conda environment if not already activated
   conda activate MultiGATEenv

   # Test the installation
   python -c "import MultiGATE; print('MultiGATE installed successfully')"
   ```

### Troubleshooting

If you encounter any errors during the installation, consider the following tips:

- Ensure that your Conda environment is properly activated before installing any packages.
- Check that the CUDA toolkit and cuDNN library versions are compatible with TensorFlow 1.15.0.
- If pip installation fails, verify your internet connection and ensure that your Python environment is correctly configured to install packages.

By following these detailed steps, you can set up the MultiGATE package and prepare for running your analyses. This setup provides a robust environment for computational studies in genomics and bioinformatics.