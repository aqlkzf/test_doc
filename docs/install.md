```shell
conda create -n MultiGATEinstall  python=3.7 -y 
conda install tensorflow-gpu=1.15.0 cudatoolkit=10.0 cudnn=7.6.5 -y
conda install scikit-learn  pandas scanpy jupyterlab tqdm matplotlib conda-forge::networkx bioconda::pybedtools  -y
pip install MultiGATE

