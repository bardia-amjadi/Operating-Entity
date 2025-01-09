# Z++ Assembly

## Overview
Z++ Assembly is a lightweight virtual assembly engine designed for processing and executing scripts in the Z++ language. It interprets high-level commands to execute logical operations, manage loops and conditions, handle imports, and interact with user input/output.

## Features
- **Conditional Execution**: Supports `IF`, `ELSE`, and `ENDIF` statements.
- **Loops**: Implements `LOOP` and `ENDLOOP` for iterative execution.
- **File Imports**: Includes external scripts using the `IMPORT` keyword.
- **Dynamic Variables**: Create and manage variables using `NEW`.
- **I/O Operations**: Supports user interaction via `PRINT`, `input()`, and `keyboard()`.

## Script Syntax

### Conditional Statements
```txt
IF condition
    [commands]
ELSE
    [commands]
ENDIF
```
- `==`: Checks equality.
- `!=`: Checks inequality.

### Loops
```txt
LOOP n
    [commands]
ENDLOOP
```
Executes the block `n` times. Use `BREAK` to exit and `SKIP` to skip the current iteration.

### Importing Files
```txt
IMPORT [file_path] AS alias
alias.EXCUTE()
```
Loads and executes the content of an external file.

### Printing
```txt
PRINT 'Your message here'
ENDLINE
```
Outputs text to the console.

### Creating Variables
```txt
NEW value variable_name
```
Creates a new variable with the given value.

### Input Handling
- `input()`: Reads a line of input.
- `keyboard()`: Captures a single key press.

## Example Scripts

### Kernel.txt
```txt
IMPORT [c:\main.txt] AS FORM
FORM.EXCUTE()
```

### Main.txt
```txt
PRINT 'Main Form'
ENDLINE
LOOP 3
    PRINT 'This is iteration'
    ENDLINE
ENDLOOP
```

### Expected Output
```txt
Main Form
This is iteration
This is iteration
This is iteration
```

## Code Structure

### Core Classes
- `EntityRegister`: Represents a variable or entity with a name, value, and optional parent.
- `OperatingEntity`: Manages the virtual space, including memory, files, and registers.
- `ZppAssembly`: The main interpreter for processing and executing Z++ scripts.
- `ImportSystem`: Handles external file imports and their execution.

## Extending the Assembly
- Add new commands by updating the `ZppAssembly.Assemble()` method.
- Expand conditional operations in `ZppAssembly.AssembleCondition()`.
- Enhance error handling for unrecognized commands or invalid syntax.

## Running the Program
1. Create a primary script (e.g., `Kernel.txt`).
2. Define additional scripts for import (e.g., `Main.txt`).
3. Load and execute the scripts using `ZppAssembly`.

## License
This project is open-source. Contributions and modifications are welcome!
