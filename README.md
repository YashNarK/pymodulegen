# pymodulegen

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://example.com/build)
[![Version](https://img.shields.io/badge/version-0.0.1-blue)](https://github.com/YashNarK/pymodulegen/releases)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Command-Line Interface](#command-line-interface)
- [Contributing](#contributing)
- [License](#license)

## Description

pymodulegen is a project aimed to generate python modules and packages, and add root directory of the project in sys path to allow importing parent modules in child using absolute paths relative to root directory.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/YashNarK/pymodulegen.git
   ```

2. Navigate to the project directory:
   ```bash
   cd src\pymodulegen
   ```



## Usage

Explain how to use your project and provide code examples, screenshots, or GIFs if applicable.

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

### Other CLI Commands

Provide documentation for other CLI commands if your project has them.

## Contributing

Contributions are welcome! Please follow these guidelines:

1. Create an issue to discuss major changes or enhancements.
2. Fork the repository and create a new branch for your contribution.
3. Submit a pull request with a clear description of your changes.
4. Follow coding standards and maintain code quality.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgments

- Mention any contributors, libraries, or resources that helped you in building your project.

## Contact

- Email: your.email@example.com
- GitHub: [yourusername](https://github.com/yourusername)

## Additional Sections

Add any additional sections relevant to your project, such as "Troubleshooting," "Changelog," "Demo," etc.

## Examples and Screenshots

Include examples, screenshots, or GIFs of your project in action to showcase its features.
```

Feel free to copy and paste this template into your README.md file and customize it according to your project's details.