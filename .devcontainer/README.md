# Dev Container Configuration

This directory contains the configuration for GitHub Codespaces and VS Code Dev Containers.

## What is a Dev Container?

A development container (or dev container for short) allows you to use a container as a full-featured development environment. This project's dev container is configured to provide:

- Python 3.11 environment
- Jupyter Notebook support
- All required Python packages (automatically installed from `requirements.txt`)
- Pre-configured VS Code extensions for Python and Jupyter development
- Git and GitHub CLI tools

## Using GitHub Codespaces

To create a Codespace for this repository:

1. Navigate to the repository on GitHub
2. Click the green "Code" button
3. Select the "Codespaces" tab
4. Click "Create codespace on main" (or your preferred branch)

GitHub will automatically:
- Create a cloud-based development environment
- Install Python 3.11
- Install all dependencies from `requirements.txt`
- Set up Jupyter Notebook extensions
- Open VS Code in your browser

## Using VS Code Dev Containers Locally

If you have Docker and VS Code installed locally:

1. Install the "Dev Containers" extension in VS Code
2. Open this repository in VS Code
3. Press `F1` and select "Dev Containers: Reopen in Container"
4. Wait for the container to build and start

## What Gets Installed

The `devcontainer.json` configuration includes:

- **Base Image**: Python 3.11 official dev container
- **VS Code Extensions**:
  - Python (Microsoft)
  - Pylance (Python language server)
  - Jupyter
  - Jupyter Keymap
  - Jupyter Renderers
- **Python Packages**: All packages from `requirements.txt`:
  - pandas >= 1.3.0
  - numpy >= 1.21.0
  - matplotlib >= 3.4.0
  - seaborn >= 0.11.0
  - scikit-learn >= 1.0.0
  - jupyter >= 1.0.0

## Working with the Notebook

Once your Codespace is ready:

1. Open `fraud_detection.ipynb` in VS Code
2. Select the Python kernel (should be auto-detected)
3. Run cells individually or all at once
4. Note: You'll need to provide your own `fraudTest.csv` dataset

## Troubleshooting

**Packages not installed?**
- The `postCreateCommand` runs `pip install --user -r requirements.txt` automatically
- If needed, you can manually run: `pip install -r requirements.txt`

**Jupyter kernel not found?**
- Reload the window: Press `F1` and select "Developer: Reload Window"
- Or manually install: `pip install jupyter ipykernel`

**Need additional packages?**
- Install them with: `pip install <package-name>`
- To make them permanent, add them to `requirements.txt`

## Customizing the Environment

To modify the dev container configuration:

1. Edit `.devcontainer/devcontainer.json`
2. Rebuild the container: `F1` → "Dev Containers: Rebuild Container"

For more information, see the [Dev Containers documentation](https://containers.dev/).
