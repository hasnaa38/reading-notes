# read 05 
In this file a summary of *Read: 05 - Operators and Loops* will be provided. The file includes a summary of multiple articles, them being: 
[Expressions and operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators) // [Loops and iterations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration). 

## JavaScript Operators
JavaScript has the following types of operators. The main ones are: 

- **Assignment operator ** `=` assigns a value to its left operand based on the value of its right operand.


- **Arithmetic operators** take 2 numerical operands and return a single numerical value.

| Operator      | Meaning |
| ----------- | ----------- |
| + | Addition|
| - | Subtraction |
| * | Multiplication |
| / | Division |
| % | Remainder |

_**Note**_ the addition operator `+` is used to add two numerical operands. However, if at least one of the ooerands is a string, it will be used as a concatenation operator that concatenates the values together. 


- **Comparison operators** compare their operands and return a logical value based on the comparison result (true or false).

| Operator      | Meaning |
| ----------- | ----------- |
| == | Equal to in value |
| != | Not equal to in value |
| === | Equal to in value and type |
| !== | Not equal to in value and type |
| > | Greater than |
| < | Less than |

- **Logical operators** 

| Operator      | Meaning |
| ----------- | ----------- |
| `&&` | And |
| `||` | OR |
| `!` | Not |

Each one of these operators has its own truth table: 

#### And truth table: 

| A      | B      | A && B |
|--------|--------|--------|
| True   | True   | True   |
| True   | False  | False  | 
| False  | True   | False  | 
| False  | False  | False  |

#### Or truth table: 

| A      | B      | `A || B` |
|--------|--------|--------|
| True   | True   | True   |
| True   | False  | True  | 
| False  | True   | True  | 
| False  | False  | False  |

#### Not truth table: 

| A      | !A    |
|--------|-------|
| True   | False |
| False  | True  | 



## Expressions
An expression is any valid unit of code that resolves to a value.



