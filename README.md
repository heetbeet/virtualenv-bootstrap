# VirtualEnv Bootstrap for Windows

This script, `virtualenv.cmd`, is designed for Windows users who need to create Python virtual environments without installing Python globally on their system. It acts as a shim to bootstrap an underlying Python binary, allowing you to specify the Python version and set up a virtual environment with ease.

## Features

- **Python Version Specification:** Allows specifying a Python version (3.x.x format) to bootstrap the virtual environment with that specific Python version.
- **No Global Python Installation Required:** Enables the creation of Python virtual environments on Windows machines without the need for a globally installed Python.
- **Automatic Python Download:** Downloads the specified or default Python version automatically from the official Python repository.

## Usage

1. **Download the Script:** Download `virtualenv.cmd` to your project directory or a known location on your system.

2. **Make Accessible Everywhere:** Optionally, add the script's directory to your system's PATH by running add-directory-to-user-path.cmd. This lets you use virtualenv.cmd from any command prompt without navigating to its folder.

3. **Open Command Prompt:** Navigate to the directory where you've placed `virtualenv.cmd` if it's not in your PATH.

4. **Run the Script:**
   - To create a virtual environment with the default Python version, simply run:
     ```
     virtualenv [ARGS]
     ```
   - To specify a Python version (e.g., 3.8.10), use the version as the first argument:
     ```
     virtualenv 3.8.10 [ARGS]
     ```

## How It Works

When `virtualenv.cmd` is executed, it:
- Checks if the first argument matches a Python version pattern (3.x.x).
- Downloads the specified (or default) Python version's embedded package from the official Python repository.
- Extracts the package to a temporary directory.
- Installs `pip` and `virtualenv`.
- Creates a virtual environment in the current directory or a specified path.

## License

This script is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).