# pymodulegen

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://example.com/build)
[![Version](https://img.shields.io/badge/version-0.0.1-blue)](https://github.com/YashNarK/pymodulegen/releases)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

## Table of Contents
- [Installation](#installation)
- [Command-Line Interface](#command-line-interface)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgments)
- [Contact](#contact)


## Description

pymodulegen is a project aimed to generate python modules and packages, and add root directory of the project in sys path to allow importing parent modules in child using absolute paths relative to root directory.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/YashNarK/pymodulegen.git
   ```

2. Navigate to the project directory:
   ```bash
   cd pymodulegen\src\pymodulegen
   ```



## Command-Line Interface

### Generate Module

To generate a module, use the following command:

```bash
python main.py modulegen module_name [--options]
```

Options:
- `module_name`: The name of the module to generate.
- `--directory`: (Optional) The directory where the module should be created.
- `--root_directory`: (Optional) The root directory for sys.path.
- `--is_module_only`: (Optional) Specify if the module should be used as a module only.

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


