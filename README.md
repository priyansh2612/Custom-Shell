# Custom Shell Project

### Developer: Priyansh Sharma  
**Roll No:** 21EE10003  
**Institution:** Indian Institute of Technology, Kharagpur

---

## Table of Contents

1. [Introduction](#introduction)  
2. [Features](#features)  
3. [Project Structure](#project-structure)  
4. [Files Overview](#files-overview)  
5. [Usage](#usage)  
6. [Dependencies](#dependencies)  
7. [Compilation](#compilation)  
8. [Execution](#execution)  

---

## Introduction

This project implements a custom shell in C++, providing a simple command-line interface with basic functionality. The shell supports command execution, input/output redirection, piping, and process control, similar to a typical UNIX shell.

## Features

- **Command Execution:** Execute standard shell commands.  
- **Input/Output Redirection:** Redirect input and output using `<` and `>`.  
- **Piping:** Use the `|` symbol to pass the output of one command as input to another.  
- **Background Processes:** Execute commands in the background using `&`.  
- **Custom Commands:** Includes additional features like custom `delep` and `sb` commands.  
- **Signal Handling:** Handles signals like `SIGINT`, `SIGTSTP`, and `SIGCHLD` to manage interruptions and background processes.

## Project Structure

- `main.cpp`: The main entry point of the shell, handling the command parsing, execution, and signal management.  
- `lock.cpp`: Demonstrates file locking using `flock` in a concurrent environment.  
- `test.cpp`: A test program showcasing thread synchronization using `pthread` and process creation using `fork`.  
- `utility.cpp`: Contains utility functions for command parsing, history management, wildcard handling, and process management.

## Files Overview

1. **`main.cpp`**  
   The core of the shell, responsible for reading user input, parsing commands, and executing them. It includes signal handling for `SIGINT`, `SIGTSTP`, and `SIGCHLD`.  

2. **`lock.cpp`**  
   A program to demonstrate file locking with the `flock` system call. It creates a child process that writes to a file under a lock to prevent concurrent access.  

3. **`test.cpp`**  
   A testing file that demonstrates the use of `pthread` for thread synchronization and `fork` for creating child processes.  

4. **`utility.cpp`**  
   Provides utility functions like command history management, input parsing, wildcard expansion, and custom commands like `delep`.  

## Usage

- **Executing Commands:** Simply type commands as you would in any standard shell. The shell supports standard commands, piping, redirection, and background processes.  
- **Custom Commands:**  
   - `delep <filename>`: Delete a file using custom logic.  
   - `sb <args>`: Execute a custom script or command with the given arguments.

## Dependencies

- **C++ Compiler:** g++ or any other modern C++ compiler.  
- **POSIX Libraries:** Required for system calls, threading, and signal handling.

## Compilation

To compile the project, use the following command in the terminal:

```bash
g++ -o shell main.cpp lock.cpp test.cpp utility.cpp -lreadline -pthread
```

## Execution

After compiling, you can run the shell by executing:

```bash
./shell
```

The shell will display a prompt, and you can start typing commands. To exit, type `exit`.

---
