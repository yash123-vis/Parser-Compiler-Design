
# Go Program Parser

This project features a parser built using Flex and Yacc, specifically designed to analyze and process Go programs. It performs lexical and syntax analysis based on the rules defined in the Flex and Yacc input files and generates output accordingly.

## Overview

The parser reads an input Go program, conducts lexical and syntax analysis, and produces an output based on predefined patterns and rules.

## Requirements

- **Flex** (Fast Lexical Analyzer)
- **Yacc** (Yet Another Compiler Compiler)
- **GCC** (GNU Compiler Collection)
- Windows or Unix-like operating system

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Generate the Parser

Run the following commands in the terminal:

```bash
flex lexer.l.txt
yacc -d parser.y.txt -Wno-yacc
g++ -w lex.yy.c ast.cpp ast.h y.tab.c -o gocompiler
```

These commands will generate an executable file named `gocompiler` (on Unix-like systems) or `gocompiler.exe` (on Windows).

### 3. Run the Parser

Execute the parser with the following command:

```bash
./gocompiler test.go
```

Replace `test.go` with the path to the Go file you want to parse.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request if you have suggestions or improvements.

## License

This project is licensed under the [MIT License](LICENSE).
