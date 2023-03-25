# Project Description
This is a compiler project built using Haskell and the **E-Graph open-source library (Egg)** for optimizing code. The compiler takes source code as input, performs *lexical analysis*, *parsing*, *semantic analysis*, *code generation and optimization*, and *generates machine code* as output.

* The project directory structure includes:
* `app/` directory containing the entry point of the application `(Main.hs)` and the optimizer module `(Optimizer.hs)`.
* `src/` directory containing the compiler modules `(Lexer.hs, Parser.hs, SemanticAnalyzer.hs, SymbolTable.hs, CodeGenerator.hs)` and a general library module **(Lib.hs)**.
* `test/` directory containing the test modules `(Spec.hs and subdirectories LexerSpec.hs, ParserSpec.hs, SemanticAnalyzerSpec.hs, SymbolTableSpec.hs, CodeGeneratorSpec.hs, and OptimizerSpec.hs)` using the **Hspec library**.
* The E-Graph library is used to represent and manipulate expressions, which is a key part of optimizing code. `The Optimizer.hs` module uses the egg library to perform various optimizations on the code generated by the compiler.

# About the Project

The goal of this project is to demonstrate the use of E-graphs as a powerful tool for optimizing code in compilers. E-graphs are a data structure that can be used to represent and manipulate expressions in a way that is both efficient and flexible.

By using E-graphs in the optimizer, this compiler is able to perform advanced optimizations on the generated code, such as constant folding and common subexpression elimination. This results in code that is faster and more efficient than what would be generated by a traditional compiler.

Overall, this project demonstrates the potential for E-graphs to be used in a variety of applications where efficient expression manipulation is required, including compilers, theorem provers, and program synthesizers.

# Directory Structure

```bash
.
├── app/
│   ├── Main.hs
│   └── Optimizer.hs
├── src/
│   ├── Compiler/
│   │   ├── Lexer.hs
│   │   ├── Parser.hs
│   │   ├── SemanticAnalyzer.hs
│   │   ├── SymbolTable.hs
│   │   └── CodeGenerator.hs
│   └── Lib.hs
└── test/
    ├── Spec.hs
    └── TestCompiler/
        ├── LexerSpec.hs
        ├── ParserSpec.hs
        ├── SemanticAnalyzerSpec.hs
        ├── SymbolTableSpec.hs
        ├── CodeGeneratorSpec.hs
        └── OptimizerSpec.hs
```

# Installation Instructions
## Prerequisites
To run this project, you need to have the following software installed on your system:

> The Haskell programming language (version 8.10 or later)
> The Rust programming language (version 1.55 or later)
## Setup
1. Clone the repository: ` git clone https://github.com/Vtewari2311/E-Graph-Optimizer.git `
2. Navigate to the project directory: ` cd project `
3. Install the required Haskell packages: ` cabal install --dependencies-only `
4. Build the project: ` cabal build `
5. Install the egg library: ` cargo install egg `
6. Start the application: ` cabal run `

## Testing
To run the tests, navigate to the project directory and run the following command: cabal test. This will run all the tests in the test/ directory.

# Usage Instructions
To use the compiler, create a file containing the source code to compile, and run the following command from the project directory: cabal run your-file-name. This will compile your code and generate machine code as output. If you want to optimize the code, add the -o flag: ` cabal run -o your-file-name `.


Additionally, To use the compiler, navigate to the app directory and run the Main executable. The executable takes a single argument, which is the path to the source code file that you want to compile. For example, to compile a source file named example.src, you would run the following command:

> ./Main ../example.src
The compiled code will be output to a file named out.s in the same directory as the source file.