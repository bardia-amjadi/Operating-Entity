# Operating Entity

**Operating Entity** refers to projects such as lightweight operating systems that aim to provide a functional and secure environment similar to a modern operating system, but without the complexity usually associated with them. The project is highly modular and offers a customizable platform for different use cases, including command-line interfaces (CLI), graphical user interfaces (GUI), etc.
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
