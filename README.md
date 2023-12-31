# pymodulegen
[![Python unittests](https://github.com/YashNarK/pymodulegen/actions/workflows/python-ci.yml/badge.svg)](https://github.com/YashNarK/pymodulegen/actions/workflows/python-ci.yml)
[![Version](https://img.shields.io/badge/version-0.0.8-blue)](https://github.com/YashNarK/pymodulegen/releases)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgments)
- [Contact](#contact)
- [Examples and Screenshots](#examples-and-screenshots)


## Description

pymodulegen is a project aimed to generate python modules and packages, and add root directory of the project in sys path to allow importing parent modules in child using absolute paths relative to root directory.

## Issue Resolution

This section outlines the types of issues and problems that our package, `pymodulegen`, is designed to address. If you encounter any of the following scenarios, our package can be a valuable solution:

### Problem 1: Importing modules from parent packages

Since Python 3.3, referencing or importing a module in the parent directory is not allowed. Hence, we must handle it manually.
For example, in a folder structure like the one below,
```
.
    ├── directory_tree.txt
    └── src
        ├── main.py
        └── api
            ├── __init__.py
            └── common
                ├── load_environment.py
                ├── __init__.py
            └── v1
                ├── __init__.py
                └── endpoints
                    ├── chat.py
                    ├── __init__.py

```

If you wish to import 'load_environment' into 'chat.py', you will get the following error:

chat.py:
```
from src.api.common import load_environment
```
Error:
```
  File "your-machine-path\project-root\src\api\v1\endpoints\chat.py", line 1, in <module>
    from src.api.common import load_environment
ModuleNotFoundError: No module named 'src'
```

### Problem 2: Creating folder structures, packages and modules for a python project

Currently, in Python development, we have to either manually create files and folders (along with __init__.py files) or use a third-party template provider like Cookiecutter, FastAPI Project Generator,Django-style CLI, etc. However, if you want to generate packages as per your liking in a custom fashion, it can only be done manually for the time being.

## How Our Package Helps

When we setup the folder structures using our package, it includes codes in the __init__.py file (or in the module itself, depending on the user preference), which will allow us to do imports using absolute paths (not relative paths, like the usage of '.','..') even from parent packages.
Also, it is pretty easy to setup folder structures using our command-line tool rather than doing it manually.

## Installation

### Using pip
   ```bash
   pip install pymodulegen
   ```
### Clone from source
   ```bash
   git clone https://github.com/YashNarK/pymodulegen.git
   ```


## Usage
To generate a module or package and set root directory, use the following command:

```bash
pymodulegen module_name [--options]
```

Options:
- `module_name`: The name of the module to generate.
- `--directory`: (Optional) The directory where the module should be created.
- `--root_directory`: (Optional) The root directory for sys.path.
- `--is_module_only`: (Optional) Specify if the module should be used as a module only.
- `--not_is_module_only`: (Optional) Specify if the module should be used as a main program as well

## Contributing

Contributions are welcome! Please follow these guidelines:

1. Create an issue to discuss major changes or enhancements.
2. Fork the repository and create a new branch for your contribution.
3. Submit a pull request with a clear description of your changes.
4. Follow coding standards and maintain code quality.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgments

I would like to acknowledge the following resources that were helpful during the development of this project:

- [GeeksforGeeks - Python Import from Parent Directory](https://www.geeksforgeeks.org/python-import-from-parent-directory/): This tutorial provided valuable insights into importing modules from parent directories in Python. It was a useful reference while working on this project.


## Contact

- Email: narenkrithick@gmail.com
- GitHub: [YashNarK](https://github.com/YashNarK)

## Examples and Screenshots

### Example 1

[![Screenshot 1](https://raw.githubusercontent.com/YashNarK/pymodulegen/main/images/screenshot1.png)](https://raw.githubusercontent.com/YashNarK/pymodulegen/main/images/screenshot1.png)

Generate a module named "mymodule" in the current directory (default settings).

### Example 2

[![Screenshot 2](https://raw.githubusercontent.com/YashNarK/pymodulegen/main/images/screenshot2.png)](https://raw.githubusercontent.com/YashNarK/pymodulegen/main/images/screenshot2.png)

Generate a module named "chatgpt" in the "app/api/v1/endpoints" directory with root directory "project-root" and use it as a main program as well.

### Example 3

[![Screenshot 3](https://raw.githubusercontent.com/YashNarK/pymodulegen/main/images/screenshot3.png)](https://raw.githubusercontent.com/YashNarK/pymodulegen/main/images/screenshot3.png)

Generate a package (with __init__.py) named "my_package" in the current directory (default settings) with a module my_module.

