# portable-python
A quick tutorial for installing a python environment (including PyTorch with Cuda) for machine learning on a PC that isn't yours. Primarily targetted at Informatics Students at the University of Sussex, though it should be applicable elsewhere.

**Colab is convenient, but if it's kicking you off, it would be silly not to use the i9-12900 and RTX A4000 under your desk!**

## Steps

### 1. Install Python 3.8.10
As it's a good version for compatibility with lots of machine learning packages which aren't updated too often. In future, you may wish to use 3.9 or 3.10 when 3.8 becomes end of life (see https://devguide.python.org/versions/).
1. **Open the installer**, which is included for Windows users (`python-3.8.10-amd64.exe`, for Mac and Linux see https://www.python.org/downloads/release/python-3810/).
2. **Deselect 'Install launcher for all users (recommended)' checkbox**. On managed PCs this will be an admin-only action, but just installing for just you won't be.
3. **(Optional) Select 'Add Python 3.8 to PATH'** to add python3.8 and pip3.8 commands to your command line. Note: Changes to windows path variables require a restart to take effect so this may not be very useful if you can't physically restart the PC you're using. 
4. **Click 'Install now'**.

### 2. Clone this repository to your machine
For ease, this guide uses GitHub Desktop, which should be found on Software Hub. 

1. Once launched and signed in, select 'Clone a repository from the Internet...' or if you've used GitHub Desktop before, select File->'Clone Repository...'. 
2. Select the 'URL' tab on the far right, and enter either your current URL, or danbates1452/portable-python. 
3. Hit clone
4. By default, a clone of this repo should appear in `C:\Users\<USER>\Documents\GitHub\portable-python`. Navigate there for the next step.

### 3. Setting up your Virtual Environment
Note: This section takes place in your command line/terminal of choice, as long as you're working directory is your local clone of this repository. You may want to be using something like VSCode for both your terminal and code editting.
1. Create a virtual environment by running Python from it's installed path. In windows: `python -m venv venv` (or the following for those without Python 3.8.10 in path: `c:/Users/<User>/AppData/Local/Programs/Python/Python38/python.exe -m venv venv`). You should see your virtual environment has been created in the subdirectory 'venv'.
2. Activate your virtual environment by running its activate script: ```./venv/Scripts/activate``` . You can now use 'pip' and 'python' freely as they're in the PATH of your new virtual environment.
3. Run ```pip install -r ./requirements.txt``` to install some recommended packages.
4. (Optional) To install PyTorch with Cuda, run ```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117```. This must be done after the other requirements to avoid conflicts.
5. Should you want to deactivate your virtual environment, just run `deactivate` since this too will be in your virtual environments PATH.
## Additional Notices
### Adding Packages
- It's best practice to add them to your requirements.txt
- Or use pip to install them directly e.g. `pip install <package_name>`


### Saving your work
- You should probably save your work in another git repository, so to remove this directory from git run both `del /f /s /q .git\*` and `rmdir /s /q .git`. `rm -rf .git/*` should also work but was not available on Lab PCs when tested. Using the wildcard `.git\*` leaves behind the included .gitignore file which will prevent you from adding your virtual environment files to your new git repository.
- You may be tempted to use OneDrive, but don't. The hundreds of small files in your virtual environment's packages will take ages to sync. If you must use a network drive, and are at sussex, use Home Share (N:). 

### GPU Support
It should be pre-installed on Lab PCs, but may need to download CUDA before you can use or install it with PyTorch: https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exe_local

## Contributions
You're more than welcome to suggest changes via GitHub issues. Or better yet, via pull requests.