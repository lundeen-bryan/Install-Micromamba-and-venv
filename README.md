<div align='center'>

# CREATE VIRTUAL ENVIRONMENT WITH MICROMAMBA BASH SCRIPT

*This Bash script automates the process of creating a Python virtual environment using [Micromamba](https://micromamba.snakepit.net/). It's a convenient tool for Python developers to manage isolated Python environments for their projects.*


</div>

__Table of Contents__

<!-- TOC -->

- [1. About](#1-about)
- [2. Prerequisites](#2-prerequisites)
- [3. Purpose](#3-purpose)
- [4. Usage](#4-usage)
- [5. Activation](#5-activation)
- [6. Troubleshooting](#6-troubleshooting)

<!-- /TOC -->

## 1. About

This Bash script simplifies the process of creating and managing Python virtual environments using Micromamba. Whether you are a Python developer, data scientist, or simply need a clean and isolated environment for your Python projects, this script can help streamline the setup process.

**The Need for Virtual Environments**

Python virtual environments are essential for isolating and managing Python projects' dependencies. They allow you to create separate, self-contained environments for different projects, preventing conflicts between packages and ensuring consistent development environments. This ensures that each project can use its own set of Python packages, without interfering with system-wide installations or other projects.

**Why Use Micromamba?**

Micromamba is a fast, lightweight, and efficient package manager designed specifically for managing Conda-based environments. It offers advantages over traditional package managers, making it an excellent choice for managing Python virtual environments:

- **Lightweight**: Micromamba is a smaller footprint compared to Anaconda, making it quick to install and easy to work with.
- **Efficient**: It provides faster package management and dependency resolution, reducing the time it takes to create and update environments.
- **Conda Compatibility**: Micromamba is fully compatible with Conda environments and packages, allowing you to switch between tools seamlessly.

## 2. Prerequisites

Before using this script, ensure the following prerequisites are met:

1. **Git-Bash**: Install Git-Bash on your system.
2. **Micromamba**: Make sure Micromamba is properly installed and available in your system's PATH.

## 3. Purpose

This script simplifies the process of creating a Python virtual environment with Micromamba. It allows you to specify the Python version and the name of the virtual environment. Additionally, you can choose to install packages from a `requirements.txt` file within the virtual environment.

## 4. Usage

1. **Download the Script**:

   You can download the Bash script file provided in this repository.

2. **Run the Script**:

   Open your terminal (Git-Bash or similar) and navigate to the directory where the script is located. Run the script by executing:

   ```bash
   bash create_python_virtual_env.sh
   ```

3. **Script Execution**:

   - The script will prompt you to confirm if you want to proceed. Type `Y` or `yes` to continue; otherwise, type `N` or `no` to exit the script.
   - You will be asked to enter the Python version (e.g., `3.8`) you want to use in the virtual environment.
   - Optionally, you can specify a custom environment name; pressing Enter will use the default name `.venv`.
   - Micromamba will create the virtual environment with the provided Python version.

4. **Install Packages from `requirements.txt`**:

   - If a `requirements.txt` file is found in the same directory as the script, you will be asked if you want to install packages from it. Type `Y` or `yes` to proceed.
   - The script will activate the virtual environment and install packages from `requirements.txt`. If the activation fails, you may need to restart your shell.

5. **Completion**:

   - Once the process is complete, the script will display a success message with instructions on how to activate your environment.
   - If an error occurs during execution, you can view the log file (`install_log.txt`) to diagnose issues.

## 5. Activation

To activate the newly created virtual environment, use the following command:

```bash
micromamba activate <env_name>
```

Replace `<env_name>` with the name you provided during script execution (or use the default name, `.venv`).

## 6. Troubleshooting

If you encounter any issues or errors during the script's execution, you can review the log file (`install_log.txt`) for more information. You can also open the log file using the script if prompted.

If you encounter problems activating the environment, consider restarting your shell.

---

Feel free to use this script to streamline your Python development workflow and manage isolated Python environments with ease. If you have any feedback or encounter issues, please report them in this repository's issues section.

[⭡backtotop](#1-about)
