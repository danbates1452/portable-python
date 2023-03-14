# portable-python
Easy to setup python environment for my own use on the University of Sussex Engineering and Informatics School computers

## Installation
### Python 3.8.10
1. Run the binary (python-3.8.10-amd64.exe for Windows, see https://www.python.org/downloads/release/python-3810/ for other operating systems)
2. Deselect 'Install launcher for all users (recommended)'
3. Select 'Add Python 3.8 to PATH' though it probably won't work!
4. Click 'Install now'

#### NOTE:
Default Path to Python Executable: `c:/Users/db524/AppData/Local/Programs/Python/Python38/python.exe`, substitute any reference to 'python' or 'python3' with this.
Default Path to PIP Executable: `c:/Users/db524/AppData/Local/Programs/Python/Python38/Scripts/pip3.8.exe`, substitute any reference to 'pip', 'pip3', or 'pip3.8' with this.

### Virtual Environment
1. Create a virtual environment by running `c:/Users/db524/AppData/Local/Programs/Python/Python38/python.exe -m venv venv`
2. Activate your virtual environment by running ```./venv/Scripts/activate``` (```./venv/bin/activate``` for Unix systems)
3. Run ```c:/Users/db524/AppData/Local/Programs/Python/Python38/Scripts/pip3.8.exe install -r ./requirements.txt``` to install dependencies

## Adding Packages
1. Use pip to install them
2. Run ```pip freeze > requirements.txt``` to save a full requirements list back
3. If intended to be a mainstay in this repo, git push back to master

## GPU Support
You may have to download CUDA: https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exe_local