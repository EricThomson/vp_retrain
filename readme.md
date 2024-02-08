# retrain volpy maskrcnn in torch
WIP.

## Set up virtual env
Virtual env setup I followed (note I have mamba in my base env):

    conda create -n torch_play python=3.10

To install pytorch locally: https://pytorch.org/get-started/locally/
Then check with `nvidia-smi` what version of cuda you are running. I have cuda 12.0 it works to install with cuda 12.1 using:

    mamba install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia

Test whether it sees your gpu, go into python and:

    import torch
    torch.cuda.is_available()

Install additional libraries (pycocotools not currently being used but might be):

    mamba install -c conda-forge opencv matplotlib scikit-image pycocotools jupyterlab

install torchinfo (gives summary of models -- not really essential but can be useful):

    pip install torchinfo

## Run notebook
All the important things should be in `volpy_training_initial.ipynb`, including which source materials it is adapted from, what needs to be improved, what might be improved, etc. 


