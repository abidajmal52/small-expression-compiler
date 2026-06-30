# Small Expression Compiler using Flex & Bison

A Small Expression Compiler developed using Flex and Bison that performs lexical analysis, syntax analysis, semantic analysis, expression evaluation, symbol table management, and compiler error detection.

## Features

✔ Lexical Analysis

- Keywords
- Identifiers
- Operators
- Integer constants
- Floating-point constants
- Parentheses

✔ Syntax Analysis

- Arithmetic expressions
- Assignment statements
- Operator precedence
- Associativity

✔ Semantic Analysis

- Undeclared variable detection
- Type checking
- Expression evaluation

✔ Symbol Table

- Identifier storage
- Data type
- Scope
- Initialization status
- Runtime value

✔ Error Detection

- Lexical errors
- Syntax errors
- Semantic errors
- Line number reporting

---

## Technologies

- C
- Flex
- Bison
- GCC

---

## Project Structure

```
src/
generated/
test/
docs/
```

---

## Compilation

Generate lexer

```bash
flex lexer.l
```

Generate parser

```bash
bison -d parser.y
```

Compile

```bash
gcc main.c lex.yy.c parser.tab.c symbol_table.c -o compiler -lm
```

Run

```bash
./compiler test/input.txt
```

---

## Sample Input

```c
int main(){
int a,b;
a=10+5;
b=a*2;
c=b+d;
return 0;
}
```

---

## Sample Output

```
=== Evaluation Results ===

Line 5:
Semantic Error:
Undeclared variable d

Compilation Summary

Lexical Errors : 0
Syntax Errors : 0
Semantic Errors : 1

Status : FAILED

Symbol Table

Name      Type   Scope   Initialized   Value
---------------------------------------------
a         int    global      yes        15
b         int    global      yes        30
```

---

## Compiler Components

- Lexical Analyzer
- Parser
- Symbol Table
- Expression Evaluator
- Semantic Checker
- Error Handler

---

## Extra Features

- Floating-point support
- Unary operators
- Built-in functions
- Parenthesized expressions

---

## Future Improvements

- if-else statements
- loops
- functions
- arrays
- strings
- AST generation
- Intermediate Code Generation
- Assembly Code Generation

---

## Author

Abid Ajmal Tahmid

Compiler Laboratory Project

Department of Computer Science & Engineering,

Bangladesh University of Professionals,Mirpur,Dhaka-1216,Bangladesh
