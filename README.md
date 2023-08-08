# miniconda_ubuntu
A comprehensive guide on how to download, install, and use Miniconda. This guide includes steps for creating and activating Conda environments, installing packages within specific environments, and running Python scripts within a chosen environment.


# Miniconda Installation Guide

## Downloading and Installing Miniconda

1. Download Miniconda using the following link:
   [Miniconda3-py310_22.11.1-1-Linux-x86_64.sh](https://repo.anaconda.com/miniconda/Miniconda3-py310_22.11.1-1-Linux-x86_64.sh)
2. Navigate to your downloads directory:
   ```
   cd path_to_your_downloads_directory
   ```
3. Make the downloaded file executable:
   ```
   chmod +x Miniconda3-py310_22.11.1-1-Linux-x86_64.sh
   ```
4. Run the installer:
   ```
   ./Miniconda3-py310_22.11.1-1-Linux-x86_64.sh
   ```
5. Follow the on-screen instructions. Accept the licenses and type "yes" when prompted. Install it to the default location.

## Post-Installation

- Close and reopen your terminal. You should now see a `(base)` indicator at the beginning of the command prompt, signaling that Miniconda was installed successfully.

- The official [Conda Cheat Sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf) is a helpful resource.

## Creating a Conda Environment

To create a new environment with a specific Python version, use:

```
conda create --name your_environment_name python=desired_python_version
```
Example:
```
conda create --name mae python=3.8
```
Note: Some projects may require a specific Python version.

## Activating a Conda Environment

1. List all available environments:
   ```
   conda env list
   ```
2. Activate the desired environment:
   ```
   conda activate your_environment_name
   ```

Once activated, you'll notice the `(base)` indicator changes to `(your_environment_name)`.

## Installing Packages to a Specific Environment

To ensure a clean Python installation, use Conda environments instead of modifying the base Python installation.

1. Navigate to your project workspace.
2. Activate the desired Conda environment.
3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

## Running a Python Script in a Conda Environment

1. Open a terminal in the directory containing your `main.py` file.
2. Activate the desired Conda environment.
3. Run your script:
   ```
   python main.py
   ```
