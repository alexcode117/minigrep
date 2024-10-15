# MiniGrep

MiniGrep is a simple command-line tool written in Rust that searches for a specified query string in a given file and prints the lines containing the query. This project demonstrates basic file I/O, command-line argument parsing, and modular code organization in Rust.

## Table of Contents

- [MiniGrep](#minigrep)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Project Structure](#project-structure)
    - [src/main.rs](#srcmainrs)
    - [src/lib.rs](#srclibrs)
  - [Usage](#usage)
  - [Implementation Details](#implementation-details)
    - [Config Struct](#config-struct)
    - [run Function](#run-function)
    - [search Function](#search-function)
  - [Future Improvements](#future-improvements)

## Features

- Search for a query string in a specified file
- Print matching lines from the file
- Simple and efficient implementation
- Modular code structure

## Project Structure

The project consists of two main Rust files:

1. `src/main.rs`: Contains the entry point of the application
2. `src/lib.rs`: Contains the core functionality and data structures

### src/main.rs

This file is responsible for:

- Parsing command-line arguments
- Creating a `Config` instance
- Running the main logic of the program

### src/lib.rs

This file contains:

- The `Config` struct and its implementation
- The `run` function, which reads the file and performs the search
- The `search` function, which finds matching lines in the content

## Usage

To use MiniGrep, run the compiled binary with two arguments:

1. The filename to search in
2. The query string to search for

Example:

$ cargo run filename.txt "search query"

The program will output:

1. The filename being searched
2. The query string being used
3. Any lines from the file that contain the query string

## Implementation Details

### Config Struct

The `Config` struct holds the filename and query string parsed from command-line arguments. It has a `new` method that creates a new `Config` instance from the provided arguments.

### run Function

The `run` function is the main logic of the program. It:

1. Reads the contents of the specified file
2. Calls the `search` function to find matching lines
3. Prints the matching lines

### search Function

The `search` function takes the query string and the file contents as input. It:

1. Iterates through each line of the content
2. Checks if the line contains the query string
3. If a match is found, adds the line to the results vector
4. Returns the vector of matching lines

## Future Improvements

1. Error handling: Implement proper error handling for file I/O and argument parsing.
2. Case-insensitive search: Add an option for case-insensitive searching.
3. Performance optimization: Explore more efficient search algorithms for larger files.
4. Multiple file support: Allow searching in multiple files or directories.
5. Regular expression support: Implement regex-based searching for more powerful queries.

Feel free to contribute to this project by submitting pull requests or opening issues for bugs and feature requests.
