# Operating Entity

**Operating Entity** is a lightweight operating system-like project that aims to provide an efficient and secure environment similar to a traditional operating system but without the complexity typically associated with them. The project is highly modular and provides a customizable platform for various use cases, including command-line interfaces (CLI), graphical user interfaces (GUI), and more.

## Features

- **Lightweight design**: Operates with minimal resources, making it suitable for small and embedded systems.
- **Custom bootloaders**: Includes different bootloaders (`yLoader`, `xLoader`, `VgaLoader`, `Winshell Disto`) for various configurations and requirements.
- **Modular architecture**: The system is divided into different components such as `.oe` files, `.oew` files,  `.entity`,and `.oec` files for configuration and script execution.
- **Z++ Assembely**: Provides a unique language for scripting within the system, allowing users to automate tasks and customize system behavior.
- **Virtual Space**: Executes programs in a virtualized environment to ensure isolation and stability.
- **Extensibility**: You can add new components or modify the existing ones by creating and modifying configuration files.

## Project Structure

The project consists of several key components:

1. **Bootloaders**:
   - `yLoader`: Used for CLI-based Operating Entity configurations.
   - `xLoader`: Used for GUI-based Operating Entity configurations.
   - `VgaLoader`: Designed for environments that require legacy VGA graphics.
   - `Winshell Disto`: A dynamic bootloader offering the most complex and powerful booting mechanism.

2. **Files**:
   - `.oe`: Main Operating Entity files.
   - `.oew`: Files containing specific configurations.
   - `.oec`: Script files for configuring the outputs and behaviors of the system.

3. **Execution**: The system executes the configuration files within the "output" directory and generates a file named `[ProjectName].Entity`, which can be run in the Virtual Space.

## Installation

### Prerequisites

Before running the project, ensure that you have the following installed:

- .NET runtime (if applicable for running the project code)
- A terminal or command prompt for interacting with the CLI components.
