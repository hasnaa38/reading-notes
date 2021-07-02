# read 05 
In this file a summary of *Read: 05 - Operators and Loops* will be provided. The file includes a summary of multiple articles, them being: 
[Expressions and operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators) // [Loops and iterations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration). 

## JavaScript Operators and Expressions

### Topic 1 - JavaScript Operators
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

| A      | B      | A or B |
|--------|--------|--------|
| True   | True   | True   |
| True   | False  | True   | 
| False  | True   | True   | 
| False  | False  | False  |

#### Not truth table: 

| A      | !A    |
|--------|-------|
| True   | False |
| False  | True  | 


### Topic 2 - JavaScript Expressions
An expression is any valid unit of code that resolves to a value.
conceptually, there are two types of expressions:

1. Expressions with side effects - for example: `x = 8` is an expression that used the `=` operator to assign the value 8 to the variable x. 

2. Expressions that evaluate and therefore resolve to a value - for example: `4 + 4` is an expression that uses the `+` operator to add 4 and 4 together without assigning the result to a variable.



## Loops and iteration

Loops offer a quick and easy way to do something repeatedly. There are different kinds of loops, but they all essentially do the same thing: they repeat an action some number of times. The main loop statements provided in JavaScript are: 

### for statement 
A for loop repeats until a specified condition evaluates to `false`. Syntax: 
```
for ([initial expression]; [condition]; [increment expression]) {
  statement 
}
```

#### Execution:

1. The initializing expression initializes one or more loop counters. An example of an initializing expression would be `var i = 0` . 
2. The condition expression expression is evaluated: 
- if the value of condition is true, the loop statements execute. 
- if the value of condition is false, the for loop terminates. 

_**Note**_ if the condition expression is omitted entirely, the condition is assumed to be true.

3. The statement executes. 

4. The update expression (increment expression) is executed.

5. Control returns to Step 2.

### while statement

A while statement executes its statements as long as a condition evaluates to true. If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop. Syntax: 
```
while (condition) {
  statement
}
```
