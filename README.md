# portable-python
Easy to set up python environment for my own use in data science / machine learning projects. Comes with PyTorch (w/Cuda), and the usual suspects. See requirements.txt for the full list.

## Installation
### Python 3.8.10
1. Run the binary (python-3.8.10-amd64.exe for Windows, see https://www.python.org/downloads/release/python-3810/ for other operating systems)
2. Deselect 'Install launcher for all users (recommended)'
3. Select 'Add Python 3.8 to PATH' though it probably won't work!
4. Click 'Install now'

#### NOTE: (WINDOWS)
Default Path to Python Executable: `c:/Users/<User>/AppData/Local/Programs/Python/Python38/python.exe`, substitute any reference to 'python' or 'python3' with this.
Default Path to PIP Executable: `c:/Users/<User>/AppData/Local/Programs/Python/Python38/Scripts/pip3.8.exe`, substitute any reference to 'pip', 'pip3', or 'pip3.8' with this.

### Virtual Environment
1. Create a virtual environment by running Python from it's installed path (e.g. default in windows: `c:/Users/<User>/AppData/Local/Programs/Python/Python38/python.exe -m venv venv`).
2. Activate your virtual environment by running ```./venv/Scripts/activate``` (```./venv/bin/activate``` for Unix systems). From now on using the virtual environment version of pip (under venv/Scripts) and python.
3. Run ```.\venv\Scripts\pip3.8.exe install -r ./requirements.txt``` to install dependencies.
4. (Optional) You may also have to run ```.\venv\Scripts\pip3.8.exe install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117``` to get PyTorch to install with Cuda properly.

## Adding Packages
1. Use pip to install them
2. Run ```pip freeze > requirements.txt``` to save a full requirements list
3. Make sure to save your changes in a new repo!

## GPU Support
You may have to download CUDA: https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exe_local
