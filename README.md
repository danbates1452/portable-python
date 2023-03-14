# portable-python
Easy to setup python environment for my own use

## Installation
Requires Python 3.8.10 to already be installed on the device
1. Create a virtual environment with ```python3 -m venv venv```
2. Activate your virtual environment by running ```./venv/Scripts/activate``` (```./venv/bin/activate``` for Unix systems)
3. Run ```pip install -r requirements.txt``` to install dependencies

## Adding Packages
1. Use pip to install them
2. Run ```pip freeze > requirements.txt``` to save a full requirements list back
3. If intended to be a mainstay in this repo, git push back to master

## GPU Support
You may have to download CUDA: https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exe_local