# Mini Shell (C)

## Overview
Mini Shell is a C-based system programming project that implements a simplified version of a Unix/Linux command-line shell. It allows users to execute system commands, handle built-in commands, and manage processes using core Linux system calls.

This project provides hands-on experience with operating system concepts such as process creation, execution, and termination, making it highly relevant for system and embedded software roles.

## Features
- Execute external Linux commands
- Support for built-in commands (cd, exit, pwd, etc.)
- Command-line parsing
- Process creation using fork()
- Program execution using exec family
- Parent-child process synchronization using wait()
- Error handling for invalid commands

## Technologies Used
- Language: C
- Concepts:
  - Linux system calls
  - Process management
  - Command parsing
  - Pointers and memory handling
  - Modular programming

## Project Flow

### Command Execution Flow
1. Display shell prompt.
2. Read user input command.
3. Parse command and arguments.
4. Check for built-in commands.
5. If built-in:
   - Execute internally.
6. If external command:
   - Create child process using fork().
   - Execute command using exec().
   - Parent waits for child using wait().
7. Display prompt again.

## Usage

### Compilation
gcc *.c -o minishell

### Execution
./minishell

### Sample Commands
- ls
- pwd
- cd <directory>
- ps
- exit

## Project Structure
Mini-Shell/
│
├── shell.c
├── builtins.c
├── parser.c
├── execute.c
├── types.h
├── main.c
└── README.md

## Limitations
- No piping or redirection
- No background process support
- Limited built-in commands

## Future Enhancements
- Add piping and I/O redirection
- Support background execution (&)
- Implement command history
- Add signal handling (Ctrl+C, Ctrl+Z)

## Learning Outcomes
- Deep understanding of Linux process model
- Practical use of system calls
- Improved command parsing and debugging skills
- Strong foundation in operating system concepts

## Author
Syed Shifan Ali
