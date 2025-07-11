# GitHub Codespaces


GitHub Codespaces provides a cloud-based development environment that is ideal for data science work with Python. It allows you to develop, run, and collaborate on code directly from your browser or VS Code, with all dependencies and tools pre-installed.

## 1. Managing Codespaces
- **GitHub Codespaces Dashboard:** From your GitHub profile, click your avatar (top right) and select "Your codespaces" to see all your codespaces across repositories.
- **Create:** Click the green "Code" button on your repository and select "Create codespace on main".
- **Start/Stop:** To stop a codespace, use the Codespaces dashboard on GitHub and click the "..." menu next to your codespace, then select "Stop". You can also stop a running codespace from within VS Code by opening the Command Palette (`Ctrl+Shift+P`), searching for "Codespaces: Stop Current Codespace", and selecting it.
- **Rebuild:** To rebuild a codespace, use the "Rebuild Container" option from the Codespaces dashboard on GitHub, or in VS Code open the Command Palette and search for "Codespaces: Rebuild Container".
- **Delete:** Delete unused codespaces from the Codespaces dashboard by clicking the "..." menu next to your codespace and selecting "Delete".

## 2. Using Git in Codespaces
Codespaces comes with Git pre-installed. Use the built-in terminal or VS Code Source Control panel to clone, commit, push, pull, and manage branches as you would locally.

## 3. devcontainer.json Configuration Basics

The `.devcontainer/devcontainer.json` file customizes your codespace environment:
- **Python Environment:** Specify the Python version and base image (e.g., `mcr.microsoft.com/devcontainers/python`).
- **Installing Dependencies:** Use `requirements.txt` or `conda` in the `postCreateCommand` to install packages automatically.
- **VS Code Extensions & Settings:** List extensions in the `extensions` array and customize settings in `settings`.
- **Lifecycle Commands:**
  - `onCreateCommand`: Runs once when the container is created.
  - `postCreateCommand`: Runs after the container is built (commonly used for installing dependencies).
  - `postAttachCommand`: Runs each time you attach to the codespace.

**Example `devcontainer.json`:**
```json
{
	"name": "Python 3 devcontainer",
	"image": "mcr.microsoft.com/devcontainers/python:0-3.11",
	"onCreateCommand": "pip install --user -r requirements.txt",
	"customizations": {
	  "vscode": {
		"settings": {
			"python.defaultInterpreterPath": "/usr/local/bin/python3",
		},
		"extensions": [
		  "ms-python.python",
		  "ms-toolsai.jupyter",
		]
	  }
	},
	"postAttachCommand": "htop"
}
```

## 4. Using Secrets in Codespaces
Store sensitive information (like API keys) as secrets in your repository settings under Codespaces > Secrets. Access these secrets as environment variables in your codespace without exposing them in code.

## 5. Setting Up Codespace Prebuilds
Prebuilds automatically prepare your codespace with dependencies and settings, reducing setup time. Enable prebuilds in your repository settings under the Codespaces tab.