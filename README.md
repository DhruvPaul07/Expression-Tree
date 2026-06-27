[README_ExpressionTree.md](https://github.com/user-attachments/files/29417954/README_ExpressionTree.md)

# Expression Tree

**Course:** IB Computer Science SL
**Year:** Junior Year, Semester 1

## Description

A Java prefix-expression parser built on a binary tree structure. The user enters a prefix expression as a string; the program recursively constructs a tree and evaluates it. Supports standard arithmetic operators as well as special single-character operators for modular division, hypotenuse calculation, negation, and factorial.

## Files

| File | Purpose |
|---|---|
| `ENode.java` | Expression node storing a character operator/operand and its computed integer value |
| `ETree.java` | Tree class with recursive `insert` (parser + evaluator), `prefix`, `infix`, and `postfix` traversals |
| `MyProgram.java` | Driver — reads a prefix expression, builds the tree, and prints the result |

## How to Run

```bash
javac *.java
java MyProgram
```

Enter a prefix expression when prompted, e.g., `+34` → result: `7`.

## Supported Operators

| Symbol | Operation |
|---|---|
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `c` | `(left % right) + (left / right)` |
| `h` | Hypotenuse: `√(left² + right²)` |
| `n` | Negation: `-left` (unary) |
| `f` | Factorial of left operand (unary) |

## Example

Input: `*+23-54`

Tree structure:
```
      *
     / \
    +   -
   / \ / \
  2  3 5  4
```
Result: `5 * 1 = 5`

## Key Concepts

- Prefix (Polish notation) parsing via recursive descent
- Binary tree evaluation with operator dispatch
- In-order, pre-order, and post-order traversal methods
